## To make `Worms20_MasterDo.do` run (using Citrix):

Starting from a fresh download of the [reproduction package](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/TTYMHI) for ['Twenty-year economic impacts of deworming'](https://www.pnas.org/content/118/14/e2023185118):

1. Open Stata via Citrix, and open `Worms20_MasterDo.do`
    - As instructed in `Twenty Year Impacts of Deworming - Data Replication_README.pdf`, change the global directory on line 13 to the folder containing your reproduction files, and add `\\Client` to the beginning
      - For example, if my reproduction files/folders (e.g. `do`, `data`, `ado`, and so on) are located at `C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker`, then I would change the directory on line 13 to be `\\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker`
      - This is because `\Client`, rather than `C:`, is the root directory for a user accessing Stata via Citrix. The additional backslash `\` is used to escape the backslash in the name of the root directory, so that Stata reads the file path correctly
    - If you try running `Worms20_MasterDo.do` right now, you will run into an error saying that some file already exists (error code `r(602)`). To fix this, we need to …

2. Set the location where `.ado` files will be installed
    - Berkeley provides a [guide](https://guides.lib.berkeley.edu/citrix/stata) to installing `.ado` files for Citrix users. Despite much testing, I could not get Stata to successfully install and/or recognize the required `.ado` files following Berkeley's guide
    - Here is my workaround:
      - Somewhere on your local machine, create a folder to store the `.ado` files you install from online. My folder is located at the path `C:\Users\myzha\Documents\Stata\ado`
      - Every single time you start up Stata via Citrix, you will need to enter the following two commands:
        - `sysdir set PLUS \\Client\insert_your_file_path_here`. For example, I would enter `sysdir set PLUS \\Client\C:\Users\myzha\Documents\Stata\ado`. This command tells Stata to change its default location for installing user-made `.ado` files from online (hence why the directory is named `PLUS`)
        - `sysdir set PERSONAL \\Client\insert_your_file_path_here`. I would enter `sysdir set PERSONAL \\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker\ado`. This command tells Stata to change its default location for installing personally made `.ado` files, e.g. the file `fdr_adjustment.ado`, which is provided in the reproduction package and required for the analysis, but cannot be installed from online
      - In the folder where `fdr_adjustment.ado` is located (in my case, `C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker\ado`), create a folder named `f` and place `fdr_adjustment.ado` inside. This is because when Stata searches its adopath, i.e. the list of directories where it will look for an `.ado` file, it looks first for a folder whose name is just the first letter of said file, and then looks for the file itself
    - As a sanity check, you can enter the command `adopath` to verify that the `PLUS` and `PERSONAL` directories have been appropriately changed. Once your packages are installed (this is done automatically by the `.do` files, except for `texdoc`, see below), you can enter `which package_name` (e.g. `which lincom`) to verify that they have been properly installed, and that Stata can find them
    - After all of this, you will need to enter the command `ssc install texdoc, replace` as well
      - This installs the package `texdoc` and replaces any previous installation. It should be found in your new `PLUS` directory
    - If you try running `Worms20_MasterDo.do` right now, you will run into an error with `esttab`, saying that your output `.tex` file cannot be found (error code `r(603)`). The final fix is to …

3. Change file paths referenced in the command `esttab`
    - `esttab` is a function that comes from the package `estout`. It takes the analysis you have run and outputs them in table form into a document
      - For whatever reason, it does not like when you give the absolute file path of the document you would like it to output to. For example, on line 369 of `Earnings_consumption_hhearn_main_byage.do`, we see the command `esttab using "$output/KLPS4_E+_earnings_consumption_main_byage.tex", append`
      - The `$output` in the file path is a reference to the global variable (?) `output` (defined on line 27 of `Worms20_MasterDo.do`), which is the string `"$dir/output"`. `dir` in turn is the global directory you specified earlier
      - So in my file, `"$output/KLPS4_E+_earnings_consumption_main_byage.tex"` is read as `"\\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker/output/KLPS4_E+_earnings_consumption_main_byage.tex"` (the alternation between `\` and `/` has no effect)
    - `esttab` will not find your `.tex` file with this absolute file path! You will have to change it to a relative file path, by removing the `$`, to get `esttab using "output/KLPS4_E+_earnings_consumption_main_byage.tex", append`
      - This works because Stata has set its working directory to your global directory. The command will now look in the `output` folder in your working directory for your `.tex` file, successfully find it, and output your analysis into it
    - … you have to remove the `$` in every single instance of `esttab using` in every single `.do` file. This process sucks.
      - Note: you **only** have to do this each time you find `esttab using`! Other uses of `esttab` don't output into a document, and thus don't throw an error
    - Additionally, in three `.do` files in the `appendix` folder (`Earnings_consump_parentsedu_long.do`, `Three_panel_main_outcomes.do`, and `Threepanel_earn_consump_5yr_agebuckets_long.do`), `esttab`'s file path will contain `$table` instead of `$output`. `table` references the same directory `output` does, so you should replace each instance of `$table` with `output`
    - If you try running `Worms20_MasterDo.do` right now, everything will work!!

The runtime is around 10 minutes. Enjoy the rest of your reproduction!

P.S. To all Stata users, present and future, please make the right choice and use R instead. Thank you :)



## old, please ignore

- change global directory to `\\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker`
- remove `$` from every filepath within an `esttab using` command
  - for 3 files, replace `$table` with `output`
- in Stata command line:
  - enter `sysdir set PLUS \\Client\C:\Users\myzha\Documents\Stata\ado`
  - enter `sysdir set PERSONAL \\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker\ado`
  - in `C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker\ado`, create a folder `f` and place `fdr_adjustment.do` inside
  - also need to enter `ssc install texdoc, replace`

## temporary reference

- fdr_sharpened_qvalues.do is actually fdr_adjustment.ado ?
- readme, code files 1C, fix name of `Worms20_master_paper_appendix.do`

https://stackoverflow.com/questions/43287524/stata-ado-package-not-found

https://www.statalist.org/forums/forum/general-stata-discussion/general/1299948-stata-won-t-change-content-directory

https://www.statalist.org/forums/forum/general-stata-discussion/general/1542570-stata-does-not-find-the-location-of-an-ado-file

https://www.statalist.org/forums/forum/general-stata-discussion/general/1468243-cannot-write-in-directory-c-ado-plus-o

https://kb.iu.edu/d/arur

https://www.stata.com/manuals/psysdir.pdf

https://guides.lib.berkeley.edu/citrix/stata

https://www.eui.eu/ServicesAndAdmin/ComputingService/KnownIssues/CitrixStataCannotInstallPackage

https://www.statalist.org/forums/forum/general-stata-discussion/general/1588097-estout-returning-file-could-not-be-opened-error-except-for-tex-files

https://www.statalist.org/forums/forum/general-stata-discussion/general/1315088-r-603-error-can-save-file-help
