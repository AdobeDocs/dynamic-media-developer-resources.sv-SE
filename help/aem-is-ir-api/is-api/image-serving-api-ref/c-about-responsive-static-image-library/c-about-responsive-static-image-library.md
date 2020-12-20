---
description: Responsive Image Library är en JavaScript-modul som dynamiskt justerar kvaliteten på bilder som hanteras från Scene7 och bäddas in på responsiva webbsidor. Dessutom ger den bättre bildkvalitet på enheter med skärmar med hög densitet. Biblioteket kan även återge resultat från smart beskärning och smarta färgrutor på ett responsivt sätt.
seo-description: Responsive Image Library är en JavaScript-modul som dynamiskt justerar kvaliteten på bilder som hanteras från Scene7 och bäddas in på responsiva webbsidor. Dessutom ger den bättre bildkvalitet på enheter med skärmar med hög densitet. Biblioteket kan även återge resultat från smart beskärning och smarta färgrutor på ett responsivt sätt.
seo-title: Om bibliotek för responsiv bild
solution: Experience Manager
title: Om bibliotek för responsiv bild
topic: Scene7 Image Serving - Image Rendering API
uuid: 0906a940-59ff-45b0-b509-57bd02f2da57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# Om bibliotek för responsiv bild{#about-responsive-image-library}

Responsive Image Library är en JavaScript-modul som dynamiskt justerar kvaliteten på bilder som hanteras från Scene7 och bäddas in på responsiva webbsidor. Dessutom ger den bättre bildkvalitet på enheter med skärmar med hög densitet. Biblioteket kan även återge resultat från smart beskärning och smarta färgrutor på ett responsivt sätt.

## Demo-URL:er {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Det enklaste sättet att använda det responsiva bildbiblioteket är att definiera en lista med brytpunktsvärden för bildbredd. Den här listan ser till att rätt återgivning läses in och visas när en bild storleksändras på grund av att webbsidans layout ändras från att användaren ändrar storlek på webbläsarfönstret eller ändrar enhetens orientering. Biblioteket övervakar kontinuerligt skärmbildens storlek och varje gång en ny brytpunktsbredd nås hämtas en ny bildåtergivning från Scene7.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Demo-URL </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Följande är ett enkelt exempel där den responsiva bilden finns i en behållare som tar 50 % av webbsidans bredd. Varje gång webbläsarfönstret ändrar storlek ändras behållarbredden. När bildbredden når en av de konfigurerade brytpunkterna, som är inställda på 200, 400, 600 och 800 pixlar för illustrativa ändamål, hämtas och visas en ny återgivning. Målet är att undvika att läsa in stora bilder i onödan och spara bandbredd i nätverket. </p> <p>Klicka på webbadressen för att öppna webbsidan, ändra storlek på webbläsarfönstret och övervaka nätverkstrafiken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>I följande Bootstrap-exempel visas samma användningsfall på en webbsida. Enligt Bootstrap CSS kan layoutcellen som den responsiva bilden läggs till i ha någon av följande bredder: 360, 720 och 940 pixlar. Detta är de exakta värden som skickas som brytpunkter till det responsiva bildbiblioteket. Därför ser Scene7 till att klientens nätverksbandbredd används effektivt. Dessutom ser det till att bilden visas i exakt den storlek som behövs, med den aktuella webbsidans layout, utan att webbläsaren skalas. </p> <p>Klicka på webbadressen för att öppna webbsidan, ändra storlek på webbläsarfönstret för att hitta olika brytpunkter och övervaka nätverkstrafiken. </p> <p>Fler avancerade användningsområden är att associera olika bildförinställningar, eller bildservningskommandon, eller båda, med olika brytpunktsvärden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>I det här nästa exemplet används förinställningar av olika bildkvalitet och format för olika brytpunktsstorlekar. För en liten brytpunkt används en förinställning med låg kvalitet som tvingar bildservern att återge GIF-bilden komprimerad till endast sex färger. En medelstor brytpunkt använder en bildförinställning som är konfigurerad för JPEG med hög komprimering. Den största brytpunkten är associerad med en bildförinställning av hög kvalitet med förlustfri PNG. En sådan metod säkerställer att bilder av hög kvalitet levereras till sådana enheter, baserat på antagandet att enheter med större skärmar har större bandbredd och bearbetningskraft. </p> <p>Klicka på webbadressen för att öppna webbsidan, ändra storlek på webbläsarfönstret från större till mindre och se hur bildkvaliteten försämras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Förutom Bildförinställningar kan du koppla speciella bildserverkommandon till brytpunkter. I följande exempel visas hur det är möjligt att gradvis beskära banderollbilden till det intressanta området när skärmbildens storlek blir mindre. Här har den största brytpunkten inga bildserverkommandon alls, så banderollbilden är helt synlig. Vid medelbrytpunkt tillämpas måttlig beskärning, vilket gör att bara texten"Running" visas. Vid en liten brytpunkt tillämpas mer beskärning så att endast produkten visas. </p> <p>Klicka på webbadressen för att öppna webbsidan och ändra storlek på webbläsarfönstret. Lägg märke till hur bilden beskärs gradvis när du går från större till mindre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Du kan också använda kommandona Bildserver med Bildmallar för att styra vissa mallparametrar baserat på bildstorleken. I det här nästa exemplet används en bildservermall där teckensnittsstorleken för textövertäckningen parametriseras med parametern <span class="codeph"> $fontsize </span>. Responsiv bild är konfigurerad att använda en större teckenstorlek för mindre bildstorlekar för att säkerställa att texten alltid förblir läsbar: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Systemkrav {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Servermaskinvara och -programvara**

* Scene7 Image Serving 6.0.1 eller senare.

**Lägsta krav för klientwebbläsare**

* Microsoft® Windows® 7 eller senare; Mac OS X 10.8 eller senare.
* Firefox 23, Safari 6, Chrome 29, IE 9 eller senare.
* iOS 6 eller senare.
* Certifierad på iPhone3GS eller senare och iPad2 eller senare (endast inbyggda webbläsare).
* Android OS 2.3 eller senare.
* Internet Explorer på mobila enheter stöds inte för närvarande.

