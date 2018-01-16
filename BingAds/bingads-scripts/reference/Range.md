# Range
This class represents a range of cells in a worksheet.

|Method|Return Type|Description|
|-|-|-
clear|[Range](./Range)|Clears all content, formatting and data validation rules from this range.<br />
clearContent|[Range](./Range)|Clears all content from this range, but retains the formatting information.<br />
clearFormat|[Range](./Range)|Clears all formatting information from this range.<br />
copyFormatToRange(longgridId, long column, long columnEnd, long row, long rowEnd)|void|Copies the formatting information from this range to the specified target range in the spreadsheet indicated by the provided ID.<br />
copyFormatToRange|void|Copies the formatting information from this range to the specified target range in the given spreadsheet.<br />
copyTo(Range destination)|void|Copies content and formatting information from this range to the target range.<br />
getCell(long row, long column)|Range|Returns the cell indicated by the specified row and column from this range.<br />
getColumn|long|Returns the starting column position for this range.<br />
getDataValidations|[DataValidation[][]](./DataValidation)|Returns an array containing the data validation rules applicable to this range.<br />
getFormula|String|Returns the formula (in A1 notation), if defined, for the top-left cell of this range.<br />
getLastRow|long|Returns the position of the last row of this range.<br />
getNumColumns|long|Returns the number of columns in this range.<br />
getNumRows|long|Returns the number of rows in this range.<br />
getRow|long|Returns the position of the row for this range.<br />
getSheet|Sheet|Returns the sheet containing this range.<br />
getValue|Object|Returns the value contained by the top-left cell in this range.<br />
getValues|Object[][]|Returns a two-dimensional array of values contained by this range, beginning with the top-left cell.<br />
isBlank|boolean|Returns <br />
mergeAcross|[Range](./Range)|Merges the cells across the columns in this range and returns the range with the merged cells.<br />
moveTo(Range target)|void|Moves (cut and paste) the content and formatting information from this range to the target range.<br />
offset(long rowOffset, long columnOffset)|[Range](./Range)|Returns a new range starting at row and column positions offset from this range by the specified increments. The values for the offset can be negative to effect an offset in the opposite direction.<br />
setBackground(String color)|[Range](./Range)|Sets the background color of the cells in this range to the specified color. The color is in the CSS format (for example, '#0000ff' or 'blue'). Specifying null resets the color.<br />
setBorder(boolean top, boolean left, boolean bottom, boolean right, boolean vertical, boolean horizontal)|[Range](./Range)|Turns on the border for all cells in this range in the directions specified by the given boolean values. <br />
setDataValidation|[Range](./Range)|Sets the specified data validation rule on all cells in this range.<br />
setDataValidations|[Range](./Range)|Sets the specified data validation rules to the cells in this range, assigning each rule to the cell based on matching row and column positions. The dimensions of the input rule array must match the dimensions of this range.<br />
setFontColor(String color)|[Range](./Range)|Sets the specified font color to the cells in this range. The color must be in CSS notation (for example '0000ff' or 'blue').<br />
setFontFamily(String fontFamily)|[Range](./Range)|Sets the font family for cells in this range. Example values include 'Tahoma' or 'Verdana'.<br />
setFontSize(long size)|[Range](./Range)|Sets the specified point size to use for fonts on all the cells in this range.<br />
setFontWeight(String fontWeight)|[Range](./Range)|Sets the specified point weight to use for fonts on all the cells in this range. Valid values include 'normal' and 'bold'.<br />
setFormula(String formula)|[Range](./Range)|Sets the formula on all cells in this range with the specified formula in A1 notation.<br />
setFormulas(String[][] formulas)|[Range](./Range)|Sets the specified formulas to the cells in this range, assigning each formula to the cell based on matching row and column positions. The dimensions of the input formula array must match the dimensions of this range and each formula must be in A1 notation.<br />
setFormulasR1C1|[Range](./Range)|Sets the specified formulas to the cells in this range, assigning each formula to the cell based on matching row and column positions. The dimensions of the input formula array must match the dimensions of this range and each formula must be in R1C1 notation.<br />
setHorizontalAlignment(String alignment)|[Range](./Range)|Sets the horizontal alignment of content in the cells in this range. Valid values include 'left', 'center' or 'normal'.<br />
setNumberFormat(String numberFormat)|[Range](./Range)|Sets the number format of the cells in this range to the specified format string.<br />
setNumberFormats|[Range](./Range)|Sets the specified format strings to the cells in this range, assigning each format string to the cell based on matching row and column positions. The dimensions of the input format string array must match the dimensions of this range.<br />
setValue(Object value)|[Range](./Range)|Sets the value to all cells in this range.<br />
setValues(Object[][] values)|[Range](./Range)|Sets the specified values to the cells in this range, assigning each value to the cell based on matching row and column positions. The dimensions of the input value array must match the dimensions of this range.<br />
setVerticalAlignment|[Range](./Range)|Sets the vertical alignment of content in the cells in this range. Valid values include 'top', 'middle' or 'bottom'.<br />
setWraps(Object[][] isWrapEnabled)|[Range](./Range)|Sets the specified boolean flags to the wrap property of the cells in this range, assigning each boolean value to the cell based on matching row and column positions. The dimensions of the input boolean array must match the dimensions of this range.<br />
sort(Object sortSpecObj)|[Range](./Range)|Sorts the columns in this range based on the specified sort object.<br />
