---
description: Anger det zoommål som är associerat med en resursbild. Befintliga zoommål skrivs över.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`assetHandle`*` | `xsd:string` | Ja | Tillgång till det zoommål som du vill ange. |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Ja | Matris med zoommåldefinitioner. |

**Utdata (setZoomTargetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | Ja | Den uppsättning handtag för de zoommål som skapas av den här åtgärden. |

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

