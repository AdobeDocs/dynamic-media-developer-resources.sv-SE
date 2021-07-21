---
description: Alternativ för PDF-filer.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# PDFOptions{#pdfoptions}

Alternativ för PDF-filer.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`process`*` | `xsd:string` | Val av&quot;PDF-processer&quot;. |
| `*`upplösning`*` | `xsd:double` | Filupplösning. |
| `*`färgrymd`*` | `xsd:string` | Färgrymdsval efter skript. |
| `*`pdfCatalog`*` | `xsd:boolean` | Om en PDF-fil med flera sidor ska kombineras i en e-katalog efter återgivningen (standardvärdet är true). |
| `*`extractSearchWords`*` | `xsd:boolean` | Om sökord ska extraheras från PDF-filen. |
| `*`extractLinks`*` | `xsd:boolean` | Om PDF-länkar ska extraheras till bildscheman som tilldelats de rastrerade sidorna i IPS. |
