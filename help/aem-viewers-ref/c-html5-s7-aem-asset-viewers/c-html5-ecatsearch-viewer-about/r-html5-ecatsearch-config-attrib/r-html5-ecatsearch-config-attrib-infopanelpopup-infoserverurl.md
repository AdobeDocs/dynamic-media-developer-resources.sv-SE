---
description: 'null'
seo-description: 'null'
seo-title: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 7af5e3d3-40c2-4f02-94e2-0314b698905d
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>URL-mallen för Info-servern används för att hämta nyckel/värde-par för variabelersättning i informationspanelens innehållsmall. Den angivna mallen innehåller vanligtvis makroplatshållare som ersätts med aktuella data innan begäran skickas till servern. </p> <p><span class="codeph"> $1$</span> ersätts med det rollover-värde som utlöste aktiveringen av <span class="codeph"> InfoPanelPopup</span> . </p> <p><span class="codeph"> $2$</span> ersätts med sekvensnumret för den aktuella bildrutan i bilduppsättningen. </p> <p><span class="codeph"> $3$</span> ersätts med det första sökvägselementet som anges i namnet på den överordnade uppsättningen för det aktuella objektet. Det motsvarar vanligtvis katalog-ID:t. </p> <p><span class="codeph"> $4$</span> ersätts med följande element i sökvägen och motsvarar resurs-ID:t. Den faktiska syntaxen för informationsserverbegäran är beroende av informationsservern och skiljer sig från server till server. Följande är till exempel en typisk mall för en Scene7-informationsserver: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tänk på att när du konfigurerar Info Panel-popup körs den HTML-kod och JavaScript-kod som skickas till Info-panelen på klientens dator. Kontrollera därför att sådan HTML-kod och JavaScript-kod är säkra.

## Egenskaper {#section-71356e3c13244e62b0582980d9d05328}

Valfritt.

## Standard {#section-22e9af803f724434807d34e200eb7518}

Ingen.

## Exempel {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
