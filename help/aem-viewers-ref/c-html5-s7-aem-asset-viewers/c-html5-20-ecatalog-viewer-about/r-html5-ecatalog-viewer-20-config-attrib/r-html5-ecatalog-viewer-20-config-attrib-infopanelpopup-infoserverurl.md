---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>URL-mallen för Info-servern används för att hämta nyckel/värde-par för variabelersättning i informationspanelens innehållsmall. Den angivna mallen innehåller vanligtvis makroplatshållare som ersätts med aktuella data innan begäran skickas till servern. </p> <p><span class="codeph"> $1$</span> ersätts med det rollover-värde som utlöste aktiveringen av <span class="codeph"> InfoPanelPopup </span> . </p> <p><span class="codeph"> $2$</span> ersätts med sekvensnumret för den aktuella bildrutan i bilduppsättningen. </p> <p><span class="codeph"> $3$</span> ersätts med det första sökvägselementet som anges i namnet på den överordnade uppsättningen för det aktuella objektet. Det motsvarar vanligtvis katalog-ID:t. </p> <p><span class="codeph"> $4$</span> ersätts med följande element i sökvägen och motsvarar resurs-ID:t. Den faktiska syntaxen för informationsserverbegäran är beroende av informationsservern och skiljer sig från server till server. Följande är till exempel en typisk Dynamic Media Info Server-begärandemall: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>När du konfigurerar popup-rutan för panelen Info körs HTML-koden och JavaScript-koden som skickas till panelen Info på klientens dator. Se därför till att sådan HTML-kod och JavaScript-kod är säkra.

## Egenskaper {#section-71356e3c13244e62b0582980d9d05328}

Valfritt.

## Standard {#section-22e9af803f724434807d34e200eb7518}

Ingen.

## Exempel {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
