# BingAdsAccount
Represents an account in the Bing Ads system.       

|Method|Return Type|Description|
|-|-|-
applyLabel(String name)|void|Applies an account label to this account<br />
getCurrencyCode|String|Returns the currency code of the account in descriptive format, as defined in the list here.<br />
getCustomerId|String|Returns the customer ID of this account.<br />
getEntityType|String|Returns the type of this account as a String, which is, Account.
getName|String|Returns the name of this account.<br />
getStatsFor|[BingAdsAccountStats](./BingAdsAccountStats)|Returns the account stats for the provided date range.<br />
getStatsFor|[BingAdsAccountStats](./BingAdsAccountStats)|Returns the account stats for the provided custom date range.
getTimeZone|String|Returns the POSIX time zone of this account.<br />
labels|[AccountLabelSelector](./AccountLabelSelector)|Returns the labels associated with this account.                      <br />
