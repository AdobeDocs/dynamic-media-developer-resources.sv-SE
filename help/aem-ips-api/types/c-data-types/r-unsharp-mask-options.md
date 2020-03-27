---
description: Inställningar som förbättrar bildskärpan för optimerade TIF-pyramidfiler.
seo-description: Inställningar som förbättrar bildskärpan för optimerade TIF-pyramidfiler.
seo-title: UnsharpMaskOptions
solution: Experience Manager
title: UnsharpMaskOptions
topic: Scene7 Image Production System API
uuid: 73073de0-41b6-471c-8887-f6b94ed2af90
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# UnsharpMaskOptions{#unsharpmaskoptions}

Inställningar som förbättrar bildskärpan för optimerade TIF-pyramidfiler.

`unsharpMaskOptions=[ *`mängd, radie, tröskelvärde, monokrom`*]`

## Parametrar {#section-c3f0d03136ba4422819cb463bd393885}

Ange ett värde för `unsharpMaskOptions` alternativ med `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Namn </th>
   <th colname="col2" class="entry"> Typ </th>
   <th colname="col3" class="entry"> Beskrivning </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> belopp</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:dubbel</span></td>
   <td colname="col3"><p>Styr kontrast som används på kantpixlar. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Intervall: 0.0 - 5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Standard: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> radie</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:dubbel</span></td>
   <td colname="col3"><p>Styr skärpan genom att ange antalet pixlar runt en bilds kant. Vilket värde som är korrekt beror på bildens storlek. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Intervall: 0.0 - 250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Med låga värden ökas skärpan endast för kantpixlar. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Höga värden gör ett bredare pixelband skarpare. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> tröskelvärde</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Avgör hur olika pixlar måste vara från det omgivande området innan de betraktas som kantpixlar och kan göras skarpare. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Intervall: 0 - 255 (endast heltal). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Standard: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monokrom</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Värdena är bara <span class="codeph"> 0</span> eller <span class="codeph"> 1</span> . </p><p>Ange <span class="codeph"> 0</span> för varje färgkomponent separat eller 1 <span class="codeph"></span> för endast bildens intensitet (intensitet). Lagermasken eller den sammansatta masken blir också skarpare. </p><p><span class="codeph"><span class="varname"> monokrom</span></span> ignoreras för gråskalebilder. </p></td>
  </tr>
 </tbody>
</table>

## Exempel {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Används av {#section-db8124a5468b498694a780f8a56a4560}

Typen `unsharpMaskOptions` används av:

* [ÅterbearbetaResurserJobb](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [API-referens för bildservering: op_usm](https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/http_ref/r_op_usm.html)

