# EmbeddedChart
Represents an embedded chart in a spreadsheet.

|Method|Return Type|Description|
|-|-|-
getContainerInfo|[ContainerInfo](./ContainerInfo)|Returns information on the position of this chart within a sheet.<br />
getOptions|[ChartOptions](./ChartOptions)|Returns the options for this chart specified when it was constructed.<br />
getRanges|[Range[]](./Range)|Returns the cell ranges that this chart uses as a data source.<br />
modify|[EmbeddedChartBuilder](./EmbeddedChartBuilder)|Returns an EmbeddedChartBuilder that can be used to modify this chart.<br />
