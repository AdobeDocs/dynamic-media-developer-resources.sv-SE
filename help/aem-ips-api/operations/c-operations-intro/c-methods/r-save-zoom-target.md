---
description: Skapa eller redigera ett zoommål.
seo-description: Skapa eller redigera ett zoommål.
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Scene7 Image Production System API
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveZoomTarget{#savezoomtarget}

Skapa eller redigera ett zoommål.

Syntax

## Auktoriserad användartyp {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-4a23983cae4e49a098e9bbe736933996}

**Indata (saveZoomTargetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med det zoommål som du vill spara. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Handtaget till zoommålet. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Nej | Redigerar eller skapar ett zoommål. |
| ` *`name`*` | `xsd:string` | Ja | Zoommålnamn. |
| ` *`xPosition`*` | `xsd:int` | Ja | Vänster pixelplacering. |
| ` *`yPosition`*` | `xsd:int` | Ja | Plats för övre pixel. |
| ` *`width`*` | `xsd:int` | Ja | Zooma målbredd. |
| ` *`height`*` | `xsd:int` | Ja | Zooma målhöjd. |
| ` *`userData`*` | `xsd:string` | Ja | För kundspecifik information. Kan innehålla alla typer av data. |

**Utdata (saveZoomTargetReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`zoomTargetHandle`*` | `xsd:string` | Ja | Hantera det nyskapade zoommålet. |

## Exempel {#section-509c472c316549cdb228d7e1cfa8400a}

Det här kodexemplet sparar ett zoommål. Svaret returnerar zoommålreferensen.

**Begäran**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Svar**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```

