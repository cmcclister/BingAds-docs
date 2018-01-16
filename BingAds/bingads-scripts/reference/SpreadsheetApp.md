# SpreadsheetApp
This class allows opening and creating spreadsheets on OneDrive.

|Method|Return Type|Description|
|-|-|-
create(String name)|[Spreadsheet](./Spreadsheet)|Creates a new spreadsheet using the specified name.<br />
create(String name, long rows, long columns)|[Spreadsheet](./Spreadsheet)|Creates a new spreadsheet using the specified name and the provided number of rows and columns.<br />
getActive|[Spreadsheet](./Spreadsheet)|Returns the spreadsheet that is currently active, or null if none is active.<br />
getActiveSpreadsheet|[Spreadsheet](./Spreadsheet)|Returns the spreadsheet that is currently active, or null if none is active.<br />
newDataValidation|[DataValidationBuilder](./DataValidationBuilder)|Creates a builder for constructing data validation rules.<br />
open(File file)|[Spreadsheet](./Spreadsheet)|Returns the spreadsheet object which corresponds to the specified File object.<br />
openById(String id)|[Spreadsheet](./Spreadsheet)|Returns the spreadsheet which has the given ID.<br />
openByUrl(String url)|[Spreadsheet](./Spreadsheet)|Returns the spreadsheet located at the given url.<br />
