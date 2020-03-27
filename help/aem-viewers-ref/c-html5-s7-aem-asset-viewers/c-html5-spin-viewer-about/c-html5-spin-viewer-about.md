---
description: Snurra visningsprogram är ett bildvisningsprogram som ger en 360-gradersvy av bilden eller till och med flerdimensionell vy om rätt snurruppsättning används. Den har verktyg för zoomning och snurra, stöd för helskärmsläge och en valfri stängningsknapp. Den är utformad för att fungera på stationära datorer och mobila enheter.
keywords: responsive
seo-description: Snurra visningsprogram är ett bildvisningsprogram som ger en 360-gradersvy av bilden eller till och med flerdimensionell vy om rätt snurruppsättning används. Den har verktyg för zoomning och snurra, stöd för helskärmsläge och en valfri stängningsknapp. Den är utformad för att fungera på stationära datorer och mobila enheter.
seo-title: Snurra
solution: Experience Manager
title: Snurra
topic: Dynamic media
uuid: 5d5cdf83-cfe8-48cd-af74-b270f7400b14
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Snurra{#spin}

Snurra visningsprogram är ett bildvisningsprogram som ger en 360-gradersvy av bilden eller till och med flerdimensionell vy om rätt snurruppsättning används. Den har verktyg för zoomning och snurra, stöd för helskärmsläge och en valfri stängningsknapp. Den är utformad för att fungera på stationära datorer och mobila enheter.

>[!NOTE]
>
>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet.

Visningstyp 503.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400)

## Använda Spin Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Spin Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-fil innehåller alla SDK-komponenter för visningsprogrammet som används av det här visningsprogrammet, resurser, CSS) som hämtats av visningsprogrammet under körning.

Snurra visningsprogram kan användas både i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer eller i inbäddat läge, där den integreras med målwebbsidan med dokumenterat API.

Konfigurationen och skalningen liknar den för andra visningsprogram. All skalning kan göras via anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensamma för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med Spin Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Snurra visningsprogram har stöd för följande pekgester som är vanliga i andra mobilprogram. När visningsprogrammet inte kan bearbeta en användares dragningsgest vidarebefordrar det händelsen till webbläsaren för att utföra en inbyggd sidbläddring. Detta gör att användaren kan navigera på sidan även om användaren upptar större delen av enhetens skärmområde.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesture </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dubbelknacka </p> </td> 
   <td colname="col2"> <p> Zoomar in en nivå tills maximal förstoring nås. Nästa dubbelknackningsgest återställer visningsprogrammet till det inledande visningsläget. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Knipning </p> </td> 
   <td colname="col2"> <p>Zoomar in eller ut i bilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vågrät dragning eller snärtning </p> </td> 
   <td colname="col2"> <p> Om bilden är i ett återställningsläge snurrar den vågrätt genom den angivna uppsättningen. </p> <p> Om bilden zoomas in flyttas den vågrätt. Om bilden flyttas till vykanten och en svepning fortfarande utförs i den riktningen utför gesten en inbyggd sidrullning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lodrät dragning eller snärtning </p> </td> 
   <td colname="col2"> <p> Om bilden är i ett återställningsläge ändras den lodräta vyvinkeln om en flerdimensionell snurruppsättning används. I en endimensionell snurra, eller när en flerdimensionell snurra är på den sista eller första axeln, så att den lodräta svepningen inte resulterar i en vertikal vinkeländring, utför gesten en en inbyggd sidrullning. </p> <p> Om bilden är inzoomad flyttas den vertikalt. Om bilden flyttas till vykanten och en svepning fortfarande utförs i den riktningen utför gesten en inbyggd sidrullning. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Visningsprogrammet har också stöd för både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Visningsprogrammet är fullt åtkomligt via tangentbordet.

Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in Spin Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en länk som, när användaren klickar på den, öppnar visningsprogrammet i ett separat webbläsarfönster. I andra fall är det nödvändigt att bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup-fönster, inbäddning i fast storlek och responsiv designinbäddning.

**Om popup-läge**

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändrar storlek eller om en mobilenhets orientering ändras.

Popup-läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med hjälp av `window.open()` JavaScript-anrop, korrekt konfigurerade `A` HTML-element eller någon annan lämplig metod.

Vi rekommenderar att du använder en körklar HTML-sida för popup-åtgärder. I det här fallet anropas den [!DNL SpinViewer.html] och finns i undermappen [!DNL html5/] för din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Du kan anpassa visuellt genom att använda anpassad CSS.

