# Spreadsheet
This class represents a spreadsheet.

|Method|Return Type|Description|
|-|-|-
addEditor(String emailAddress)|[Sheet](./Sheet)|Adds the specified user (email address) to the list of editors of this spreadsheet.<br />
addEditors(String[] emailAddresses)|Array|Adds the specified array of users (email addresses) to the list of editors of this spreadsheet.<br />
copy(String name)|[Spreadsheet](./Spreadsheet)|Copies the contents of this spreadsheet into a new spreadsheet and returns it.<br />
deleteSheet(Sheet sheet)|[Sheet](./Sheet)|Deletes the current sheet from this spreadsheet and returns the new active sheet.<br />
duplicateActiveSheet|[Sheet](./Sheet)|Creates a copy of the active sheet, makes it the active sheet and returns it.<br />
getActiveSheet|[Sheet](./Sheet)|Returns the active sheet in this spreadsheet.<br />
getId|String|Returns the unique ID for this spreadsheet.<br />
getName|String|Returns the name of this spreadsheet.<br />
getRange(String a1Notation)|[Range](./Range)|Returns the range as indicated by the given A1 or R1C1 notation.<br />
getRangeByName(String name)|[Range](./Range)|Returns the named range which matches the provided name, or null if no match is found. If multiple sheets use the same range names, use the sheet name in addition to the range name. For example, 'Sheet1!ProductList' where Sheet1 is the name of the sheet and ProductList is the name of the range.  <br />
getSheetByName(String name)|[Sheet](./Sheet)|Returns a <br />
getSheets|[Sheet[]](./Sheet)|Returns all the sheets in this spreadsheet.<br />
getSpreadsheetTimeZone|String|Returns the time zone of this spreadsheet in “long” format (for example, "America/Los_Angeles"/ See [joda.org](http://joda-time.sourceforge.net/timezones.html) for more examples.<br />
getUrl|String|Returns the URL where this spreadsheet is located.<br />
insertSheet|[Sheet](./Sheet)|Inserts a new sheet in this spreadsheet using the default name and makes it the active sheet.<br />
moveActiveSheet(long pos)|void|Moves the active sheet to the specified position (index) in the list of sheets contained by this spreadsheet.<br />
setActiveSheet(Sheet sheet)|[Sheet](./Sheet)|Sets the specified sheet as the active sheet in this spreadsheet.<br />
setSpreadsheetTimeZone|void|Sets the specified time zone for this spreadsheet.<br />
