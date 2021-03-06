---
title: PriceUnit Value Set - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Defines price units for price ad extensions.
---
> [!IMPORTANT]
> This Bing Ads API Version 12 preview documentation is subject to change. To return to version 11 content, use the version selector near the table of contents at the top and left side of the page.

# PriceUnit Value Set - Campaign Management
Defines price units for price ad extensions.

## Syntax
```xml
<xs:simpleType name="PriceUnit" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:restriction base="xs:string">
    <xs:enumeration value="Unknown" />
    <xs:enumeration value="PerHour" />
    <xs:enumeration value="PerDay" />
    <xs:enumeration value="PerWeek" />
    <xs:enumeration value="PerMonth" />
    <xs:enumeration value="PerYear" />
    <xs:enumeration value="None" />
    <xs:enumeration value="PerNight" />
  </xs:restriction>
</xs:simpleType>
```

## <a name="values"></a>Values

|Value|Description|
|-----------|---------------|
|<a name="none"></a>None|The price of the [PriceAdExtension](priceadextension.md) will not be appended with price unit text.|
|<a name="perday"></a>PerDay|The *Per Day* price unit text will be appended to the price of the [PriceAdExtension](priceadextension.md), for example *$9.99 Per Day*.|
|<a name="perhour"></a>PerHour|The *Per Hour* price unit text will be appended to the price of the [PriceAdExtension](priceadextension.md), for example *$9.99 Per Hour*.|
|<a name="permonth"></a>PerMonth|The *Per Month* price unit text will be appended to the price of the [PriceAdExtension](priceadextension.md), for example *$9.99 Per Month*.|
|<a name="pernight"></a>PerNight|The *Per Night* price unit text will be appended to the price of the [PriceAdExtension](priceadextension.md), for example *$9.99 Per Night*.|
|<a name="perweek"></a>PerWeek|The *Per Week* price unit text will be appended to the price of the [PriceAdExtension](priceadextension.md), for example *$9.99 Per Week*.|
|<a name="peryear"></a>PerYear|The *Per Year* price unit text will be appended to the price of the [PriceAdExtension](priceadextension.md), for example *$9.99 Per Year*.|
|<a name="unknown"></a>Unknown|Reserved for forward compatibility.|

## Requirements
Service: [CampaignManagementService.svc v12](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v12/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v12  

## Used By
[PriceTableRow](pricetablerow.md)  
