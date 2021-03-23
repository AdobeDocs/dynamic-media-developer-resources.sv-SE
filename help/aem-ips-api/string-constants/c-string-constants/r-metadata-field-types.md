---
description: Används av MetadataField/type, saveMetadataFieldParam/fieldType och createMetadataField/fieldType.
seo-description: Används av MetadataField/type, saveMetadataFieldParam/fieldType och createMetadataField/fieldType.
seo-title: Fälttyper för metadata
solution: Experience Manager
title: Fälttyper för metadata
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
feature: Dynamic Media Classic,SDK/API,Metadata
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
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

