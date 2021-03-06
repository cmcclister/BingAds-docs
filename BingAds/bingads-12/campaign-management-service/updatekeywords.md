---
title: UpdateKeywords Service Operation - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Updates the keywords within a specified ad group.
dev_langs: 
  - csharp
  - java
  - php
  - python
---
> [!IMPORTANT]
> This Bing Ads API Version 12 preview documentation is subject to change. To return to version 11 content, use the version selector near the table of contents at the top and left side of the page.

# UpdateKeywords Service Operation - Campaign Management
Updates the keywords within a specified ad group.

## <a name="request"></a>Request Elements
The *UpdateKeywordsRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="adgroupid"></a>AdGroupId|The identifier of the ad group whose keywords will be updated.|**long**|
|<a name="keywords"></a>Keywords|An array of [Keyword](keyword.md) objects that contains the updated keyword information. The *Id* element of each of these objects identifies the keyword to update.<br /><br />This array can contain a maximum of 1,000 elements.|[Keyword](keyword.md) array|
|<a name="returninheritedbidstrategytypes"></a>ReturnInheritedBidStrategyTypes|Determines whether or not the service should return the bid strategy type that is inherited from the parent campaign or ad group.<br/><br/>The default value is false, and the [InheritedBidStrategyTypes](#inheritedbidstrategytypes) element will only be returned if you set this element true.|**boolean**|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *UpdateKeywordsResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="inheritedbidstrategytypes"></a>InheritedBidStrategyTypes|The value of each string represents the type of bidding scheme or bid strategy type that is inherited from the parent campaign or ad group.<br/><br/>Each string in the list is returned in the same order and corresponds to the keywords in the request message. If a keyword does not inherit from the ad group or campaign, the corresponding item in the list will be nil.<br/><br/>This element is not returned by default. You must set *ReturnInheritedBidStrategyTypes* true in the request.|**string** array|
|<a name="partialerrors"></a>PartialErrors|An array of [BatchError](batcherror.md) objects that contain details for any request items that were not successful.<br /><br />The list of errors do not correspond directly to the list of items in the request. The list can be empty if there were no errors, or can include one or more error objects corresponding to each unsuccessful list item in the request.|[BatchError](batcherror.md) array|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
The following template shows the order of the [body](#request-body) and [header](#request-header) elements for the SOAP request.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
    <Action mustUnderstand="1">UpdateKeywords</Action>
    <ApplicationToken i:nil="false">ValueHere</ApplicationToken>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <CustomerAccountId i:nil="false">ValueHere</CustomerAccountId>
    <CustomerId i:nil="false">ValueHere</CustomerId>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
    <Password i:nil="false">ValueHere</Password>
    <UserName i:nil="false">ValueHere</UserName>
  </s:Header>
  <s:Body>
    <UpdateKeywordsRequest xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
      <AdGroupId>ValueHere</AdGroupId>
      <Keywords i:nil="false">
        <Keyword>
          <Bid i:nil="false">
            <Amount i:nil="false">ValueHere</Amount>
          </Bid>
          <BiddingScheme i:nil="false" i:type="-- derived type specified here with the appropriate prefix --">
            <Type i:nil="false">ValueHere</Type>
            <!--This field is applicable if the derived type attribute is set to MaxClicksBiddingScheme-->
            <MaxCpc i:nil="false">
              <Amount i:nil="false">ValueHere</Amount>
            </MaxCpc>
            <!--This field is applicable if the derived type attribute is set to MaxConversionsBiddingScheme-->
            <MaxCpc i:nil="false">
              <Amount i:nil="false">ValueHere</Amount>
            </MaxCpc>
            <!--These fields are applicable if the derived type attribute is set to TargetCpaBiddingScheme-->
            <MaxCpc i:nil="false">
              <Amount i:nil="false">ValueHere</Amount>
            </MaxCpc>
            <TargetCpa i:nil="false">ValueHere</TargetCpa>
            <!--No additional fields are applicable if the derived type attribute is set to ManualCpcBiddingScheme-->
            <!--No additional fields are applicable if the derived type attribute is set to EnhancedCpcBiddingScheme-->
            <!--This field is applicable if the derived type attribute is set to InheritFromParentBiddingScheme-->
            <InheritedBidStrategyType i:nil="false">ValueHere</InheritedBidStrategyType>
          </BiddingScheme>
          <DestinationUrl i:nil="false">ValueHere</DestinationUrl>
          <EditorialStatus i:nil="false">ValueHere</EditorialStatus>
          <FinalAppUrls xmlns:e1241="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1241:AppUrl>
              <e1241:OsType i:nil="false">ValueHere</e1241:OsType>
              <e1241:Url i:nil="false">ValueHere</e1241:Url>
            </e1241:AppUrl>
          </FinalAppUrls>
          <FinalMobileUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalMobileUrls>
          <FinalUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalUrls>
          <ForwardCompatibilityMap xmlns:e1242="http://schemas.datacontract.org/2004/07/System.Collections.Generic" i:nil="false">
            <e1242:KeyValuePairOfstringstring>
              <e1242:key i:nil="false">ValueHere</e1242:key>
              <e1242:value i:nil="false">ValueHere</e1242:value>
            </e1242:KeyValuePairOfstringstring>
          </ForwardCompatibilityMap>
          <Id i:nil="false">ValueHere</Id>
          <MatchType i:nil="false">ValueHere</MatchType>
          <Param1 i:nil="false">ValueHere</Param1>
          <Param2 i:nil="false">ValueHere</Param2>
          <Param3 i:nil="false">ValueHere</Param3>
          <Status i:nil="false">ValueHere</Status>
          <Text i:nil="false">ValueHere</Text>
          <TrackingUrlTemplate i:nil="false">ValueHere</TrackingUrlTemplate>
          <UrlCustomParameters xmlns:e1243="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1243:Parameters i:nil="false">
              <e1243:CustomParameter>
                <e1243:Key i:nil="false">ValueHere</e1243:Key>
                <e1243:Value i:nil="false">ValueHere</e1243:Value>
              </e1243:CustomParameter>
            </e1243:Parameters>
          </UrlCustomParameters>
        </Keyword>
      </Keywords>
      <ReturnInheritedBidStrategyTypes i:nil="false">ValueHere</ReturnInheritedBidStrategyTypes>
    </UpdateKeywordsRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
The following template shows the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <UpdateKeywordsResponse xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
      <InheritedBidStrategyTypes d4p1:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <a1:string>ValueHere</a1:string>
      </InheritedBidStrategyTypes>
      <PartialErrors d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <BatchError d4p1:type="-- derived type specified here with the appropriate prefix --">
          <Code>ValueHere</Code>
          <Details d4p1:nil="false">ValueHere</Details>
          <ErrorCode d4p1:nil="false">ValueHere</ErrorCode>
          <FieldPath d4p1:nil="false">ValueHere</FieldPath>
          <ForwardCompatibilityMap xmlns:e1244="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
            <e1244:KeyValuePairOfstringstring>
              <e1244:key d4p1:nil="false">ValueHere</e1244:key>
              <e1244:value d4p1:nil="false">ValueHere</e1244:value>
            </e1244:KeyValuePairOfstringstring>
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
    </UpdateKeywordsResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<UpdateKeywordsResponse> UpdateKeywordsAsync(
	long adGroupId,
	IList<Keyword> keywords,
	bool? returnInheritedBidStrategyTypes)
{
	var request = new UpdateKeywordsRequest
	{
		AdGroupId = adGroupId,
		Keywords = keywords,
		ReturnInheritedBidStrategyTypes = returnInheritedBidStrategyTypes
	};

	return (await CampaignManagementService.CallAsync((s, r) => s.UpdateKeywordsAsync(r), request));
}
```
```java
static UpdateKeywordsResponse updateKeywords(
	java.lang.Long adGroupId,
	ArrayOfKeyword keywords,
	boolean returnInheritedBidStrategyTypes) throws RemoteException, Exception
{
	UpdateKeywordsRequest request = new UpdateKeywordsRequest();

	request.setAdGroupId(adGroupId);
	request.setKeywords(keywords);
	request.setReturnInheritedBidStrategyTypes(returnInheritedBidStrategyTypes);

	return CampaignManagementService.getService().updateKeywords(request);
}
```
```php
static function UpdateKeywords(
	$adGroupId,
	$keywords,
	$returnInheritedBidStrategyTypes)
{

	$GLOBALS['Proxy'] = $GLOBALS['CampaignManagementProxy'];

	$request = new UpdateKeywordsRequest();

	$request->AdGroupId = $adGroupId;
	$request->Keywords = $keywords;
	$request->ReturnInheritedBidStrategyTypes = $returnInheritedBidStrategyTypes;

	return $GLOBALS['CampaignManagementProxy']->GetService()->UpdateKeywords($request);
}
```
```python
response=campaignmanagement_service.UpdateKeywords(
	AdGroupId=AdGroupId,
	Keywords=Keywords,
	ReturnInheritedBidStrategyTypes=ReturnInheritedBidStrategyTypes)
```

## Requirements
Service: [CampaignManagementService.svc v12](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v12/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v12  

