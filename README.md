# reprod-hamory-miguel-walker
A revised reproduction package for 'Twenty-year economic impacts of deworming' by Joan Hamory, Edward Miguel, Michael Walker, Michael Kremer, and Sarah Baird (2021)

This reproduction attempt was documented on the [Social Science Reproduction Platform](https://www.socialsciencereproduction.org/). The link to this reproduction can be found [here](https://www.socialsciencereproduction.org/reproductions/0d5ad5d3-5a6e-40f0-96c4-56f377588d7b/index). A reproduction tree can be found below:

```
output placeholder 1
└── Worms20_MasterDo.do
    └── input placeholder 1
output placeholder 2
└── Worms20_Globals.do
    └── input placeholder 2
output placeholder 3
└── Worms20_master_main.do
    └── input placeholder 3
output placeholder 4
└── Worms20_master_paper_appendix.do
    └── input placeholder 4
output placeholder 5
└── Worms20_intext_calc.do
    └── input placeholder 5
KLPS4_E+_earnings_consumption_main_byage.tex (Table 1)
└── Earnings_consumption_hhearn_main_byage.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_earnings_labor_occchoice_main_byage.tex (Table 2)
└── Earnings_wealth_labor_occchoice_main_byage.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_KD_fullsample.eps (Figure 1)
└── Consumption_earnings_KD.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_consumption_graph.eps (Figure S3 A)
└── Consumption_graph.R
    └── Consumption_results_for_R.xlsx
        └── Consumption_gender_results_for_R.do
            └── Worms20_Analysis.dta
                └── MISSING CLEANING MAIN
                    ├── KLPS-2
                    ├── KLPS-3
                    └── KLPS-4
KLPS4_earnings_graph.eps (Figure S3 B)
└── Earnings_graph.R
    └── Earnings_results_for_R.xlsx
        └── Earnings_gender_results_for_R.do
            └── Worms20_Analysis.dta
                └── MISSING CLEANING MAIN
                    ├── KLPS-2
                    ├── KLPS-3
                    └── KLPS-4
ConsumptionTreatEffect_YearsTreat.eps (Figure S4)
└── Consumption_yearstreat_figure.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_Attrition_main.tex (Table S1)
└── Attrition_main.do
    └── Worms20_Attrition.dta
        └── MISSING CLEANING ATTRITION
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_Attrition_olderyounger.tex (Table S2)
└── Attrition_byage.do
    └── Worms20_Attrition.dta
        └── MISSING CLEANING ATTRITION
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_earnings_consumption_main_byage_klps4.tex (Table S3)
└── Earnings_consumption_hhearn_main_byage_klps4.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_earnings_labor_occchoice_main_byage_klps4.tex (Table S4)
└── Earnings_wealth_labor_occchoice_main_byage_klps4.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_earnings_consumption_main_byage_scyvoced.tex (Table S5)
└── Earnings_consumption_hhearn_main_byage_scyvoced.do
    ├── Worms20_Analysis.dta
    │   └── MISSING CLEANING MAIN
    │       ├── KLPS-2
    │       ├── KLPS-3
    │       └── KLPS-4
    └── Worms20_Analysis_scyvoced.dta
        └── MISSING CLEANING SCYVOCED
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_earnings_labor_occchoice_main_byage_scyvoced.tex (Table S6)
└── Earnings_wealth_labor_occchoice_main_byage_scyvoced.do
    ├── Worms20_Analysis.dta
    │   └── MISSING CLEANING MAIN
    │       ├── KLPS-2
    │       ├── KLPS-3
    │       └── KLPS-4
    └── Worms20_Analysis_scyvoced.dta
        └── MISSING CLEANING SCYVOCED
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_pooled_outcomes_extended.tex (Table S7)
└── Three_panel_main_outcomes.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_pooled_earnings_consumption_parentsedu_long.tex (Table S8)
└── Earnings_consump_parentsedu_long.do
    ├── Worms20_Heterogeneity.dta
    │   └── MISSING CLEANING HETEROGENEITY
    │       ├── KLPS-2
    │       ├── KLPS-3
    │       └── KLPS-4
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_pooled_earnings_consumption_5yr_agebuckets_long.tex (Table S9)
└── Threepanel_earn_consump_5yr_agebuckets_long.do
    └── Worms20_Analysis.dta
        └── MISSING CLEANING MAIN
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_heterogeneity_summarystats.tex (Table S10)
└── Heterogeneity_summarystats.do
    ├── Worms20_Heterogeneity.dta
    │   └── MISSING CLEANING HETEROGENEITY
    │       ├── KLPS-2
    │       ├── KLPS-3
    │       └── KLPS-4
    └── Worm_Infection_Panel.dta
        └── MISSING CLEANING INFECTION
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
KLPS4_E+_heterogeneity_treateffects.tex (Table S11)
└── Heterogeneity_treateffects.do
    ├── Worms20_Heterogeneity.dta
    │   └── MISSING CLEANING HETEROGENEITY
    │       ├── KLPS-2
    │       ├── KLPS-3
    │       └── KLPS-4
    └── Worm_Infection_Panel.dta
        └── MISSING CLEANING INFECTION
            ├── KLPS-2
            ├── KLPS-3
            └── KLPS-4
Cost_benefit_table_pooled.tex (Table S12)
└── Cost_benefit_table_pooled.Rmd
    └── input placeholder 6
KLPS4_cost_benefit_pooled.eps (Figure 2)
└── Cost_benefit_pooled.R
    └── input placeholder 7
```

A guide to reproducing 'Twenty-year economic impacts of deworming' for users who access Stata through Citrix can be found below:

#### To make `Worms20_MasterDo.do` run (using Citrix):

Starting from a fresh download of the [reproduction package](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/TTYMHI) for ['Twenty-year economic impacts of deworming'](https://www.pnas.org/content/118/14/e2023185118):

1. Open Stata via Citrix, and open `Worms20_MasterDo.do`
    - As instructed in `Twenty Year Impacts of Deworming - Data Replication_README.pdf`, change the global directory on line 13 to the folder containing your reproduction files, and add `\\Client` to the beginning
      - For example, if my reproduction files/folders (e.g. `do`, `data`, `ado`, and so on) are located at `C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker`, then I would change the directory on line 13 to be `\\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker`
      - This is because `\Client`, rather than `C:`, is the root directory for a user accessing Stata via Citrix. The additional backslash `\` is used to escape the backslash in the name of the root directory, so that Stata reads the file path correctly
    - If you try running `Worms20_MasterDo.do` right now, you will run into an error saying that some file already exists (error code `r(602)`). To fix this, we need to …

2. Set the location where `.ado` files will be installed
    - UC Berkeley provides a [guide](https://guides.lib.berkeley.edu/citrix/stata) to installing `.ado` files for Citrix users. Despite much testing, I could not get Stata to successfully install and/or recognize the required `.ado` files following Berkeley's guide
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
