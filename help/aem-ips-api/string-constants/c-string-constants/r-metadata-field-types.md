---
description: Används av MetadataField/type, saveMetadataFieldParam/fieldType och createMetadataField/fieldType.
solution: Experience Manager
title: Fälttyper för metadata
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
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
