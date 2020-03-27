---
description: Använd PDF-jobbalternativ. En jobbalternativfil eller PDF-förinställning är en fil som genereras av Illustrator i dialogrutan Spara som PDF-alternativ eller PDF-förinställningar i InDesign.
seo-description: Använd PDF-jobbalternativ. En jobbalternativfil eller PDF-förinställning är en fil som genereras av Illustrator i dialogrutan Spara som PDF-alternativ eller PDF-förinställningar i InDesign.
seo-title: joboption
solution: Experience Manager
title: joboption
topic: Scene7 Image Serving - Image Rendering API
uuid: 7288cf29-850f-4121-8425-5f995daac22d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# joboption{#joboption}

Använd PDF-jobbalternativ. En jobbalternativfil eller PDF-förinställning är en fil som genereras av Illustrator i dialogrutan Spara som PDF-alternativ eller PDF-förinställningar i InDesign.

` joboption= *`value`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> värde</span></span> </p> </td> 
  <td class="stentry"> <p>IPSID för jobbalternativsfilen. </p></td> 
 </tr> 
</table>

Jobbalternativfilen kan laddas upp och publiceras av IPS/SPS. PDF-alternativen i jobbalternativsfilen används när PDF-filen genereras.

Följande alternativ stöds för närvarande:

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Allmänt </p></td> 
  <td class="stentry"> <p> Kompatibilitet </p> <p> Objektnivåkomprimering </p> <p> Bädda in miniatyrer </p> <p> Optimera för snabb webbvisning </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Bilder </p></td> 
  <td class="stentry"> <p> Nedsampla, Upplösning, Tröskelvärde och Komprimering för färg, grått och mono </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Teckensnitt </p></td> 
  <td class="stentry"> <p> Bädda in alla teckensnitt </p> <p> Bädda in OpenType-teckensnitt </p> <p> Skapa delmängder av inbäddade teckensnitt när andelen tecken som används är mindre än: </p> <p> Inkludera alltid lista </p> <p> Inkludera aldrig lista </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Färg </p></td> 
  <td class="stentry"> <p> Färgstrategi (tagga endast bilder behandlas som tagga allt) </p> <p> Dokumentåtergivningsmetod </p> <p> Endast följande arbetsfärgrymder stöds i 4.2.5. </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB med kodningsintervall [-4.0, 4.0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> Platt XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">Linjär ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8-bitars </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-YCC 8-bitars </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">Grå <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">Grå gamma 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">Grå gamma 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">Punktförstoring 10 % </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">Punktförstoring 15 % </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">Punktförstoring 20 % </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> Punktförstoring 25 % </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">Punktförstoring 30 % </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> Bevara CMYK-värden för kalibrerade CMYK-färgmodeller </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Avancerat </p></td> 
  <td class="stentry"> <p>Bevara OPI-kommentarer är alltid aktiverat. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Standarder </p></td> 
  <td class="stentry"> <p>Kompatibilitetsstandard. </p></td> 
 </tr> 
</table>

