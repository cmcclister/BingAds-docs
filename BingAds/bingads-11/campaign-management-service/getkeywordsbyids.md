---
title: GetKeywordsByIds Service Operation - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Retrieves the specified keywords.
dev_langs: 
  - csharp
  - java
  - php
  - python
---
# GetKeywordsByIds Service Operation - Campaign Management
Retrieves the specified keywords.

## <a name="request"></a>Request Elements
The *GetKeywordsByIdsRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="adgroupid"></a>AdGroupId|The identifier of the ad group whose keywords you want to get.|**long**|
|<a name="keywordids"></a>KeywordIds|A maximum of 1,000 identifiers of the keywords to get.|**long** array|
|<a name="returnadditionalfields"></a>ReturnAdditionalFields|The list of additional properties that you want included within each returned [Keyword](keyword.md) object. This set of flags enables you to get the latest features using the current version of Bing Ads Campaign Management API, and in the next version the corresponding elements will be included by default.|[KeywordAdditionalField](keywordadditionalfield.md)|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *GetKeywordsByIdsResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="keywords"></a>Keywords|An array of [Keyword](keyword.md) objects that corresponds directly to the keyword identifiers that you specified in the request. Items of the list may be returned as null. For each list index where a keyword was not retrieved, the corresponding element will be null.|[Keyword](keyword.md) array|
|<a name="partialerrors"></a>PartialErrors|An array of [BatchError](batcherror.md) objects that contain details for any request items that were not successful.<br /><br />The list of errors do not correspond directly to the list of items in the request. The list can be empty if there were no errors, or can include one or more error objects corresponding to each unsuccessful list item in the request.|[BatchError](batcherror.md) array|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
The following template shows the order of the [body](#request-body) and [header](#request-header) elements for the SOAP request.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/CampaignManagement/v11">
    <Action mustUnderstand="1">GetKeywordsByIds</Action>
    <ApplicationToken i:nil="false">ValueHere</ApplicationToken>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <CustomerAccountId i:nil="false">ValueHere</CustomerAccountId>
    <CustomerId i:nil="false">ValueHere</CustomerId>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
    <Password i:nil="false">ValueHere</Password>
    <UserName i:nil="false">ValueHere</UserName>
  </s:Header>
  <s:Body>
    <GetKeywordsByIdsRequest xmlns="https://bingads.microsoft.com/CampaignManagement/v11">
      <AdGroupId>ValueHere</AdGroupId>
      <KeywordIds i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
        <a1:long>ValueHere</a1:long>
      </KeywordIds>
      <ReturnAdditionalFields i:nil="false">ValueHere</ReturnAdditionalFields>
    </GetKeywordsByIdsRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
The following template shows the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/CampaignManagement/v11">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <GetKeywordsByIdsResponse xmlns="https://bingads.microsoft.com/CampaignManagement/v11">
      <Keywords d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <Keyword>
          <Bid d4p1:nil="false">
            <Amount d4p1:nil="false">ValueHere</Amount>
          </Bid>
          <BiddingScheme d4p1:nil="false" d4p1:type="-- derived type specified here with the appropriate prefix --">
            <Type d4p1:nil="false">ValueHere</Type>
            <!--This field is applicable if the derived type attribute is set to MaxClicksBiddingScheme-->
            <MaxCpc d4p1:nil="false">
              <Amount d4p1:nil="false">ValueHere</Amount>
            </MaxCpc>
            <!--This field is applicable if the derived type attribute is set to MaxConversionsBiddingScheme-->
            <MaxCpc d4p1:nil="false">
              <Amount d4p1:nil="false">ValueHere</Amount>
            </MaxCpc>
            <!--These fields are applicable if the derived type attribute is set to TargetCpaBiddingScheme-->
            <MaxCpc d4p1:nil="false">
              <Amount d4p1:nil="false">ValueHere</Amount>
            </MaxCpc>
            <TargetCpa d4p1:nil="false">ValueHere</TargetCpa>
            <!--No additional fields are applicable if the derived type attribute is set to ManualCpcBiddingScheme-->
            <!--No additional fields are applicable if the derived type attribute is set to EnhancedCpcBiddingScheme-->
            <!--This field is applicable if the derived type attribute is set to InheritFromParentBiddingScheme-->
            <InheritedBidStrategyType d4p1:nil="false">ValueHere</InheritedBidStrategyType>
          </BiddingScheme>
          <DestinationUrl d4p1:nil="false">ValueHere</DestinationUrl>
          <EditorialStatus d4p1:nil="false">ValueHere</EditorialStatus>
          <FinalAppUrls xmlns:e241="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V11" d4p1:nil="false">
            <e241:AppUrl>
              <e241:OsType d4p1:nil="false">ValueHere</e241:OsType>
              <e241:Url d4p1:nil="false">ValueHere</e241:Url>
            </e241:AppUrl>
          </FinalAppUrls>
          <FinalMobileUrls d4p1:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalMobileUrls>
          <FinalUrls d4p1:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalUrls>
          <ForwardCompatibilityMap xmlns:e242="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
            <e242:KeyValuePairOfstringstring>
              <e242:key d4p1:nil="false">ValueHere</e242:key>
              <e242:value d4p1:nil="false">ValueHere</e242:value>
            </e242:KeyValuePairOfstringstring>
          </ForwardCompatibilityMap>
          <Id d4p1:nil="false">ValueHere</Id>
          <MatchType d4p1:nil="false">ValueHere</MatchType>
          <Param1 d4p1:nil="false">ValueHere</Param1>
          <Param2 d4p1:nil="false">ValueHere</Param2>
          <Param3 d4p1:nil="false">ValueHere</Param3>
          <Status d4p1:nil="false">ValueHere</Status>
          <Text d4p1:nil="false">ValueHere</Text>
          <TrackingUrlTemplate d4p1:nil="false">ValueHere</TrackingUrlTemplate>
          <UrlCustomParameters xmlns:e243="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V11" d4p1:nil="false">
            <e243:Parameters d4p1:nil="false">
              <e243:CustomParameter>
                <e243:Key d4p1:nil="false">ValueHere</e243:Key>
                <e243:Value d4p1:nil="false">ValueHere</e243:Value>
              </e243:CustomParameter>
            </e243:Parameters>
          </UrlCustomParameters>
        </Keyword>
      </Keywords>
      <PartialErrors d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <BatchError d4p1:type="-- derived type specified here with the appropriate prefix --">
          <Code>ValueHere</Code>
          <Details d4p1:nil="false">ValueHere</Details>
          <ErrorCode d4p1:nil="false">ValueHere</ErrorCode>
          <FieldPath d4p1:nil="false">ValueHere</FieldPath>
          <ForwardCompatibilityMap xmlns:e244="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
            <e244:KeyValuePairOfstringstring>
              <e244:key d4p1:nil="false">ValueHere</e244:key>
              <e244:value d4p1:nil="false">ValueHere</e244:value>
            </e244:KeyValuePairOfstringstring>
          </ForwardCompatibilityMap>
          <Index>ValueHere</Index>
          <Message d4p1:nil="false">ValueHere</Message>
          <Type d4p1:nil="false">ValueHere</Type>
          <!--These fields are applicable if the derived type attribute is set to EditorialError-->
          <Appealable d4p1:nil="false">ValueHere</Appealable>
          <DisapprovedText d4p1:nil="false">ValueHere</DisapprovedText>
          <Location d4p1:nil="false">ValueHere</Location>
          <PublisherCountry d4p1:nil="false">ValueHere</PublisherCountry>
          <ReasonCode>ValueHere</ReasonCode>
        </BatchError>
      </PartialErrors>
    </GetKeywordsByIdsResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<GetKeywordsByIdsResponse> GetKeywordsByIdsAsync(
	long adGroupId,
	IList<long> keywordIds,
	KeywordAdditionalField? returnAdditionalFields)
{
	var request = new GetKeywordsByIdsRequest
	{
		AdGroupId = adGroupId,
		KeywordIds = keywordIds,
		ReturnAdditionalFields = returnAdditionalFields
	};

	return (await CampaignManagementService.CallAsync((s, r) => s.GetKeywordsByIdsAsync(r), request));
}
```
```java
static GetKeywordsByIdsResponse getKeywordsByIds(
	java.lang.Long adGroupId,
	ArrayOflong keywordIds,
	ArrayList<KeywordAdditionalField> returnAdditionalFields) throws RemoteException, Exception
{
	GetKeywordsByIdsRequest request = new GetKeywordsByIdsRequest();

	request.setAdGroupId(adGroupId);
	request.setKeywordIds(keywordIds);
	request.setReturnAdditionalFields(returnAdditionalFields);

	return CampaignManagementService.getService().getKeywordsByIds(request);
}
```
```php
static function GetKeywordsByIds(
	$adGroupId,
	$keywordIds,
	$returnAdditionalFields)
{

	$GLOBALS['Proxy'] = $GLOBALS['CampaignManagementProxy'];

	$request = new GetKeywordsByIdsRequest();

	$request->AdGroupId = $adGroupId;
	$request->KeywordIds = $keywordIds;
	$request->ReturnAdditionalFields = $returnAdditionalFields;

	return $GLOBALS['CampaignManagementProxy']->GetService()->GetKeywordsByIds($request);
}
```
```python
response=campaignmanagement_service.GetKeywordsByIds(
	AdGroupId=AdGroupId,
	KeywordIds=KeywordIds,
	ReturnAdditionalFields=ReturnAdditionalFields)
```

## Requirements
Service: [CampaignManagementService.svc v11](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v11/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v11  

