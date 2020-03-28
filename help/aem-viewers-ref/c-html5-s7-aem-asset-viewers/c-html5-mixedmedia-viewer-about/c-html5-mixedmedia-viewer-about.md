---
description: Mixed Media Viewer är ett visningsprogram för media. Det har stöd för mediauppsättningar som innehåller bilder, färgruteuppsättningar, snurruppsättningar, videor och adaptiva videouppsättningar.
keywords: responsive
seo-description: Mixed Media Viewer är ett visningsprogram för media. Det har stöd för mediauppsättningar som innehåller bilder, färgruteuppsättningar, snurruppsättningar, videor och adaptiva videouppsättningar.
seo-title: Blandade media
solution: Experience Manager
title: Blandade media
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Blandade media{#mixed-media}

Mixed Media Viewer är ett visningsprogram för media. Det har stöd för mediauppsättningar som innehåller bilder, färgruteuppsättningar, snurruppsättningar, videor och adaptiva videouppsättningar.

En miniatyrbild längst ned i visningsprogrammet representerar varje medieuppsättningselement tillsammans med resurstypsindikatorn. När ett element i färgruteuppsättningen är markerat visas en andra rad med färgrutor så att du kan välja färgvariation i färgruteuppsättningen. Bilder och element för färgruteuppsättning har stöd för zoomning i löpande läge eller infogat läge. snurruppsättningar har stöd för både zoomning och snurrning. Videofilmer och adaptiva videouppsättningar har stöd för alla grundläggande uppspelningskontroller så länge som valfria undertexter visas ovanpå videoinnehållet. Användaren kan när som helst växla till helskärm genom att klicka på helskärmsknappen. Visningsprogrammet har en valfri stängningsknapp. Den är utformad för att fungera på stationära datorer och mobila enheter.

Mixed Media Viewer använder HTML5-direktuppspelad videouppspelning i HLS-format i standardkonfigurationen när det underliggande systemet stöder det. På system som saknar stöd för HTML5-direktuppspelning återgår visningsprogrammet till progressiv HTML5-videoleverans.

>[!NOTE]
>
>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet.

Visningstyp 505.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Använda blandad mediavisare {#section-f21ac23d3f6449ad9765588d69584772}

Mixed Media Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-fil innehåller alla SDK-komponenter för visningsprogrammet som används av det här visningsprogrammet, resurser och CSS) som hämtats av visningsprogrammet under körning.

Du kan använda blandad mediavisare i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer. Du kan också använda visningsprogrammet i inbäddat läge, där det är integrerat i en målwebbsida med hjälp av det dokumenterade API:t.

Konfigurationen och skalningen av visningsprogrammet liknar de andra visningsprogrammen. All skalning görs med anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensamma för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med blandad Media Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Mixed Media Viewer har stöd för enkelberörings- och flerberöringsgester som är vanliga i andra mobilprogram. När visningsprogrammet inte kan bearbeta en användares dragningsgest vidarebefordrar det händelsen till webbläsaren för att utföra en inbyggd sidbläddring. Med den här funktionen kan en användare navigera på sidan även om användaren upptar större delen av enhetens skärmområde.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesture </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Enkeltryckning </p> </td> 
   <td colname="col2"> <p> Aktiverar den utfällbara vyn eller ändringar mellan den primära och sekundära zoomnivån. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dubbelknacka </p> </td> 
   <td colname="col2"> <p>När du använder <span class="codeph"> kontinuerligt </span> zoomläge zoomas zoomningen in en nivå tills maximal förstoring nås. Nästa dubbelknackningsgest återställs till ursprungsläget. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tryck och håll </p> </td> 
   <td colname="col2"> <p> I <span class="codeph"> inline- </span> zoomläge aktiveras den zoomade bilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Knipning </p> </td> 
   <td colname="col2"> <p>I kontinuerligt zoomläge zoomas bilden in eller ut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vågrät dragning eller snärtning </p> </td> 
   <td colname="col2"> <p> När den aktuella resursen är en snurrfunktion och bilden är i ett återställningsläge snurrar den genom rotationsrutan vågrätt. </p> <p> När den aktuella resursen är en snurrfunktion eller en bild och bilden är inzoomad flyttas bilden vågrätt. Om bilden flyttas till vykanten och svepningen fortfarande utförs i den riktningen utför gesten en inbyggd sidrullning. </p> <p> Bläddrar igenom listan med färgrutor i färgrutefältet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lodrät dragning eller snärtning </p> </td> 
   <td colname="col2"> <p> Om bilden är i ett återställningsläge ändras den lodräta vyvinkeln om en flerdimensionell snurruppsättning används. I en endimensionell snurruppsättning, eller när en flerdimensionell snurra är på den sista eller första axeln, så att vertikal dragning inte resulterar i vertikal vinkeländring, utför gesten intern sidrullning. </p> <p> När den aktuella resursen är en snurra eller en bild och bilden är inzoomad, flyttar bilden lodrätt. Om bilden flyttas till vykanten och svepningen fortfarande utförs i den riktningen, utför gesten den inbyggda sidrullningen. </p> <p> Om gesten görs i färgruteområdet utförs en inbyggd sidrullning. </p> </td> 
  </tr> 
 </tbody> 
</table>

Visningsprogrammet har också stöd för både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Visningsprogrammet är fullt åtkomligt via tangentbordet.

Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in blandad Media Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en länk som, när användaren klickar på den, öppnar visningsprogrammet i ett separat webbläsarfönster. I andra fall är det nödvändigt att bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup-fönster, inbäddning i fast storlek och responsiv designinbäddning.

## Om popup-läge {#section-77d5aa03b8b94566958a179b1a2cd474}

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändrar storlek eller om en mobilenhets orientering ändras.

Popup-läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med hjälp av `window.open()` JavaScript-anrop, korrekt konfigurerade `A` HTML-element eller någon annan lämplig metod.

Vi rekommenderar att du använder en körklar HTML-sida för popup-åtgärder. I det här fallet anropas den [!DNL MixedMediaViewer.html] och finns i undermappen [!DNL html5/] för din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Du kan anpassa visuellt genom att använda anpassad CSS.

Följande är ett exempel på HTML-kod som öppnar visningsprogrammet i ett nytt fönster:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Om inbäddning av fast storlek och responsiv design {#section-ec86b100ba5943d0b16694268520bbde}

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet tar normalt bara upp en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designsidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här är det bästa alternativet för webbsidor som har en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet kan behöva ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`utan begränsningar, väljer visningsprogrammet automatiskt dess höjd enligt proportionerna för den resurs som används. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor som använder responsiva designlayoutramverk som Bootstrap, Foundation och så vidare.

Om webbsidan ställer in både bredd och höjd för visningsprogrammets behållare `DIV`fyller visningsprogrammet bara det området och följer den storlek som webbsidans layout ger. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

## Inbäddning med fast storlek {#section-17d162f76ffa4804b27928f51e7bea1d}

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i HTML-huvudet. Innan du kan använda visningsprogrammets API måste du ta med [!DNL MixedMediaViewer.js]. Filen [!DNL MixedMediaViewer.js] finns under undermappen [!DNL html5/js/] för din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Scene7-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Scene7-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Du bör bara referera till JavaScript- `include` filen för huvudvisningsprogrammet på sidan. Du bör inte referera till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körningen. Referera inte direkt till HTML5 SDK- `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökvägen (så kallad konsoliderad SDK `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversioner. Adobe sparar inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att om du skickar en direkt referens till ett sekundärt JavaScript `include` som används av visningsprogrammet på sidan så bryts visningsprogrammets funktion i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API. DIV har den storlek som anges via CSS.

   Platshållarens DIV är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   Kontrollera att helskärmsfunktionen fungerar som den ska i Internet Explorer. Kontrollera att det inte finns några andra element i DOM som har en högre staplingsordning än DIV:n för platshållaren.

   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Ange visningsprogrammets storlek

   I det här visningsprogrammet visas miniatyrer när du arbetar med uppsättningar med flera objekt. På stationära datorer placeras miniatyrbilder under huvudvyn. Samtidigt tillåter visningsprogrammet växling av huvudresursen under körning med hjälp av `setAsset()` API. Som utvecklare har du kontroll över hur visningsprogrammet hanterar miniatyrbildsområdet längst ned när den nya resursen bara har ett objekt. Det går att behålla den yttre visningsstorleken intakt och låta huvudvyn öka höjden och uppta miniatyrområdet. Eller så kan du hålla storleken på huvudvyn statisk och komprimera det yttre visningsområdet, låta webbsidans innehåll röra sig uppåt och sedan använda det lediga sidutrymmet som finns kvar från miniatyrbilderna.

   Om du vill behålla de yttre gränserna för visningsprogrammet intakt definierar du storleken för CSS-klassen på den översta nivån i absoluta enheter `.s7mixedmediaviewer` . Storleksändring i CSS kan placeras direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som senare tilldelas till en visningsförinställningspost i Scene7 Publishing System, eller skickas explicit med style-kommando.

   Mer information om hur du formaterar visningsprogrammet med CSS finns i [Anpassa visningsprogrammet för blandade media](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) .

   Följande är ett exempel på hur du definierar den statiska storleken på det yttre visningsprogrammet på en HTML-sida:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Du kan se beteendet med ett fast yttre visningsområde på följande exempelsida. Observera att storleken på det yttre visningsprogrammet inte ändras när du växlar mellan uppsättningar:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   Om du vill göra huvudvyns dimensioner statiska definierar du visningsstorleken i absoluta enheter för den inre `Container` SDK-komponenten med hjälp av `.s7mixedmediaviewer .s7container` CSS-väljaren eller med hjälp av `stagesize` modifieraren.

   Följande är ett exempel på hur du definierar visningsstorleken för den inre `Container` SDK-komponenten så att huvudvisningsområdet inte ändrar dess storlek när du byter resurs:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Följande exempelsida visar visningsprogrammets beteende med en fast storlek för huvudvyn. Observera att när du växlar mellan uppsättningar förblir huvudvyn statisk och webbsidans innehåll flyttas lodrätt:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   Du kan ställa in modifieraren antingen i visningsprogrammets förinställningspost i Scene7 Publishing System, eller skicka den explicit med visarens initieringskod med `stagesize` `params` samling, eller som ett API-anrop enligt beskrivningen i kommandoreferensavsnittet i den här hjälpen, som i följande exempel:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.MixedMediaViewer` klassen, skickar all konfigurationsinformation till konstruktorn och anropar `init()` metoden för en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet bör åtminstone ha det `containerId` fält som innehåller namnet på visningsbehållar-ID och det kapslade JSON- `params` objektet med konfigurationsparametrar som visningsprogrammet stöder. I det här fallet måste objektet ha minst den URL för bildserver som skickas som `params` egenskap, den URL-adress för videoservern som skickas som `serverUrl` egenskap och ursprunglig resurs som `videoserverurl` `asset` parameter. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet anropar du metoden precis före den avslutande `init()` taggen eller på body- `BODY` `onload()` händelsen.

   Samtidigt bör behållarelementet inte nödvändigtvis vara en del av webbsidans layout just nu. Den kan till exempel vara dold med hjälp av ett format som är tilldelat den. `display:none` I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar `init()` metoden. Exemplet förutsätter `mixedMediaViewer` att visningsprograminstansen är `s7viewer` platshållarens namn `DIV`, [!DNL http://s7d1.scene7.com/is/image/] är webbadressen till bildservern, [!DNL http://s7d1.scene7.com/is/content/] är webbadressen till videoservern, och [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] är tillgången:

```
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

Följande kod är ett komplett exempel på en enkel webbsida som bäddar in blandad Media Viewer med fast storlek:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Responsiv inbäddning med obegränsad höjd {#section-056cb574713c4d07be6d07cf3c598839}

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets behållares körningsstorlek `DIV`. I följande exempel kan du anta att webbsidan tillåter att visningsprogrammets behållare tar 40 % av webbläsarens fönsterstorlek, och låter dess höjd vara obegränsad. `DIV` HTML-koden för webbsidan ser ut så här:

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

Att lägga till visningsprogrammet på en sådan sida liknar stegen för inbäddning med fast storlek. Den enda skillnaden är att du inte behöver definiera visningsprogrammets storlek explicit.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Skapa och initiera visningsprogrammet.

Alla steg ovan är desamma som med inbäddning med fast storlek. Lägg till behållar-DIV i befintlig `"holder"` DIV. Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## Flexibel storleksinbäddning med definierad bredd och höjd {#section-0a329016f9414d199039776645c693de}

Vid flexibel inbäddning med bredd och höjd är webbsidans format annorlunda. DIV:n får båda storlekarna och den centreras i webbläsarfönstret. `"holder"` Dessutom ställer webbsidan in storleken på elementet `HTML` och `BODY` elementet till 100 procent.

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

Resten av inbäddningsstegen är identiska med stegen som används för responsiv designinbäddning med obegränsad höjd. Följande exempel visas:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Bädda in med Setter-baserat API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Om du använder den här API-konstruktorn används inga parametrar och konfigurationsparametrar anges med metoderna `setContainerId()`, `setParam()`och `setAsset()` API med separata JavaScript-anrop.

I följande exempel visas hur du använder inbäddning med fast storlek med set-based API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```

