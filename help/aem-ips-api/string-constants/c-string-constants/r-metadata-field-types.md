---
description: Används av MetadataField/type, saveMetadataFieldParam/fieldType och createMetadataField/fieldType.
seo-description: Används av MetadataField/type, saveMetadataFieldParam/fieldType och createMetadataField/fieldType.
seo-title: Fälttyper för metadata
solution: Experience Manager
title: Fälttyper för metadata
topic: Dynamic Media Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '107'
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

