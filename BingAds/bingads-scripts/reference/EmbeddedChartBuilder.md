# EmbeddedChartBuilder
Provides methods for building an embedded chart in a spreadsheet.

|Method|Return Type|Description|
|-|-|-
addRange(Range range)|[EmbeddedChartBuilder](./EmbeddedChartBuilder)|Adds the specified <br />
build|[EmbeddedChart](./EmbeddedChart)|Builds and returns the chart defined by this builder.<br />
removeRange(Range range)|[EmbeddedChartBuilder](./EmbeddedChartBuilder)|Removes the given Range from the chart defined by this builder. <br />
setChartType(ChartType type)|[EmbeddedChartBuilder](./EmbeddedChartBuilder)|Sets the given chart type for the chart defined by this builder.<br />
setOption(String option, Object value)|[EmbeddedChartBuilder](./EmbeddedChartBuilder)|Sets the specified options for the chart defined by this builder.<br />
setPosition(long anchorRowPos, long anchorColPos, long offsetX, long offsetY)|[EmbeddedChartBuilder](./EmbeddedChartBuilder)|Sets the position where the chart displays on the containing sheet.<br />
