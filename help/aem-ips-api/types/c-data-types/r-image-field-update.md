---
description: Uppdaterar bildfältet som är associerat med en bildresurs.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# ImageFieldUpdate{#imagefieldupdate}

Uppdaterar bildfältet som är associerat med en bildresurs.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| assetHandle | `xsd:string` | Resurshandtag. |
| upplösning | `xsd:double` | Bildupplösning i pixlar per tum. |
| anchorX | `xsd:int` | Bildankarpunkt för X-axel. |
| anchorY | `xsd:int` | Bildankarpunkt för Y-axel. |
| userData | `xsd:string` | Värdet för `userData` metadatafält, som publiceras till den bild som används i katalogfältet för användardata. |
