# Sheet
This class represents a worksheet within a spreadsheet.

|Method|Return Type|Description|
|-|-|-
activate|[Sheet](./Sheet)|Sets this sheet as active and returns the currently active sheet.<br />
appendRow(Object[] rowContents)|[Sheet](./Sheet)|Appends a new row to this sheet using the supplied values. This method is atomic in execution.<br />
autoResizeColumn(long columnPosition)|[Sheet](./Sheet)|Makes the given column wide enough to fit its contents.<br />
clear|[Sheet](./Sheet)|Clears the contents of this sheet as well as any formatting information.<br />
clearContents|[Sheet](./Sheet)|Clears the contents of this sheet but leaves the formatting information intact.<br />
clearFormats|[Sheet](./Sheet)|Clears the formatting information of this sheet but leaves the content intact.<br />
clearNotes|[Sheet](./Sheet)|Clears all notes from this sheet.<br />
copyTo(Spreadsheet spreadsheet)|[Sheet](./Sheet)|Copies the contents of this sheet to the given spreadsheet. The new sheet will be named “Copy of [original name]”<br />
deleteRows(long rowPosition, long howMany)|void|Deletes the specified number of rows in this sheet starting from the provided row index.<br />
getActiveRange|[Range](./Range)|Returns the active range for this sheet.<br />
getCharts|[EmbeddedChart[]](./EmbeddedChart)|Returns an array of charts contained within this sheet.<br />
getColumnWidth(long columnPosition)|long|Returns the width of the specified column in pixels.<br />
getDataRange|[Range](./Range)|Returns a range indicating the dimensions of the region in this sheet where all the data is present.<br />
getLastColumn|long|Returns the position (index) of the last column in this sheet that has content.<br />
getLastRow|long|Returns the position (index) of the last row in this sheet that has content.<br />
getMaxColumns|long|Returns the total number of columns in this sheet, including ones which do not have content.<br />
getMaxRows|long|Returns the total number of rows in this sheet, including ones which do not have content.<br />
getRange(long row, long column)|[Range](./Range)|Returns a range (cell) from this sheet specified by the given row and column positions.<br />
getRange(String a1Notation)|[Range](./Range)|Returns a range from this sheet specified by the given A1 or R1C1 notation.<br />
hideColumns(long columnIndex)|void|Hides the column at the specified position (index) in this sheet.<br />
insertChart|[EmbeddedChart](./EmbeddedChart)|Adds a new chart to this sheet and returns it.<br />
insertColumnAfter(long afterPosition)|[Sheet](./Sheet)|Inserts a new column after the specified column position in this sheet.<br />
insertColumnsAfter(long afterPosition, long howMany)|[Sheet](./Sheet)|Inserts the specified number of new columns after the given column position in this sheet.<br />
insertImage(Blob blob, long column, long row)|void|Inserts the image contained in the specified Blob at the specified row and column positions<br />
insertRows(long rowIndex)|[Sheet](./Sheet)|Inserts a new row at the specified row position in the sheet.<br />
insertRowsAfter(long rowIndex, long howMany)|[Sheet](./Sheet)|Inserts the specified number of new rows after the given row position in this sheet.<br />
newChart|[EmbeddedChartBuilder](./EmbeddedChartBuilder)|Creates a new chart builder object and returns it.<br />
removeChart|void|Removes the given chart from this sheet.<br />
setColumnWidth(long columnPosition, long width)|[Sheet](./Sheet)|Sets the width of the column at the specified position in this sheet to the provided width value.<br />
setFrozenColumns(long columns)|void|Freezes the specified number of columns in this sheet.<br />
setFrozenRows(long rows)|void|Freezes the specified number of rows in this sheet.<br />
setName(String name)|[Sheet](./Sheet)|Sets the name of this sheet.<br />
setRowHeight(long rowPosition, long height)|[Sheet](./Sheet)|Sets the height of the row at the specified position in this sheet to the provided height value.<br />
sort(long columnPosition)|[Sheet](./Sheet)|Sorts this sheet by column in ascending order.<br />
