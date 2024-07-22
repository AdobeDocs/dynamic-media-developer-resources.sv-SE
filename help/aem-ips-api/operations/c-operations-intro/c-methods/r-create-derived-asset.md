---
description: Skapar en ny resurs som härletts från en befintlig primär källbildresurs.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# createDerivedAsset{#createderivedasset}

Skapar en ny resurs som härletts från en befintlig primär källbildresurs.

Syntax

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Härledda resurser anger Image Server-protokollkommandon som ändrar representationen av ägarbilden. Med den härledda typen `AdjustedView` kan du göra enkla ändringar i en enskild bild (till exempel genom att ange en beskärningsrektangel), medan `LayerView` hjälper dig att skapa en vy med flera lager som kan innehålla text eller ytterligare bilder.

Till skillnad från en bildkopia (se [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)) länkas en härledd bild till sin ägarbild. Ändringar av ägarbilden ändrar associerade härledda resurser. Om du tar bort ägarbilden tas alla associerade härledda bilder bort.

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
| companyHandle | `xsd:string` | Ja | Handtaget till det företag som innehåller den tillgång som du härleder den nya tillgången från. |
| ownerHandle | `xsd:string` | Ja | Handtaget till den primära bildresurs som den nya bilden kommer från. |
| folderHandle | `xsd:string` | Ja | Referensen till mappen där den nya härledda resursen skapas. |
| name | `xsd:string` | Ja | Namnet på den härledda tillgången. |
| type | `xsd:string` | Ja | Tillgångstypen för den nya härledda resursen: `AdjustedView` eller `LayerView`. |
| urlModifier | `xsd:string` | Nej | Avbildningsservning eller bildåtergivningsprotokollkommandon tillämpade *före* begäran eller `urlPostApplyModifier` kommandon. |
| urlPostApplyModifier | `xsd:string` | Nej | Avbildningsservning eller bildåtergivningsprotokollkommandon som har använts *efter* på begäran eller `urlPostApplyModifier` kommandon. |

**Utdata (createDerivedAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Referensen till den härledda tillgången. |

## Exempel {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

Exempelkoden skapar en härledd resurs med en justerad vy och `urlModifier` och `urlPostApplyModifier` med godtyckliga värden. Svaret returnerar referensen till den nyligen härledda resursen.

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
