---
description: Överföringsinställning för att bearbeta ZIP- och TAR-filer som primära resurser (ingen) eller för att extrahera och överföra deras innehåll (UnCompress).
seo-description: Överföringsinställning för att bearbeta ZIP- och TAR-filer som primära resurser (ingen) eller för att extrahera och överföra deras innehåll (UnCompress).
seo-title: AvkomprimeraAlternativ
solution: Experience Manager
title: AvkomprimeraAlternativ
topic: Scene7 Image Production System API
uuid: 1e6827db-8c5e-47db-b7ff-4e681e107e57
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# UnCompressOptions{#uncompressoptions}

Överföringsinställning för att bearbeta ZIP- och TAR-filer som primära resurser (ingen) eller för att extrahera och överföra deras innehåll (UnCompress).

>[!NOTE]
>
>`None` är standard.

## Parametrar {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> process</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Kontrollerar arkiveringsfilbearbetning för ZIP och TAR. Tillhandahåller två alternativ: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> Inget:</span> Bearbeta som primära resurser. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> UnCompress:</span> Extrahera och bearbeta innehåll. </li>
     </ul><p>Obs! Strängkonstanter är skiftlägeskänsliga. Använd <span class="codeph"> UnCompress</span>, inte <span class="codeph"> uncompress</span> eller <span class="codeph"> unCompress</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Används av {#section-b2a829cf5511412e968bb2000f85cc31}

Typen `unCompressionOptions` används av:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