Följande är ett exempel på HTML-kod som öppnar visningsprogrammet i ett nytt fönster:

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet tar normalt bara upp en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designsidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här är det bästa alternativet för webbsidor som har en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet kan behöva ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`utan begränsningar, väljer visningsprogrammet automatiskt dess höjd enligt proportionerna för den resurs som används. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor som använder responsiva designlayoutramverk som Bootstrap, Foundation och så vidare.

Om webbsidan ställer in både bredd och höjd för visningsprogrammets behållare `DIV`fyller visningsprogrammet bara det området och följer den storlek som webbsidans layout ger. Ett bra exempel kan vara att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till Spin Viewer på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i HTML-huvudet. Innan du kan använda visningsprogrammets API måste du ta med `SpinViewer.js`. `SpinViewer.js` finns under undermappen till [!DNL html5/js/] din standarddistribution av IS-Viewer:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Scene7-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Scene7-servrarna som har IS-Viewer installerat.

   Den relativa sökvägen ser ut så här:

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Du bör bara referera till JavaScript- `include` filen för huvudvisningsprogrammet på sidan. Du bör inte referera till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körningen. Referera inte direkt till HTML5 SDK- `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökvägen (så kallad konsoliderad SDK `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversioner. Adobe sparar inte äldre versioner av sekundära visningsprogram `includes` på servern.
   >
   >
   >Det innebär att om du skickar en direkt referens till ett sekundärt JavaScript `include` som används av visningsprogrammet på sidan så bryts visningsprogrammets funktion i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API.

   Platshållarens DIV är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att antingen deklarera den för CSS-klassen på den `.s7spinviewer` översta nivån i absoluta enheter eller genom att använda `stagesize` modifierare.

   Du kan ange storlek i CSS direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som sedan tilldelas en förinställningspost för visningsprogrammet i Scene7 Publishing System, eller skickas explicit med ett formatkommando.

   Mer information om hur du formaterar visningsprogrammet med CSS finns i [Anpassa Spin Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) .

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på HTML-sidan:

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Du kan ställa in modifieraren antingen i visningsprogrammets förinställningspost i Scene7 Publishing System, eller skicka den explicit med visningsprogrammets initieringskod med `stagesize` `params` samling, eller som ett API-anrop enligt beskrivningen i avsnittet Command Reference, enligt följande:

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.SpinViewer` klassen, skickar all konfigurationsinformation till konstruktorn och anropar `init()` metoden för en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet har minst `containerId` ett fält som innehåller namnet på visningsbehållar-ID och det kapslade JSON- `params` objektet med konfigurationsparametrar som visningsprogrammet stöder. I det här fallet av `params` objekt måste det ha minst den URL för bildservrar som skickats som `serverUrl` egenskap och ursprunglig resurs som `asset` parameter. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet anropar du metoden precis före den avslutande `init()` taggen eller på body- `BODY` `onload()` händelsen.

   Samtidigt bör behållarelementet inte nödvändigtvis vara en del av webbsidans layout just nu. Den kan till exempel vara dold med det format som den har tilldelats `display:none` . I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När den här åtgärden utförs återtas visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar `init()` metoden. Exemplet förutsätter `spinViewer` att det är visningsprograminstansen, `s7viewer` är platshållarens namn `DIV`, [!DNL http://s7d1.scene7.com/is/image/] är webbadressen för bildservern och [!DNL Scene7SharedAssets/SpinSet_Sample] är resursen.

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett fullständigt exempel på en enkel webbsida som bäddar in Snurra-läsaren med fast storlek:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsiv designinbäddning med obegränsad höjd**

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets behållares körningsstorlek `DIV`. I det här exemplet kan du anta att webbsidan tillåter att visningsprogrammets behållare tar 40 % av webbläsarens fönsterstorlek, och låter dess höjd vara obegränsad. `DIV` Den resulterande HTML-koden för webbsidan ser ut så här:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Att lägga till visningsprogrammet på en sådan sida liknar inbäddning med fast storlek, men den enda skillnaden är att du inte behöver definiera visningsprogrammets storlek explicit.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Skapa och initiera visningsprogrammet.

Alla stegen ovan är desamma som vid inbäddning med fast storlek. Lägg till behållaren `DIV` till den befintliga &quot;-hållaren&quot; `DIV`. Följande kod är ett komplett exempel. Du kan se hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Flexibel storleksinbäddning med definierad bredd och höjd**

Vid flexibel inbäddning med bredd och höjd är webbsidans format annorlunda. Det innebär att den ger både storlekar och centrering till &quot;hållaren&quot; `DIV` i webbläsarfönstret. Dessutom anger webbsidan storleken på elementet `HTML` och `BODY` elementet till 100 %:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

De återstående inbäddningsstegen är identiska med responsiv designinbäddning med obegränsad höjd. Följande exempel visas:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Bädda in med Setter-baserat API**

I stället för att använda JSON-baserad initiering är det möjligt att använda set-based API och no-args-konstruktor. Med denna API-konstruktor tar inga parametrar och konfigurationsparametrar anges med hjälp av `setContainerId()`-, `setParam()`och `setAsset()` API-metoder med separata JavaScript-anrop.

I följande exempel visas inbäddning med fast storlek med set-based API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```

