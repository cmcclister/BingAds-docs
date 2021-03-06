---
title: BMCStore Data Object - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Defines a Bing Merchant Center store.
---
> [!IMPORTANT]
> This Bing Ads API Version 12 preview documentation is subject to change. To return to version 11 content, use the version selector near the table of contents at the top and left side of the page.

# BMCStore Data Object - Campaign Management
Defines a Bing Merchant Center store.

Elements of this object are defined in the Bing Merchant Center store, and read-only in Bing Ads.  Values of elements do not restrict Bing Ads features. For example, a Bing Shopping campaign and product ad may be added whether the *IsActive* element is set to true or false.

## Syntax
```xml
<xs:complexType name="BMCStore" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:sequence>
    <xs:element minOccurs="0" name="HasCatalog" type="xs:boolean" />
    <xs:element minOccurs="0" name="Id" type="xs:long" />
    <xs:element minOccurs="0" name="IsActive" type="xs:boolean" />
    <xs:element minOccurs="0" name="IsProductAdsEnabled" type="xs:boolean" />
    <xs:element minOccurs="0" name="Name" nillable="true" type="xs:string" />
    <xs:element minOccurs="0" name="SubType" nillable="true" type="tns:BMCStoreSubType" />
  </xs:sequence>
</xs:complexType>
```

## <a name="elements"></a>Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="hascatalog"></a>HasCatalog|Value will be true if the store has a catalog of items, and otherwise the value is false.|**boolean**|
|<a name="id"></a>Id|The unique identifier for the  Bing Merchant Center store.|**long**|
|<a name="isactive"></a>IsActive|Value will be true if the store is active, and otherwise the value is false.|**boolean**|
|<a name="isproductadsenabled"></a>IsProductAdsEnabled|Value will be true if the store is enabled for product ads in Bing Ads, and otherwise the value is false.|**boolean**|
|<a name="name"></a>Name|Defines the name of the store as defined in the Bing Merchant Center.|**string**|
|<a name="subtype"></a>SubType|Reserved.|[BMCStoreSubType](bmcstoresubtype.md)|

## Requirements
Service: [CampaignManagementService.svc v12](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v12/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v12  

## Used By
[GetBMCStoresByCustomerId](getbmcstoresbycustomerid.md)  
