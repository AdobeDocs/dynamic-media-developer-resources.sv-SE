---
description: Returnerar IPS-inställningar för ett visst företag.
seo-description: Returnerar IPS-inställningar för ett visst företag.
seo-title: getCompanySettings
solution: Experience Manager
title: getCompanySettings
topic: Dynamic Media Image Production System API
uuid: 28ee706d-aaef-45a1-9655-3805f158cdc3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# getCompanySettings{#getcompanysettings}

Returnerar IPS-inställningar för ett visst företag.

Syntax

## Auktoriserade användartyper {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-e146f479c2744baa8f68be8c8848c97f}

**Indata (getCompanySettingsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag vars inställningar du vill hämta. |

**Utdata (getCompanySettingsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`inställningar`*` | `types:CompanySettings` | Ja | Företagsinställningar. |

## Exempel {#section-191f78995ecf473a95eadf7296204fd7}

Detta kodexempel returnerar alla IPS-inställningar för ett visst företag.

**Begäran**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**Svar**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```

