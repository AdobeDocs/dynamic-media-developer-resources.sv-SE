---
description: Uppdaterar bildfältet som är associerat med en bildresurs.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Uppdaterar bildfältet som är associerat med en bildresurs.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| assetHandle | `xsd:string` | Resurshandtag. |
| [!DNL resolution] | `xsd:double` | Bildupplösning i pixlar per tum. |
| [!DNL anchorX] | `xsd:int` | Bildankarpunkt för X-axel. |
| [!DNL anchorY] | `xsd:int` | Bildankarpunkt för Y-axel. |
| [!DNL userData] | `xsd:string` | Värdet för `userData` metadatafält, som publiceras till den bild som används i katalogfältet för användardata. |
