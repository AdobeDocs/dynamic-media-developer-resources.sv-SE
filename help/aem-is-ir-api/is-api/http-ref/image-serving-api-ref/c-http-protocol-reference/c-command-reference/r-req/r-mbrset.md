---
description: Multibithastighetsdata.
seo-description: Multibithastighetsdata.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# mbrSet{#mbrset}

Multibithastighetsdata.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingFmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> kodning</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Returnerar ett text- eller xml-svar som innehåller en lista med URL:er (och motsvarande bithastighet) som motsvarar giltiga videoposter i videouppsättningen som är kopplad till nettosökvägs-ID.

Det tidigare kravet på att en giltig videopost innehåller ett värde för `catalog::VideoBitRate` har nu förenklats. Posten kan innehålla ett värde för `catalog::VideoBitRate`*eller* `catalog::AudioBitRate`*eller* `catalog::TotalStreamBitRate`. Endast ett av dessa måste definieras för att videoposten ska vara giltig. Observera att kraven för `catalog::Path` och ett giltigt videofiltillägg inte har ändrats.

Svaren är avsedda att användas av Apple- och Flash Streaming Servers och uppfyller därför strukturellt dessa specifikationer. URL:er genereras med prefix `attribute::HttpAppleStreamingContext` och `attribute::HttpFlashStreamingContext`.

m3u8-svar innehåller bara mp4-filer om det finns några i videouppsättningen. Om det inte finns några mp4-filer innehåller svaren bara f4v-filer. Om det inte finns några mp4-filer eller f4v-filer är svaret tomt.

f4m-svar innehåller bara f4v-filer om det finns några i videouppsättningen. Om det inte finns några f4v-filer innehåller svaren bara mp4-filer. Om det inte finns några f4v-filer eller mp4-filer är svaret tomt.

Bithastigheter som visas i f4m/m3u8-svar motsvarar värdena i `catalog::TotalStreamBitRate` (konverteras till lämpliga enheter). Om `catalog::TotalStreamBitRate` inte har definierats används summeringen av `catalog::VideoBitRate` och `catalog::AudioBitRate`.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::NonImgExpiration`.
