---
description: Används av MetadataField/type, saveMetadataFieldParam/fieldType och createMetadataField/fieldType.
solution: Experience Manager
title: Fälttyper för metadata
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# Fälttyper för metadata{#metadata-field-types}

Används av MetadataField/type, saveMetadataFieldParam/fieldType och createMetadataField/fieldType.

Syntax

## Värden {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Ett specialfall av  [!DNL `SingleFixedTag`] med en icke-ändringsbar ordlista som initierats till värden  [!DNL `True`] och  [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Noll eller flera strängvärden från en stängd ordlista. Det är bara administratörer som kan ändra ordlistan.
* [!DNL `MultiTag`]: Noll eller fler strängvärden.
* [!DNL `SingleFixedTag`]: Ett strängvärde från en stängd ordlista. Om `setAssetMetadata` eller `batchSetAssetMetadata` anropas med ett värde som inte finns i ordlistan returneras ett fel. Det är bara administratörer som kan ändra ordlistan.

* [!DNL `SingleTag`]: Ett strängvärde.
* [!DNL `String`]

