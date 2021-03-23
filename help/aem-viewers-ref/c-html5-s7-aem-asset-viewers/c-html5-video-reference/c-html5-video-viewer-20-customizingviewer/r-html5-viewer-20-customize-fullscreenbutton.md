---
description: Helskärmsknappen gör att videospelaren övergår till eller avslutar helskärmsläget när en användare klickar på den.
seo-description: Helskärmsknappen gör att videospelaren övergår till eller avslutar helskärmsläget när en användare klickar på den.
seo-title: Helskärmsknapp
solution: Experience Manager
title: Helskärmsknapp
uuid: c6b90158-8658-49f1-86c3-c3dd00fe9070
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# Helskärmsknapp{#full-screen-button}

Helskärmsknappen gör att videospelaren övergår till eller avslutar helskärmsläget när en användare klickar på den.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Du kan ändra storlek, skal och position för helskärmsknappen, i förhållande till kontrollfältet som innehåller den, enligt CSS.

Utseendet på helskärmsknappen styrs av CSS-klassväljaren:

```
.s7videoviewer .s7fullscreenbutton
```

**CSS-egenskaper för helskärmsknappen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Placera från den övre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger  </span> </p> </td> 
   <td colname="col2"> <p> Placera från den högra kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster  </span> </p> </td> 
   <td colname="col2"> <p> Placera från den vänstra kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den nedre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på helskärmsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjden på helskärmsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Den bild som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder både attributväljarna `state` och `selected`, som kan användas för att tillämpa olika skal på olika knapplägen. `selected='true'` motsvarar i synnerhet helskärmsläget och `selected='false'` motsvarar normalläget.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Om du vill ställa in en helskärmsknapp som är 32 x 32 pixlar och placerad 6 pixlar från kontrollfältets övre och högra kant. Du kan även visa olika bilder för vart och ett av de fyra olika knapplägena när du markerar dem eller inte markerar dem.

```
.s7videoviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

