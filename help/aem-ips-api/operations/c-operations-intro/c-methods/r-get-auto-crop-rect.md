---
description: Returnerar ett beskuret område för en bild baserat på dess bakgrundsfärg eller genomskinlighet.
seo-description: Returnerar ett beskuret område för en bild baserat på dess bakgrundsfärg eller genomskinlighet.
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
topic: Scene7 Image Production System API
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# getAutoCropRect{#getautocroprect}

Returnerar ett beskuret område för en bild baserat på dess bakgrundsfärg eller genomskinlighet.

Syntax

## Auktoriserade användartyper {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Indata (getAutoCropRectParam)**

>[!NOTE]
>
>Ange antingen ` *`autoColorCropOptions`*` eller ` *`autoTransparentCropOptions`*` när du anropar den här metoden.

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med den resurs du vill arbeta med. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Referensen till resursen som du vill arbeta med. |
| ` *`autoColorCropOptions`*` | `types:AutoColorCropOptions` | Nej | Beräkna beskärningsrektangeln baserat på färg. Se [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| ` *`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | Nej | Beräkna beskärningsrektangeln baserat på genomskinlighet. Se [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Utdata (getAutoCropRectReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`xOffset`*` | `xsd:int` | Ja | Den inledande pixelkoordinaten för det beräknade beskärningsområdet. |
| ` *`yOffset`*` | `xsd:int` | Ja | Den inledande pixelkoordinaten för det beräknade beskärningsområdet. |
| ` *`width`*` | `xsd:int` | Ja | Bredden på det beräknade beskärningsområdet (i pixlar). |
| ` *`height`*` | `xsd:int` | Ja | Höjden på det beräknade beskärningsområdet (i pixlar). |

## Exempel {#section-ba65bd66086d491cad1cea535954ee1f}

**Begäran**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Svar**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentBeskärningsalternativ](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

