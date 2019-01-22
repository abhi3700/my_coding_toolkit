* ### UNC
  What is a UNC path?

  Short for Universal Naming Convention or Uniform Naming Convention, it is a PC format for specifying the location of resources on a local-area network (LAN). UNC uses the following format: <br/>
  `\\server-name\shared-resource-pathname` <br/>
  So, for example, to access the file test.txt in the directory EXAMPLES on the shared server SILO, you would write:<br/>
  `\\SILO\EXAMPLES\test.txt`
* ### Server file path in code
  Use this - `\\\\vmfg\folder1\folder2\file.ext` <br/>
  E.g. - <br/>
  ```python
  excel_file = pd.ExcelFile("\\\\vmfg\\VFD FILE SERVER\\SECTIONS\\DRY ETCH\\QC Log Book\\Final QC Log Book\\ASH_09_10_LOG_BOOK\\ASH09_QC_LOG_BOOK\\ASH09_QC_LOG_BOOK.xlsm")
  ```
