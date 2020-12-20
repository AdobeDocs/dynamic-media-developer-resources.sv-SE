---
description: Interactive Image Viewer är ett visningsprogram som visar en enstaka, ej zoombar bild med klickbara hotspot-områden. Syftet med detta visningsprogram är att implementera en"köpbar banner"-upplevelse. Användaren kan alltså markera en aktiveringspunkt över banderollbilden och omdirigeras till en snabbvy eller produktinformationssida på webbplatsen. Den är utformad för att fungera på stationära datorer och mobila enheter.
seo-description: Interactive Image Viewer är ett visningsprogram som visar en enstaka, ej zoombar bild med klickbara hotspot-områden. Syftet med detta visningsprogram är att implementera en"köpbar banner"-upplevelse. Användaren kan alltså markera en aktiveringspunkt över banderollbilden och omdirigeras till en snabbvy eller produktinformationssida på webbplatsen. Den är utformad för att fungera på stationära datorer och mobila enheter.
seo-title: Interaktiv bild
solution: Experience Manager
title: Interaktiv bild
topic: Dynamic media
uuid: 18b7a0c3-c047-4ce1-8920-1d8ebc1ab60e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 0%

---


# Interaktiv bild{#interactive-image}

Interactive Image Viewer är ett visningsprogram som visar en enstaka, ej zoombar bild med klickbara hotspot-områden. Syftet med detta visningsprogram är att implementera en&quot;köpbar banner&quot;-upplevelse. Användaren kan alltså markera en aktiveringspunkt över banderollbilden och omdirigeras till en snabbvy eller produktinformationssida på webbplatsen. Den är utformad för att fungera på stationära datorer och mobila enheter.

>[!NOTE]
>
>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av detta visningsprogram.

Visningstypen är 508.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## Systemkrav {#section-b7270cc4290043399681dc504f043609}

Se [Systemkrav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Använda Interactive Image Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Interactive Image Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-fil innehåller alla SDK-komponenter för visningsprogrammet som används av just detta visningsprogram, resurser, CSS) som hämtats av visningsprogrammet under körning.

Interactive Image Viewer kan endast användas i inbäddat läge, där det är integrerat med målwebbsidan med det dokumenterade API:t.

Konfigurationen och skalningen liknar den för andra visningsprogram som beskrivs i den här hjälpen. All skalning görs med anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med Interactive Image Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Den interaktion som stöds av Video Image Viewer är aktivering av hotspot på datorsystem. Den här aktiveringen sker med ett enda tryck när du klickar och på enheter med pekskärm.

