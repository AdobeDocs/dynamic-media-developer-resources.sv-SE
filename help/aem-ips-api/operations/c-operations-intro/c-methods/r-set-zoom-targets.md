---
description: Anger det zoommål som är associerat med en resursbild. Befintliga zoommål skrivs över.
seo-description: Anger det zoommål som är associerat med en resursbild. Befintliga zoommål skrivs över.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setZoomTargets{#setzoomtargets}

Anger det zoommål som är associerat med en resursbild. Befintliga zoommål skrivs över.

Syntax

## Auktoriserade användartyper {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-161f8c733cc4439f94a06e12119d4226}

**Indata (setZoomTargetsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Tillgång till det zoommål som du vill ange. |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Ja | Matris med zoommåldefinitioner. |

**Utdata (setZoomTargetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | Ja | Den uppsättning handtag för de zoommål som skapas av den här åtgärden. |

## Exempel {#section-a2f14c7a1499443e96d099ea8a76c182}

Detta kodexempel definierar en array med zoommål efter namn, position (x- och y-axel), bredd, höjd och tilldelar arrayen till en resurs. Svaret innehåller handtag till de nya zoommålen.

**Begäran**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Svar**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```

