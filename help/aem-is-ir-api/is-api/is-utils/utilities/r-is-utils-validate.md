---
description: Verktyg för bildvalidering. Detta kommandoradsverktyg verifierar bildfilerna för att säkerställa att de är giltiga och kan läsas utan problem med Image Serving.
seo-description: Verktyg för bildvalidering. Detta kommandoradsverktyg verifierar bildfilerna för att säkerställa att de är giltiga och kan läsas utan problem med Image Serving.
seo-title: validera
solution: Experience Manager
title: validera
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# validera{#validate}

Verktyg för bildvalidering. Detta kommandoradsverktyg verifierar bildfilerna för att säkerställa att de är giltiga och kan läsas utan problem med Image Serving.

Alla icke-PTIFF-bildfiler måste valideras innan filen blir tillgänglig för Image Serving som källbild. PTIFF-bilder bör valideras efter potentiellt otillförlitliga kopieringsåtgärder.

## Användning {#usage}

` validate *``* [ *``*] [ *`fileTypeOptionsSourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>Källfiltyp; minst en måste anges (-any tillåter samma bildfiltyper som stöds av IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> alternativ  </span> </span> </p> </td> 
  <td class="stentry"> <p>Andra kommandoalternativ (se nedan). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> Bildfil. Inget eller flera, avgränsade med blanksteg. </p> </td> 
 </tr> 
</table>

## Returnerar {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 om det lyckas. Om ett fel inträffar returneras ett värde som inte är noll och felinformation skickas till `stderr`.

## Alternativ {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>Anger en separat textfil som innehåller listan med bildfiler. En post per fil. Om <span class="codeph"> -fileList </span> ingår får <span class="varname"> sourceFile </span> inte anges. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>Aktiverar verifiering av hela bildfilen. Som standard valideras endast bildhuvudet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>Verifierar att den inbäddade färgprofilen är giltig. Som standard är inte profibrödtexten markerad. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> Avvisar bilder med 16 bitar per bildkomponent. Anges alltid av Image Server när fjärrkällbilder valideras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> Skriver ut mer information om bilden är ogiltig. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p>Inaktiverar <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>-utdata. Endast en status returneras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>Avbryter bearbetningen när ett filvalideringsfel inträffar, även om ytterligare filer ännu inte har validerats. Som standard fortsätter bearbetningen när ett valideringsfel inträffar </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  </span> </p> </td> 
  <td class="stentry"> <p>Returnerar versionsinformation för det här verktyget. Ange utan andra alternativ. </p> </td> 
 </tr> 
</table>

