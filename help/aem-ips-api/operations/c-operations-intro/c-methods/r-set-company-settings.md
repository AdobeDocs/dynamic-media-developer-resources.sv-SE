---
description: Anger olika företagsspecifika konfigurationsvärden.
seo-description: Anger olika företagsspecifika konfigurationsvärden.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
uuid: 5908082f-6743-4444-ba73-757ad4664890
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# setCompanySettings{#setcompanysettings}

Anger olika företagsspecifika konfigurationsvärden.

Syntax

## Auktoriserade användartyper {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-a472da6c57c74a94a179dda081004888}

**Indata (setCompanySettingsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`overwriteMode`*` | `xsd:string` | Nej | Tillgångsöverskrivningsläge. |
| `*`keepPublishState`*` | `xsd:boolean` | Nej | Ange `true` för att bevara publiceringstillståndet när en resurs överförs igen. |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | Nej | IccProfile-resurs som ska användas som standardkällfärgprofil. |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | Nej | IccProfile-resurs som ska användas som standardprofil för visningsfärg. |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | Nej | XSL-resurs som används för att mappa IPTC- och EXIF-metadata till IPS-metadatafält. |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | Nej | XSL-resurs som används för att mappa XMP metadata till IPS-metadatafält. |
| `*`discSpaceWarningMin`*` | `xsd:int` | Nej | Minsta lediga diskutrymme (i kB) som är tillgängligt innan ett varningsmeddelande skickas. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Nej | Ange `true` för att skicka ett meddelande till företagsadministratörer när resurser tömts från papperskorgen. |

**Utdata (setCompanySettingsReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Det här kodexemplet anger ett företags konfiguration.

**Begäran**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Svar**

Ingen.
