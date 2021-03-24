---
description: Alternativ för PostScript-filer.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---


# PostScriptOptions{#postscriptoptions}

Alternativ för PostScript-filer.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`process`*` | `xsd:string` | PostScript-processval. |
| `*`upplösning`*` | `xsd:double` | Filupplösning. |
| `*`färgrymd`*` | `xsd:string` | PostScript-färgmodell. |
| `*`alpha`*` | `xsd:boolean` | Om filen ska rastreras till en bild. I så fall skapas en genomskinlig bakgrund om originalfilen har definierats på det här sättet. Används vanligtvis för att skapa överlagrade logotyper. |
| `*`extractSearchWords`*` | `xsd:boolean` | Om sökord ska extraheras från PostScript-filen. |

