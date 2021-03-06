---
title: UpdateAdExtensions Service Operation - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Updates one or more ad extensions within an account's ad extension library.
dev_langs: 
  - csharp
  - java
  - php
  - python
---
> [!IMPORTANT]
> This Bing Ads API Version 12 preview documentation is subject to change. To return to version 11 content, use the version selector near the table of contents at the top and left side of the page.

# UpdateAdExtensions Service Operation - Campaign Management
Updates one or more ad extensions within an account's ad extension library.

## <a name="request"></a>Request Elements
The *UpdateAdExtensionsRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="accountid"></a>AccountId|The identifier of the account which contains the extensions.|**long**|
|<a name="adextensions"></a>AdExtensions|The list of ad extensions of any type, to update within the account. You may specify a maximum of 100 extensions per call.|[AdExtension](adextension.md) array|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *UpdateAdExtensionsResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="nestedpartialerrors"></a>NestedPartialErrors|An array of [BatchErrorCollection](batcherrorcollection.md) objects that contain details for any ad extensions that were not successfully updated. The top level error within each [BatchErrorCollection](batcherrorcollection.md) object corresponds to potential ad extension errors. The nested list of [BatchError](batcherror.md) objects would include any errors specific to the list items within an ad extension (if applicable).<br/><br/>The list of errors do not correspond directly to the list of items in the request. The list can be empty if there were no errors, or can include one or more error objects corresponding to each unsuccessful list item in the request.|[BatchErrorCollection](batcherrorcollection.md) array|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
The following template shows the order of the [body](#request-body) and [header](#request-header) elements for the SOAP request.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
    <Action mustUnderstand="1">UpdateAdExtensions</Action>
    <ApplicationToken i:nil="false">ValueHere</ApplicationToken>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <CustomerAccountId i:nil="false">ValueHere</CustomerAccountId>
    <CustomerId i:nil="false">ValueHere</CustomerId>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
    <Password i:nil="false">ValueHere</Password>
    <UserName i:nil="false">ValueHere</UserName>
  </s:Header>
  <s:Body>
    <UpdateAdExtensionsRequest xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
      <AccountId>ValueHere</AccountId>
      <AdExtensions i:nil="false">
        <AdExtension i:type="-- derived type specified here with the appropriate prefix --">
          <DevicePreference i:nil="false">ValueHere</DevicePreference>
          <ForwardCompatibilityMap xmlns:e1207="http://schemas.datacontract.org/2004/07/System.Collections.Generic" i:nil="false">
            <e1207:KeyValuePairOfstringstring>
              <e1207:key i:nil="false">ValueHere</e1207:key>
              <e1207:value i:nil="false">ValueHere</e1207:value>
            </e1207:KeyValuePairOfstringstring>
          </ForwardCompatibilityMap>
          <Id i:nil="false">ValueHere</Id>
          <Scheduling i:nil="false">
            <DayTimeRanges i:nil="false">
              <DayTime>
                <Day>ValueHere</Day>
                <EndHour>ValueHere</EndHour>
                <EndMinute>ValueHere</EndMinute>
                <StartHour>ValueHere</StartHour>
                <StartMinute>ValueHere</StartMinute>
              </DayTime>
            </DayTimeRanges>
            <EndDate i:nil="false">
              <Day>ValueHere</Day>
              <Month>ValueHere</Month>
              <Year>ValueHere</Year>
            </EndDate>
            <StartDate i:nil="false">
              <Day>ValueHere</Day>
              <Month>ValueHere</Month>
              <Year>ValueHere</Year>
            </StartDate>
            <UseSearcherTimeZone i:nil="false">ValueHere</UseSearcherTimeZone>
          </Scheduling>
          <Status i:nil="false">ValueHere</Status>
          <Type i:nil="false">ValueHere</Type>
          <Version i:nil="false">ValueHere</Version>
          <!--These fields are applicable if the derived type attribute is set to LocationAdExtension-->
          <Address i:nil="false">
            <CityName i:nil="false">ValueHere</CityName>
            <CountryCode i:nil="false">ValueHere</CountryCode>
            <PostalCode i:nil="false">ValueHere</PostalCode>
            <ProvinceCode i:nil="false">ValueHere</ProvinceCode>
            <ProvinceName i:nil="false">ValueHere</ProvinceName>
            <StreetAddress i:nil="false">ValueHere</StreetAddress>
            <StreetAddress2 i:nil="false">ValueHere</StreetAddress2>
          </Address>
          <CompanyName i:nil="false">ValueHere</CompanyName>
          <GeoCodeStatus i:nil="false">ValueHere</GeoCodeStatus>
          <GeoPoint i:nil="false">
            <LatitudeInMicroDegrees>ValueHere</LatitudeInMicroDegrees>
            <LongitudeInMicroDegrees>ValueHere</LongitudeInMicroDegrees>
          </GeoPoint>
          <IconMediaId i:nil="false">ValueHere</IconMediaId>
          <ImageMediaId i:nil="false">ValueHere</ImageMediaId>
          <PhoneNumber i:nil="false">ValueHere</PhoneNumber>
          <!--These fields are applicable if the derived type attribute is set to CallAdExtension-->
          <CountryCode i:nil="false">ValueHere</CountryCode>
          <IsCallOnly i:nil="false">ValueHere</IsCallOnly>
          <IsCallTrackingEnabled i:nil="false">ValueHere</IsCallTrackingEnabled>
          <PhoneNumber i:nil="false">ValueHere</PhoneNumber>
          <RequireTollFreeTrackingNumber i:nil="false">ValueHere</RequireTollFreeTrackingNumber>
          <!--These fields are applicable if the derived type attribute is set to ImageAdExtension-->
          <AlternativeText i:nil="false">ValueHere</AlternativeText>
          <Description i:nil="false">ValueHere</Description>
          <DestinationUrl i:nil="false">ValueHere</DestinationUrl>
          <FinalAppUrls xmlns:e1208="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1208:AppUrl>
              <e1208:OsType i:nil="false">ValueHere</e1208:OsType>
              <e1208:Url i:nil="false">ValueHere</e1208:Url>
            </e1208:AppUrl>
          </FinalAppUrls>
          <FinalMobileUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalMobileUrls>
          <FinalUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalUrls>
          <ImageMediaIds i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:long>ValueHere</a1:long>
          </ImageMediaIds>
          <TrackingUrlTemplate i:nil="false">ValueHere</TrackingUrlTemplate>
          <UrlCustomParameters xmlns:e1209="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1209:Parameters i:nil="false">
              <e1209:CustomParameter>
                <e1209:Key i:nil="false">ValueHere</e1209:Key>
                <e1209:Value i:nil="false">ValueHere</e1209:Value>
              </e1209:CustomParameter>
            </e1209:Parameters>
          </UrlCustomParameters>
          <!--These fields are applicable if the derived type attribute is set to AppAdExtension-->
          <AppPlatform i:nil="false">ValueHere</AppPlatform>
          <AppStoreId i:nil="false">ValueHere</AppStoreId>
          <DestinationUrl i:nil="false">ValueHere</DestinationUrl>
          <DisplayText i:nil="false">ValueHere</DisplayText>
          <FinalAppUrls xmlns:e1210="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1210:AppUrl>
              <e1210:OsType i:nil="false">ValueHere</e1210:OsType>
              <e1210:Url i:nil="false">ValueHere</e1210:Url>
            </e1210:AppUrl>
          </FinalAppUrls>
          <FinalMobileUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalMobileUrls>
          <FinalUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalUrls>
          <TrackingUrlTemplate i:nil="false">ValueHere</TrackingUrlTemplate>
          <UrlCustomParameters xmlns:e1211="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1211:Parameters i:nil="false">
              <e1211:CustomParameter>
                <e1211:Key i:nil="false">ValueHere</e1211:Key>
                <e1211:Value i:nil="false">ValueHere</e1211:Value>
              </e1211:CustomParameter>
            </e1211:Parameters>
          </UrlCustomParameters>
          <!--These fields are applicable if the derived type attribute is set to ReviewAdExtension-->
          <IsExact>ValueHere</IsExact>
          <Source i:nil="false">ValueHere</Source>
          <Text i:nil="false">ValueHere</Text>
          <Url i:nil="false">ValueHere</Url>
          <!--This field is applicable if the derived type attribute is set to CalloutAdExtension-->
          <Text i:nil="false">ValueHere</Text>
          <!--These fields are applicable if the derived type attribute is set to SitelinkAdExtension-->
          <Description1 i:nil="false">ValueHere</Description1>
          <Description2 i:nil="false">ValueHere</Description2>
          <DestinationUrl i:nil="false">ValueHere</DestinationUrl>
          <DisplayText i:nil="false">ValueHere</DisplayText>
          <FinalAppUrls xmlns:e1212="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1212:AppUrl>
              <e1212:OsType i:nil="false">ValueHere</e1212:OsType>
              <e1212:Url i:nil="false">ValueHere</e1212:Url>
            </e1212:AppUrl>
          </FinalAppUrls>
          <FinalMobileUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalMobileUrls>
          <FinalUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </FinalUrls>
          <TrackingUrlTemplate i:nil="false">ValueHere</TrackingUrlTemplate>
          <UrlCustomParameters xmlns:e1213="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1213:Parameters i:nil="false">
              <e1213:CustomParameter>
                <e1213:Key i:nil="false">ValueHere</e1213:Key>
                <e1213:Value i:nil="false">ValueHere</e1213:Value>
              </e1213:CustomParameter>
            </e1213:Parameters>
          </UrlCustomParameters>
          <!--These fields are applicable if the derived type attribute is set to StructuredSnippetAdExtension-->
          <Header i:nil="false">ValueHere</Header>
          <Values i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <a1:string>ValueHere</a1:string>
          </Values>
          <!--These fields are applicable if the derived type attribute is set to PriceAdExtension-->
          <Language i:nil="false">ValueHere</Language>
          <PriceExtensionType>ValueHere</PriceExtensionType>
          <TableRows i:nil="false">
            <PriceTableRow>
              <CurrencyCode i:nil="false">ValueHere</CurrencyCode>
              <Description i:nil="false">ValueHere</Description>
              <FinalMobileUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
                <a1:string>ValueHere</a1:string>
              </FinalMobileUrls>
              <FinalUrls i:nil="false" xmlns:a1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
                <a1:string>ValueHere</a1:string>
              </FinalUrls>
              <Header i:nil="false">ValueHere</Header>
              <Price>ValueHere</Price>
              <PriceQualifier>ValueHere</PriceQualifier>
              <PriceUnit>ValueHere</PriceUnit>
              <TermsAndConditions i:nil="false">ValueHere</TermsAndConditions>
              <TermsAndConditionsUrl i:nil="false">ValueHere</TermsAndConditionsUrl>
            </PriceTableRow>
          </TableRows>
          <TrackingUrlTemplate i:nil="false">ValueHere</TrackingUrlTemplate>
          <UrlCustomParameters xmlns:e1214="http://schemas.datacontract.org/2004/07/Microsoft.AdCenter.Advertiser.CampaignManagement.Api.DataContracts.V12" i:nil="false">
            <e1214:Parameters i:nil="false">
              <e1214:CustomParameter>
                <e1214:Key i:nil="false">ValueHere</e1214:Key>
                <e1214:Value i:nil="false">ValueHere</e1214:Value>
              </e1214:CustomParameter>
            </e1214:Parameters>
          </UrlCustomParameters>
        </AdExtension>
      </AdExtensions>
    </UpdateAdExtensionsRequest>
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
    <UpdateAdExtensionsResponse xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
      <NestedPartialErrors d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <BatchErrorCollection d4p1:type="-- derived type specified here with the appropriate prefix --">
          <BatchErrors d4p1:nil="false">
            <BatchError d4p1:type="-- derived type specified here with the appropriate prefix --">
              <Code>ValueHere</Code>
              <Details d4p1:nil="false">ValueHere</Details>
              <ErrorCode d4p1:nil="false">ValueHere</ErrorCode>
              <FieldPath d4p1:nil="false">ValueHere</FieldPath>
              <ForwardCompatibilityMap xmlns:e1215="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
                <e1215:KeyValuePairOfstringstring>
                  <e1215:key d4p1:nil="false">ValueHere</e1215:key>
                  <e1215:value d4p1:nil="false">ValueHere</e1215:value>
                </e1215:KeyValuePairOfstringstring>
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
          </BatchErrors>
          <Code d4p1:nil="false">ValueHere</Code>
          <Details d4p1:nil="false">ValueHere</Details>
          <ErrorCode d4p1:nil="false">ValueHere</ErrorCode>
          <FieldPath d4p1:nil="false">ValueHere</FieldPath>
          <ForwardCompatibilityMap xmlns:e1216="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
            <e1216:KeyValuePairOfstringstring>
              <e1216:key d4p1:nil="false">ValueHere</e1216:key>
              <e1216:value d4p1:nil="false">ValueHere</e1216:value>
            </e1216:KeyValuePairOfstringstring>
          </ForwardCompatibilityMap>
          <Index>ValueHere</Index>
          <Message d4p1:nil="false">ValueHere</Message>
          <Type d4p1:nil="false">ValueHere</Type>
          <!--These fields are applicable if the derived type attribute is set to EditorialErrorCollection-->
          <Appealable d4p1:nil="false">ValueHere</Appealable>
          <DisapprovedText d4p1:nil="false">ValueHere</DisapprovedText>
          <Location d4p1:nil="false">ValueHere</Location>
          <PublisherCountry d4p1:nil="false">ValueHere</PublisherCountry>
          <ReasonCode>ValueHere</ReasonCode>
        </BatchErrorCollection>
      </NestedPartialErrors>
    </UpdateAdExtensionsResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<UpdateAdExtensionsResponse> UpdateAdExtensionsAsync(
	long accountId,
	IList<AdExtension> adExtensions)
{
	var request = new UpdateAdExtensionsRequest
	{
		AccountId = accountId,
		AdExtensions = adExtensions
	};

	return (await CampaignManagementService.CallAsync((s, r) => s.UpdateAdExtensionsAsync(r), request));
}
```
```java
static UpdateAdExtensionsResponse updateAdExtensions(
	java.lang.Long accountId,
	ArrayOfAdExtension adExtensions) throws RemoteException, Exception
{
	UpdateAdExtensionsRequest request = new UpdateAdExtensionsRequest();

	request.setAccountId(accountId);
	request.setAdExtensions(adExtensions);

	return CampaignManagementService.getService().updateAdExtensions(request);
}
```
```php
static function UpdateAdExtensions(
	$accountId,
	$adExtensions)
{

	$GLOBALS['Proxy'] = $GLOBALS['CampaignManagementProxy'];

	$request = new UpdateAdExtensionsRequest();

	$request->AccountId = $accountId;
	$request->AdExtensions = $adExtensions;

	return $GLOBALS['CampaignManagementProxy']->GetService()->UpdateAdExtensions($request);
}
```
```python
response=campaignmanagement_service.UpdateAdExtensions(
	AccountId=AccountId,
	AdExtensions=AdExtensions)
```

## Requirements
Service: [CampaignManagementService.svc v12](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v12/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v12  

