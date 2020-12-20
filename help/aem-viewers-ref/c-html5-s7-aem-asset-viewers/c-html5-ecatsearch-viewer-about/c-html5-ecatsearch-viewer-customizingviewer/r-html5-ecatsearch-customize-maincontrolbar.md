---
description: Huvudkontrollfältet är det rektangulära området på stationära datorer och surfplattor som innehåller alla gränssnittskontroller (utom knapparna Stora sidor) som är tillgängliga för visningsprogrammet för eCatalog Search.
seo-description: Huvudkontrollfältet är det rektangulära området på stationära datorer och surfplattor som innehåller alla gränssnittskontroller (utom knapparna Stora sidor) som är tillgängliga för visningsprogrammet för eCatalog Search.
seo-title: Huvudkontrollfält
solution: Experience Manager
title: Huvudkontrollfält
topic: Dynamic media
uuid: 21b6e6cd-115f-4c7b-a61e-34b307142045
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---


# Huvudkontrollfält{#main-control-bar}

Huvudkontrollfältet är det rektangulära området på stationära datorer och surfplattor som innehåller alla gränssnittskontroller (utom knapparna Stora sidor) som är tillgängliga för visningsprogrammet för eCatalog Search.

På mobiltelefoner behåller den fortfarande knapparna Miniatyrbilder, Innehållsförteckning, Hämta, Skriv ut, Favoriter, Delning för sociala medier, Helskärm och Stäng. Knapparna Första sidan och Sista sidan samt Sidindikatorn tas bort från huvudkontrollfältet och läggs till i det sekundära kontrollfältet i stället. Som standard visas huvudkontrollfältet längst upp i visningsområdet på datorer och mobiltelefoner, och flyttas längst ned i visningsområdet på surfplattor. Hela den tillgängliga visningsprogrambredden används alltid. Det går att ändra färgen, höjden och den lodräta positionen i CSS i förhållande till visningsprogrammets behållare.

Utseendet på huvudkontrollfältet styrs av följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Placera högst upp i visningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p>Placera längst ned i visningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Huvudkontrollfältets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Huvudkontrollfältets bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel**  - för att ställa in ett grått huvudkontrollfält som är 36 pixlar högt och placerat högst upp i visningsbehållaren.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

Huvudkontrollfältet har stöd för en valfri rullningsfunktion. Den aktiveras om visningsprogrammets bredd är för liten och det inte finns tillräckligt med utrymme för att alla knappförinställningar i kontrollfältet ska få plats. I det här fallet visas en dubbellägesknapp till höger om kontrollfältet. Om du klickar eller trycker på den här knappen rullas alla element i kontrollfältet åt vänster eller höger, beroende på rullningsknappens läge. Det primära användningsområdet för den här funktionen är mobila enheter med små skärmar i stående orientering.

Rullningsfunktionen är aktiverad för huvudkontrollfältet och inaktiverad för det sekundära kontrollfältet. Funktionen aktiveras och inaktiveras med följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>När den är inställd på <span class="codeph"> static </span> är rullningsfunktionen inaktiverad. </p> <p>Ställ in den här egenskapen på <span class="codeph"> absolut </span> för att aktivera rullningsfunktionen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rullningsknappen läggs till i ett särskilt behållarelement som placerar knappen korrekt och där du kan formatera området runt knappen på ett annat sätt än resten av kontrollfältets bakgrund om rullningsknappens höjd är mindre än kontrollfältets höjd.

Utseendet på den här rullningsknappbehållaren styrs av följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Normalt ska vara lika med eller större än bredden på själva rullningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Behållarens bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Du kan ändra storlek och skal på själva rullningsknappen med hjälp av CSS.

Utseendet på den här knappen styrs av följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljarna `state` och `selected`, som kan användas för att tillämpa olika skal på olika knapplägen. `state="selected"` motsvarar i synnerhet det inledande rullningsknappläget när det är möjligt att rulla innehållet i kontrollfältet åt vänster, `state="default"` motsvarar läget när innehållet rullas hela vägen till vänster och rullningsknappen föreslår att det återgår till det ursprungliga läget.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

**Exempel**  - för att aktivera rullningsfunktionen i huvudkontrollfältet för mobiltelefoner och ställa in en rullningsknapp som är 64 x 64 pixlar som visar olika bilder för de fyra olika knapplägena när de är markerade eller inte är markerade:

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

