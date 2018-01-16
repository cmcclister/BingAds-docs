# AccountLabelSelector
Provides methods to select account labels by using filtering and sorting.

|Method|Return Type|Description|
|-|-|-
get|[AccountLabelIterator](./AccountLabelIterator)|Returns an iterator indexing the account labels in this selector.<br />
withCondition(String condition)|[AccountLabelSelector](./AccountLabelSelector)|Returns a selector by specifying the filtering condition on the account labels in this selector.  The format for the condition string is “columnName operator value”, for e.g., “Name CONTAINS 'Contoso'”, where:<br /> <br /> •	columnName must be from the list of supported columns for ad groups (see table below).<br /> •	operator must be from the list of standard operators supported by Bing Ads Scripts.<br />  •	value is a value that falls within the accepted range of values for the data type of the column represented by columnName.<br /><br /><code>withCondition()</code> can be used multiple times in series to more precisely filter the accounts.<br />
withIds(long[] ids)|[AccountLabelSelector](./AccountLabelSelector)|Returns a selector by specifying the list of IDs to filter account labels in this selector. The input argument can accept a  maximum of 10,000 IDs. If any more IDs are provided, any subsequent get() call on this selector will fail with an error.<br />
Supported columns for account label filtering. 

|
Name|String|withCondition(&quot;Name CONTAINS_IGNORE_CASE &#x27;new accounts&#x27;&quot;)|NA
