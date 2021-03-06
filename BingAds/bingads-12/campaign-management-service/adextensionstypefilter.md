---
title: AdExtensionsTypeFilter Value Set - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Defines the possible ad extension types.
---
> [!IMPORTANT]
> This Bing Ads API Version 12 preview documentation is subject to change. To return to version 11 content, use the version selector near the table of contents at the top and left side of the page.

# AdExtensionsTypeFilter Value Set - Campaign Management
Defines the possible ad extension types.

## Syntax
```xml
<xs:simpleType name="AdExtensionsTypeFilter" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:list>
    <xs:simpleType>
      <xs:restriction base="xs:string">
        <xs:enumeration value="LocationAdExtension" />
        <xs:enumeration value="CallAdExtension" />
        <xs:enumeration value="ImageAdExtension" />
        <xs:enumeration value="AppAdExtension" />
        <xs:enumeration value="ReviewAdExtension" />
        <xs:enumeration value="CalloutAdExtension" />
        <xs:enumeration value="SitelinkAdExtension" />
        <xs:enumeration value="StructuredSnippetAdExtension" />
        <xs:enumeration value="PriceAdExtension" />
      </xs:restriction>
    </xs:simpleType>
  </xs:list>
</xs:simpleType>
```

## <a name="values"></a>Values

|Value|Description|
|-----------|---------------|
|<a name="appadextension"></a>AppAdExtension|An ad extension that contains a link to install an application from a supported app store. For more information, see [AppAdExtension](appadextension.md).|
|<a name="calladextension"></a>CallAdExtension|An ad extension that contains a phone number and whether it's the only clickable item in an ad. For more information, see [CallAdExtension](calladextension.md).|
|<a name="calloutadextension"></a>CalloutAdExtension|An ad extension that contains additional text in the ad that can describe more about your business, products, or services. For more information, see [CalloutAdExtension](calloutadextension.md).|
|<a name="imageadextension"></a>ImageAdExtension|An ad extension that contains an image with alternative text. For more information, see [ImageAdExtension](imageadextension.md).|
|<a name="locationadextension"></a>LocationAdExtension|An ad extension that contains the address and phone number of the business. For more information, see [LocationAdExtension](locationadextension.md).|
|<a name="priceadextension"></a>PriceAdExtension|An ad extension that includes between 3 and 8 price table rows. For more information, see [PriceAdExtension](priceadextension.md).|
|<a name="reviewadextension"></a>ReviewAdExtension|An ad extension that contains third-party reviews (exact or paraphrased) about your business, products, or services. For more information, see [ReviewAdExtension](reviewadextension.md).|
|<a name="sitelinkadextension"></a>SitelinkAdExtension|An ad extension that contains one site link. For more information, see [SitelinkAdExtension](sitelinkadextension.md).|
|<a name="structuredsnippetadextension"></a>StructuredSnippetAdExtension|An ad extension that contains a header and values that tell customers more about your business. For more information, see [StructuredSnippetAdExtension](structuredsnippetadextension.md).|

## Requirements
Service: [CampaignManagementService.svc v12](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v12/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v12  

## Used By
[GetAdExtensionIdsByAccountId](getadextensionidsbyaccountid.md)  
[GetAdExtensionsAssociations](getadextensionsassociations.md)  
[GetAdExtensionsByIds](getadextensionsbyids.md)  
