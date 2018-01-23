# Ad
Represents an ad in the Bing Ads system.

|Method|Return Type|Description|
|-|-|-
[asType]('#asType')|[AdViewSpace](./AdViewSpace)|Returns an AdViewSpace object, which provides access to properties specific to the type of this ad.<br />
[enable]('#enable')|void|Enables the ad.<br />
[getAdGroup]('#getAdGroup')|[AdGroup](./AdGroup)|Returns the parent ad group of this ad.<br />
[getApprovalStatus]('#getApprovalStatus')|String|Returns the approval status of this ad. Supported values include:<br /> <br /> `APPROVED`,<br /> `DISAPPROVED`<br /><br />
[getCampaign]('#getCampaign')|[Campaign](./Campaign)|Returns the parent campaign of this ad.<br />
[getDisapprovalReasons]('#getDisapprovalReasons')|String[]|Returns an array containing the reasons for which this ad was disapproved. If it is not disapproved, the array will be empty.<br />
[getDisplayUrl]('#getDisplayUrl')|String|Returns the display URL of this ad. This value could be null for some types of ads.<br />
[getEntityType]('#getEntityType')|String|Returns the type of entity of this ad, which is “Ad”.<br />
[getHeadline]('#getHeadline')|String|Returns the headline (title) of this ad. This value could be null for some types of ads.<br />
[getId]('#getId')|long|Returns the ID of this ad. In order to specify a unique ID for an ad, both its ad group ID and this ID must be specified.<br />
[getStatsFor(String dateRange)]('#getStatsFor-String-dateRange)')|String|Returns stats for this ad for the given date range. Supported values include:<br /> <br /> `TODAY`,<br /> `YESTERDAY`,<br /> `LAST_7_DAYS`,<br /> `THIS_WEEK_SUN_TODAY`,<br /> `LAST_14_DAYS`,<br /> `LAST_30_DAYS`,<br /> `LAST_WEEK_SUN_SAT`,<br /> `THIS_MONTH`,<br /> `LAST_MONTH`,<br /> `ALL_TIME`<br /><br />
[getStatsFor(Object dateFrom, Object dateTo)]('#getStatsFor-Object-dateFrom_ Object dateTo)')|String|Returns stats for this ad for the given custom date range. Both parameters can be either a string in YYYYMMDD format or an object with year, month and day properties. In either case, a full date must be specified <br />
[getType]('#getType')|String|Returns the type of this ad. Supported values include: `EXPANDED_TEXT_AD` and `TEXT_AD`<br />
[isEnabled]('#isEnabled')|boolean|Returns true if this ad is enabled. <br />
[isMobilePreferred]('#isMobilePreferred')|boolean|Returns true if this ad indicates mobile device preference or false otherwise. <br />
[isPaused]('#isPaused')|boolean|Returns true if this ad is paused. <br />
[isType]('#isType')|[AdTypeSpace](./AdTypeSpace)|Returns an AdTypeSpace object which provides more information on the type of this ad. <br />
[pause]('#pause')|void|Pauses this ad.<br />
[remove]('#remove')|void|Removes this ad.<br />
[urls]('#urls')|[AdUrls](./AdUrls)|Returns an AdUrls object which provides access to the `URL` fields of this ad. <br />

<a name="asType"></a>
## asType
Returns an AdViewSpace object, which provides access to properties specific to the type of this ad.


<a name="enable"></a>
## enable
Enables the ad.


<a name="getAdGroup"></a>
## getAdGroup
Returns the parent ad group of this ad.


<a name="getApprovalStatus"></a>
## getApprovalStatus
Returns the approval status of this ad. Supported values include:<br /> <br /> `APPROVED`,<br /> `DISAPPROVED`<br />


<a name="getCampaign"></a>
## getCampaign
Returns the parent campaign of this ad.


<a name="getDisapprovalReasons"></a>
## getDisapprovalReasons
Returns an array containing the reasons for which this ad was disapproved. If it is not disapproved, the array will be empty.


<a name="getDisplayUrl"></a>
## getDisplayUrl
Returns the display URL of this ad. This value could be null for some types of ads.


<a name="getEntityType"></a>
## getEntityType
Returns the type of entity of this ad, which is “Ad”.


<a name="getHeadline"></a>
## getHeadline
Returns the headline (title) of this ad. This value could be null for some types of ads.


<a name="getId"></a>
## getId
Returns the ID of this ad. In order to specify a unique ID for an ad, both its ad group ID and this ID must be specified.


<a name="getStatsFor-String-dateRange)"></a>
## getStatsFor(String dateRange)
Returns stats for this ad for the given date range. Supported values include:<br /> <br /> `TODAY`,<br /> `YESTERDAY`,<br /> `LAST_7_DAYS`,<br /> `THIS_WEEK_SUN_TODAY`,<br /> `LAST_14_DAYS`,<br /> `LAST_30_DAYS`,<br /> `LAST_WEEK_SUN_SAT`,<br /> `THIS_MONTH`,<br /> `LAST_MONTH`,<br /> `ALL_TIME`<br />


<a name="getStatsFor-Object-dateFrom_ Object dateTo)"></a>
## getStatsFor(Object dateFrom, Object dateTo)
Returns stats for this ad for the given custom date range. Both parameters can be either a string in YYYYMMDD format or an object with year, month and day properties. In either case, a full date must be specified 


<a name="getType"></a>
## getType
Returns the type of this ad. Supported values include: `EXPANDED_TEXT_AD` and `TEXT_AD`


<a name="isEnabled"></a>
## isEnabled
Returns true if this ad is enabled. 


<a name="isMobilePreferred"></a>
## isMobilePreferred
Returns true if this ad indicates mobile device preference or false otherwise. 


<a name="isPaused"></a>
## isPaused
Returns true if this ad is paused. 


<a name="isType"></a>
## isType
Returns an AdTypeSpace object which provides more information on the type of this ad. 


<a name="pause"></a>
## pause
Pauses this ad.


<a name="remove"></a>
## remove
Removes this ad.


<a name="urls"></a>
## urls
Returns an AdUrls object which provides access to the `URL` fields of this ad. 

