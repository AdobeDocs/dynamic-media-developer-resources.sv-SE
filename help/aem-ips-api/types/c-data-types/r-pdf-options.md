---
description: Filalternativ för PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# [!DNL PDFOptions]{#pdfoptions}

Filalternativ för PDF.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| process | `xsd:string` | Val av&quot;PDF-processer&quot;. |
| upplösning | `xsd:double` | Filupplösning. |
| färgrymd | `xsd:string` | Färgrymdsval efter skript. |
| pdfCatalog | `xsd:boolean` | Om en sida med flera PDF ska kombineras i en e-katalog efter återgivningen (standardvärdet är true). |
| extractSearchWords | `xsd:boolean` | Om sökord ska extraheras från filen PDF. |
| extractLinks | `xsd:boolean` | Om PDF-länkar ska extraheras till bildscheman som tilldelats de rastrerade sidorna i IPS. |
