---
description: Skapar en ny resurs som härletts från en befintlig primär källbildresurs.
seo-description: Skapar en ny resurs som härletts från en befintlig primär källbildresurs.
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
topic: Scene7 Image Production System API
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# createDerivedAsset{#createderivedasset}

Skapar en ny resurs som härletts från en befintlig primär källbildresurs.

Syntax

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Härledda resurser anger Image Server-protokollkommandon som ändrar representationen av ägarbilden. Med den `AdjustedView` härledda typen kan du göra enkla ändringar i en enskild bild (till exempel genom att ange en beskärningsrektangel), medan den `LayerView` hjälper dig att skapa en vy med flera lager som kan innehålla text eller ytterligare bilder.

Till skillnad från en bildkopia (se [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)) länkas en härledd bild till sin ägarbild. Ändringar av ägarbilden ändrar associerade härledda resurser. Om du tar bort ägarbilden tas alla tillhörande härledda bilder bort.

## Auktoriserade användartyper {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-5a0dde01cff6454da3646ea805c2be1e}

**Indata (createDerivedAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till det företag som innehåller den tillgång som du kommer att hämta den nya tillgången från. |
| ` *`ownerHandle`*` | `xsd:string` | Ja | Handtaget till den primära bildresurs som den nya bilden kommer att härledas från. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Referensen till mappen där den nya härledda resursen ska skapas. |
| ` *`name`*` | `xsd:string` | Ja | Namnet på den härledda tillgången. |
| ` *`type`*` | `xsd:string` | Ja | Tillgångstypen för den nya härledda tillgången: `AdjustedView` eller `LayerView`. |
| ` *`urlModifier`*` | `xsd:string` | Nej | Bildredigerings- eller bildåtergivningsprotokollkommandon som används *före* begäran eller `urlPostApplyModifier` kommandona. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Nej | Bildredigerings- eller bildåtergivningsprotokollkommandon som används *efter* begäran eller `urlPostApplyModifier` kommandona. |

**Utdata (createDerivedAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Referensen till den härledda tillgången. |

## Exempel {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

Exempelkoden skapar en härledd tillgång med en justerad vy och `urlModifier` med godtyckliga värden `urlPostApplyModifier` . Svaret returnerar referensen till den nyligen härledda resursen.

**Begäran**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Svar**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```

