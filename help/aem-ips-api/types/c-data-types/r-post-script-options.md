---
description: Alternativ för PostScript-filer.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

Alternativ för PostScript-filer.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| process | `xsd:string` | PostScript-processval. |
| upplösning | `xsd:double` | Filupplösning. |
| färgrymd | `xsd:string` | PostScript-färgmodell. |
| alpha | `xsd:boolean` | Om filen ska rastreras till en bild. I så fall skapas en genomskinlig bakgrund om originalfilen har definierats på det här sättet. Används vanligtvis för att skapa överlagrade logotyper. |
| extractSearchWords | `xsd:boolean` | Om sökord ska extraheras från PostScript-filen. |
