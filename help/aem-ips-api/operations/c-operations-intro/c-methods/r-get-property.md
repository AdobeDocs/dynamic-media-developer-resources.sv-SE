---
description: Hämtar strängvärden för systemegenskaper som är relaterade till Image Portal.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# getProperty{#getproperty}

Hämtar strängvärden för systemegenskaper som är relaterade till Image Portal.

Följande systemegenskaper stöds:

* `IpsVersion`: IPS-versionsnummer.
* `IpsImageServerUrl`: Fullständigt, externt URL-prefix för IPS Image Server.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: URL-prefix för återgivning av SVG-resurser.
* `SvgRenderEnabled`: True om SVG-resurser kan återges av  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Maximal storlek (i byte) för fildata som tillåts i en överföring  [!DNL POST]. Filer som är större än maxgränsen nekas.

## Auktoriserade användartyper {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Indata (getPropertyParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`name`*` | `xsd:string` | Ja | Namnet på den egenskap som ska hämtas. |

**Utdata (getPropertyReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`value`*` | `xsd:string` | Ja | Egenskapsvärdet. |

## Exempel {#section-3f80a78dd60c404181b34d3a912d7a36}

I det här kodexemplet används en IPS Properties-strängkonstant för att returnera ett specifikt värde. I det här exemplet är egenskapen IPS versionen av IPS-servern.

**Begäran**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Svar**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
