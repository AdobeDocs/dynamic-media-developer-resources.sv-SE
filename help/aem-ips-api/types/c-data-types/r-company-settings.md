---
description: Företagsspecifika konfigurationsinställningar.
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---

# CompanySettings{#companysettings}

Företagsspecifika konfigurationsinställningar.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| overwriteMode | `xsd:string` | Avgör om bilder i den aktuella mappen ska skrivas över med samma basbildnamn och tillägg. |
| keepPublishState | `xsd:boolean` | Anger om en ersättningsbild som överförts till IPS ska behålla den befintliga inställningen&quot;Klart för publicering&quot; eller om den ska vara som anges i överföringen. |
| defaultSourceProfile | `types:Asset` | Anger standardfärgprofilen för källan (Coated FOGRA27 (ISO 126472:2004)) som automatiskt används som en del av&quot;Använd standardfärgbeteende&quot; när CMYK-bildfiler läggs till. |
| defaultDisplayProfile | `types:Asset` | Anger den interna standardfärgprofilen (U.S. Web Coated (SWOP) v2) som används automatiskt som en del av &quot;Use default Color Behavior&quot; när CMYK-bildfiler läggs till. |
| iptcExifMappingXslt | `types:Asset` | Extraheringen av IPTC- och EXIF-bildrubriksdata till IPS kräver konvertering från interna fältnamn till användardefinierade fältnamn för företaget. Avgör en XSL-översättningstabell (standard är &quot;Extrahera inte IPTC- eller EXIF-fält&quot;) för överförda bilder. |
| xmpMappingXslt | `types:Asset` | Extraheringen av XMP bildrubriksdata till IPS kräver konvertering från interna fältnamn till användardefinierade fältnamn för företaget. Avgör en XSL-översättningstabell (standard är &quot;Extrahera inte några XMP fält&quot;) för överförda bilder. |
| discSpaceWarningMin | `xsd:int` | Minsta mängd ledigt utrymme i bildkatalogen innan en varning skickas ut. |
| emailTrashCleanupWarning | `xsd:boolean` | Avgör om e-post ska skickas innan objekt som placeras i papperskorgen kan tas bort automatiskt. |
| javascriptUploadEnabled | `types:Asset` | Avgör om JavaScript-filer ska överföras. Detta är en potentiell säkerhetsrisk, så använd detta alternativ med försiktighet. |
