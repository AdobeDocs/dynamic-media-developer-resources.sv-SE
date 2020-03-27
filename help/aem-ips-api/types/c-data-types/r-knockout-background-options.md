---
description: Maskera (ursparning) bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. En valfri parameter som är inaktiverad som standard.
seo-description: Maskera (ursparning) bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. En valfri parameter som är inaktiverad som standard.
seo-title: BlockeraBakgrundAlternativ
solution: Experience Manager
title: BlockeraBakgrundAlternativ
topic: Scene7 Image Production System API
uuid: 1486d646-f42a-4ed4-9450-313950969c39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# BlockeraBakgrundAlternativ{#knockoutbackgroundoptions}

Maskera (ursparning) bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. En valfri parameter som är inaktiverad som standard.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## Parametrar {#section-3149b49ccb714e6eafa6655354816819}

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> hörn</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3">Markerar det hörn du vill arbeta med. <span class="codeph"> hörnet</span> accepterar följande värden: 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> UpperLeft</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> NederkantVänster</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> UpperRight</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> NederkantHöger</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerans</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3">En valfri inställning som tar bort tomt utrymme från bildkanter baserat på genomskinlighet. Accepterar ett värdeintervall från 0,0 till 1,0. Ange: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 om du vill matcha färgerna exakt. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 för att möjliggöra de största färgskillnaderna. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Styr pixelgenomskinlighet på den plats som anges av <span class="codeph"><span class="varname"> hörnvariabeln</span></span> . Dessa värden accepteras av <span class="codeph"> fillMethod</span> : </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>: Vrider alla pixlar i det angivna hörnet genomskinliga. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>: Vrider alla matchande pixlar genomskinliga oavsett plats. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## Används av {#section-28c43baafe85434a9ee9e303ed10569a}

Typen `KnockoutBackgroundOptions` används av:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

