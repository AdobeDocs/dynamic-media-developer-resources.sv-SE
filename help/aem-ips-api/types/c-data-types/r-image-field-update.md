---
description: Uppdaterar bildfältet som är associerat med en bildresurs.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# ImageFieldUpdate{#imagefieldupdate}

Uppdaterar bildfältet som är associerat med en bildresurs.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Resurshandtag. |
| `*`upplösning`*` | `xsd:double` | Bildupplösning i pixlar per tum. |
| `*`anchorX`*` | `xsd:int` | Bildankarpunkt för X-axel. |
| `*`anchorY`*` | `xsd:int` | Bildankarpunkt för Y-axel. |
| `*`userData`*` | `xsd:string` | Värdet för metadatafältet `userData`, som publiceras till den bild som används i katalogfältet för användardata. |

