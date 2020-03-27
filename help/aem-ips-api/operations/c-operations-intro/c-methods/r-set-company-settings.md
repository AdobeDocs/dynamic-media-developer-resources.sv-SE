---
description: Anger olika företagsspecifika konfigurationsvärden.
seo-description: Anger olika företagsspecifika konfigurationsvärden.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Scene7 Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| ` *`overwriteMode`*` | `xsd:string` | Nej | Tillgångsöverskrivningsläge. |
| ` *`keepPublishState`*` | `xsd:boolean` | Nej | Ange att publiceringstillståndet ska `true` bevaras när en resurs överförs igen. |
| ` *`defaultSourceProfileHandle`*` | `xsd:string` | Nej | IccProfile-resurs som ska användas som standardkällfärgprofil. |
| ` *`defaultDisplayProfileHandle`*` | `xsd:string` | Nej | IccProfile-resurs som ska användas som standardprofil för visningsfärg. |
| ` *`iptcExifMappingXsltHandle`*` | `xsd:string` | Nej | XSL-resurs som används för att mappa IPTC- och EXIF-metadata till IPS-metadatafält. |
| ` *`xmpMappingXsltHandle`*` | `xsd:string` | Nej | XSL-resurs som används för att mappa XMP-metadata till IPS-metadatafält. |
| ` *`discSpaceWarningMin`*` | `xsd:int` | Nej | Minsta lediga diskutrymme (i kB) som är tillgängligt innan ett varningsmeddelande skickas. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Nej | Ange att företagsadministratörer ska `true` få ett meddelande varje gång resurser tömts från papperskorgen. |

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
