['Twenty-year economic impacts of deworming'](https://www.pnas.org/content/118/14/e2023185118)

[replication data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/TTYMHI)

## To make `Worms20_MasterDo.do` run (using Citrix):

- change global directory to `\\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker`
- in Stata command line:
  - enter `sysdir set PLUS \\Client\C:\Users\myzha\Documents\Stata\ado\`
  - enter `sysdir set PERSONAL \\Client\C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker\ado`
  - in `C:\Users\myzha\Documents\GitHub\reprod-hamory-miguel-walker\ado`, create a folder `f` and place `fdr_adjustment.do` inside
  - also need to enter `ssc install texdoc, replace`

## temporary reference

- any time `esttab` function is used, change filepath to be relative rather than absolute
- fdr_sharpened_qvalues.do is actually fdr_adjustment.do ?
- readme, code files 1C, fixed name of `Worms20_master_paper_appendix.do`
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