Visningsprogrammet är fullt åtkomligt via tangentbordet.

Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in interaktiv bildvisare {#section-6bb5d3c502544ad18a58eafe12a13435}

Interactive Image Viewer är avsedd att bäddas in på webbsidan. En sådan webbsida kan ha en statisk layout eller vara&quot;responsiv&quot; och visas på olika enheter eller för olika webbläsarfönsterstorlekar.

För att tillgodose dessa behov har visningsprogrammet stöd för två primära åtgärdslägen: inbäddning i fast storlek och responsiv inbäddning.

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan. Den här webbsidan kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet tar normalt bara upp en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och responsiva designade sidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här är det bästa alternativet för webbsidor som har en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet kan behöva ändra storlek vid körning som svar på storleksändringen för dess behållare `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger bredden på behållaren `DIV`, och dess höjd inte begränsas, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den använda resursen. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor med flexibla ramverk för webbdesign som Bootstrap, Foundation och så vidare.

Om webbsidan ställer in både bredd och höjd för visningsprogrammets behållare `DIV` fyller visningsprogrammet bara det området. Den har också samma storlek som webbsidans layout. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i HTML-huvudet. Innan du kan använda visningsprogrammets API måste du ta med [!DNL InterativeImage.js]. Filen [!DNL InteractiveImage.js] finns under undermappen [!DNL html5/js/] i din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Du bör bara referera till JavaScript-filen `include` för huvudvisningsprogrammet på sidan. Du bör inte referera till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körningen. Referera inte direkt till HTML5 SDK `Utils.js`-biblioteket som läses in av visningsprogrammet från kontextsökvägen `/s7viewers` (s.k. konsoliderad SDK `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversioner. Adobe sparar inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att om du skickar en direkt referens till ett sekundärt JavaScript `include` som används av visningsprogrammet på sidan så bryts visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definierar behållaren `DIV`.

   Lägg till ett tomt `DIV`-element på sidan där du vill att visningsprogrammet ska visas. Elementet `DIV` måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API. DIV har den storlek som anges via CSS.

   Platshållaren `DIV` är ett placerat element, vilket innebär att CSS-egenskapen `position` är inställd på `relative` eller `absolute`.

   Följande är ett exempel på ett definierat platshållarelement `DIV`:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att antingen deklarera den för CSS-klassen på den översta nivån i absoluta enheter eller genom att använda modifieraren `.s7interactiveimage`.`stagesize`

   Du kan ange storlek i CSS direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som sedan tilldelas en post för visningsförinställningar i AEM Assets - on demand, eller skickas explicit med kommandot `style`.

   Mer information om hur du formaterar visningsprogrammet med CSS finns i [Video](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på HTML-sidan:

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Du kan skicka modifieraren `stagesize` explicit med initieringskoden för visningsprogrammet med samlingen `params` eller som ett API-anrop enligt beskrivningen i avsnittet Command Reference, så här:

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av klassen `s7viewers.InteractiveImage`, skickar all konfigurationsinformation till konstruktorn och anropar metoden `init()` för en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet ska åtminstone ha ett `containerId`-fält som innehåller namnet på visningsbehållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet. I det här fallet måste `params`-objektet ha minst den URL för bildservrar som skickas som `serverUrl`-egenskap och den ursprungliga resursen som `asset`-parameter. Med det JSON-baserade initierings-API:t kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet anropar du metoden `init()` precis före den avslutande `BODY`-taggen eller på body-händelsen `onload()`.

   Samtidigt bör behållarelementet inte nödvändigtvis vara en del av webbsidans layout just nu. Det kan till exempel vara dolt med `display:none`-format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de lägsta nödvändiga konfigurationsalternativen till konstruktorn och anropar metoden `init()`. Exemplet förutsätter att `interactiveImage` är visningsprograminstansen; `s7viewer` är namnet på platshållaren `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` är URL:en för bildhantering och `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` är resursen:

   ```
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in Video Image Viewer med fast storlek:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Responsiv designinbäddning med obegränsad höjd**

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets körningsstorlek `DIV`. I följande exempel antar du att webbsidan tillåter att visningsprogrammets behållare `DIV` tar 40 % av webbläsarens fönsterstorlek. Och höjden är obegränsad. HTML-koden för webbsidan ser ut så här:

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
1. Definierar behållaren `DIV`.
1. Skapa och initiera visningsprogrammet.

Alla steg ovan är desamma som med inbäddning med fast storlek. Lägg till behållaren `DIV` i befintlig `"holder"` `DIV`. Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

**Flexibel storlek för inbäddning med definierad bredd och höjd**

Vid flexibel inbäddning med bredd och höjd är webbsidans format annorlunda. Den ger båda storlekarna till DIV:n `"holder"` och centrerar den i webbläsarfönstret. Dessutom anger webbsidan storleken på elementen `HTML` och `BODY` till 100 procent.

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

Resten av inbäddningsstegen är identiska med stegen som används för responsiv inbäddning med obegränsad höjd. Följande exempel visas:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Bädda in med Setter-baserat API**

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Om du använder den här API-konstruktorn används inga parametrar och konfigurationsparametrar anges med API-metoderna `setContainerId()`, `setParam()` och `setAsset()` med separata JavaScript-anrop.

I följande exempel visas hur du använder inbäddning med fast storlek med det inställningsbaserade API:t:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```

