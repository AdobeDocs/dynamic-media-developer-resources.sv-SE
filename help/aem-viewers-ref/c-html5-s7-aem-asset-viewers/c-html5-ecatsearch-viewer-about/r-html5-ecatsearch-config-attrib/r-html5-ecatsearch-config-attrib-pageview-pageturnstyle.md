---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthDelderColorDelerOpacityborderOnOffborderColorFillColor`*`]

Styr komponentens utseende när [!DNL `PageView.frametransition`] är [!DNL `turn`] eller [!DNL `auto`] på skrivbordssystem.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Bredden i pixlar på skuggan för sidavgränsaren som skiljer de vänstra och högra sidorna på uppslaget åt. Den styr också bredden på den skugga som körs bredvid den vändande sidan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> Skuggfärgen i RRGGBB-format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>Skuggopaciteten i intervallet <span class="codeph"> 0</span> till <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Flagga (antingen <span class="codeph"> 0</span> eller <span class="codeph"> 1</span>) som aktiverar och inaktiverar kanten på den vänstra sidan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Kantfärgen i RRGGBB-format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Färgen på den heltäckande fyllningen i komponentområdet som används vid sidvändningsanimering, i RRGGBB-format. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-54c634116cfe4f17813318e07539264c}

Valfritt.

## Standard {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Exempel {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
