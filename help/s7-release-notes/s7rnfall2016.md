---
title: Scene7 hösten 2016
description: Den senaste versionsinformationen om Adobe Scene7 hösten 2016, en del av Adobe Experience Manager-lösningen i Adobe Experience Cloud.
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2236'
ht-degree: 0%

---

# Scene7 hösten 2016{#scene-fall-release}

Den senaste versionsinformationen om Adobe Scene7 hösten 2016 är en del av Adobe Experience Manager-lösningen i Adobe Experience Cloud.

## Scene7 hösten 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Den senaste versionsinformationen för [!DNL Adobe Scene7] hösten 2016-versionen av [!DNL Adobe Experience Manager]-lösningen i [!DNL Adobe Experience Cloud].

* [Allmänt](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visare (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visare (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visare (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 och Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Allmänt {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe är glada över att kunna meddela att det finns HTTP/2-leverans av innehåll, vilket i sin helhet ger bättre prestanda.

Se [HTTP2 Delivery of Content FAQ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Fullständig dokumentation finns på [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Nya funktioner, förbättringar och felkorrigeringar**

* Funktionen för videoinspelning har tagits bort från användargränssnittet för [!DNL Adobe Scene7 Publishing System].
* Autentisering har lagts till för alla Scene7-servrar där det är nödvändigt och möjligt
* Felkorrigering som involverar listvyn i papperskorgen.
* **Användarfunktionen Skapa Dynamic Media Classic (Scene7) Admin** har tagits bort från användarhanteringen på grund av säkerhetsproblem.
* FTP WebAdmin har nu stöd för OKTA-autentisering.
* Funktionen för standardlösenordet som skapades för nya Media Portal-användare har tagits bort.
* Felkorrigering med det tillfälliga lösenord som skapades när en ny användare lades till. Lösenordet uppfyller inte de nödvändiga lösenordskraven.
* Löste problem med WebAdmin-rotdisken full.
* Felkorrigering som innebär att en användare inaktiveras återspeglas inte direkt i användargränssnittet.
* Felkorrigering som innebär att en användare tas bort som inte gjorde att du kunde återskapa användaren senare.
* Felkorrigering med välkomstmeddelandet som skickades till nya Scene7-användare som inte innehöll autentisering för att kontrollera vissa inställningar.
* Felkorrigering som innebär att det inte gick att hämta en FTP-mapplista om någon mapp hade specialtecken i namnet.
* Konfigurera OKTA-tjänsteleverantörer för Scene7-miljöer.
* Stöd för Experience Cloud Org ID för visningsprogramanalys har lagts till.
* Implementerade Scene7 SAML-användare.

## Visare (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Fullständig dokumentation finns i [Referenshandbok för visningsprogram](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Felkorrigeringar för Image Serving 5.5.3**

* Kompatibilitet med RequireJS- och DOJO-bibliotek.

  Konsoliderade SDK JS-cachning under distributionen av visningsprogrammet.

## Visare (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Fullständig dokumentation finns i [Referenshandbok för visningsprogram](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Felkorrigeringar för Image Serving 5.5.2**

* Det gick inte att spela upp videon i Internet Explorer 11 på Windows 7.
* `initialframe` påverkade inte stående läge på mobila enheter för HTML5 eCatalog.

## Visare (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Fullständig dokumentation finns i [Referenshandbok för visningsprogram](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Nya funktioner, förbättringar och felkorrigeringar för Image Serving 5.5.1**

* HTML5 eCatalog-visningsprogram med sökfunktion.
* HLS-direktuppspelad videouppspelning har lagts till som standardmetod för videoleverans i de flesta datorsystem. Flash-baserad HDS-videoströmning är fortfarande tillgängligt som ett alternativt uppspelningsalternativ.
* Stöd för enheter med både mus- och pekrörelser som kör Chrome webbläsare.
* Stöd för Experience Cloud Org ID har lagts till i Analytics-integreringen.
* Uppdatera AppMeasurement JavaScript-bibliotek till version 1.6.1.
* Stöd för höger-till-vänster-orientering har lagts till i eCatalog-visningsprogrammet.
* Korrigerat problem där `tip=0,-1,0` orsakade ett fel utanför intervallet.

**Kompatibilitetsinformation**

* BlackBerry®

   * Inkompatibelt med äldre AVS-uppsättningar. Klienter måste överföra AVS-uppsättningar igen för att tillåta uppspelning.

* Allmänt

   * Skalning på webbläsarsidan kan göra användargränssnittet och bilderna suddiga när användaren zoomar in på sidan. Gränssnittsformatering kan också visas felaktigt beroende på zoomning. Den här effekten överförs till helskärmsläge.
   * På grund av storleksbegränsningar på mobila enheter använder visningsprogrammet för blandade media gester för att växla bildrutor i inbäddade bilduppsättningar i stället för att trycka på den inbäddade färgrutekomponenten. Komponenten finns där som en visuell indikator.
   * I Internet Explorer-webbläsare och vissa touchenheter upptar helskärmsläget inte hela enhetsskärmen. I stället ändras programmets storlek till webbläsarfönstrets storlek.
   * Knappen Stäng fungerar inte i iOS 8.0 och 8.1, men finns inte längre i iOS 8.2

* Galaxy SIII

   * Minnesläcka som visas i visningsprogrammen Zoom och eCatalog HTML 5. Upprepad navigering i bildrutor kan göra att webbläsaren kraschar.
   * Dubbeltryck på visningsprogrammet kan göra att hela sidan zoomas i stället för bara visningsprogrammet med skalning på webbläsarsidan aktiverad.

* Galaxy S4

   * Enheten har identifierats som en surfplatta i stående läge med helskärm incheckad i webbläsarinställningarna.

* Galaxy Nexus

   * Dubbeltryck på visningsprogrammet kan göra att hela sidan zoomas i stället för bara visningsprogrammet med skalning på webbläsarsidan aktiverad.

* Galaxy Nexus 10 och Galaxy

   * eCatalog med felaktigt uppslag med stående och liggande orientering.

* HTML Mobile Devices

   * HTC-mobilenheter Adobe upptäcker att det inte går att inaktivera inbyggda nyp-zoom är en funktion i HTC UI-wrapper (HTC Sense). Det här problemet kan göra att hela sidan zoomas när du använder Nyp för att zooma i visningsprogrammet. Föreslå att dubbelknacka i stället.
   * Bildschemaikoner kan överlappa om bildscheman är små och nära varandra.

* HTML5-video

   * Internet Explorer 9: anpassade förhandsvisningsbilder visas inte.
   * Modifieraren `IntialBitRate` stöds bara med HLS- och HDS-uppspelning för programvara. Det fungerar inte när uppspelningen använder den inbyggda spelaren.
   * OGG- och WebM-progressiv uppspelning stöds för närvarande inte.
   * Webbläsarskalning kan göra att videospelaren visas i fel storlek (inklusive visningsinställningar för Windows OS-kontrollpanelen).
   * Videosökning med HLS-direktuppspelning på Safari kan vara inkonsekvent.

* Internet Explorer

   * Quirks-läget stöds för närvarande inte.
   * Kompatibilitetsläget stöds för närvarande inte.
   * Internet Explorer på mobilen stöds för närvarande inte.

* iOS

   * Stora e-kataloger kan få webbläsaren att krascha på iPad 2.
   * iPhone 6+-telefoner kan av tittarna identifieras som surfplattor.

* Safari

   * Safari 6.1 eller senare: Inställningarna för Internetplugin-program kan förhindra videouppspelning av Flash.
   * Sökning efter video med HLS-direktuppspelning på Safari kan vara inkonsekvent.
   * Det går inte att söka till slutet av videon på Safari 6 med HLS-direktuppspelning.

**Kända fel och begränsningar**

* Image Serving-modifierare från `iscommands` läggs inte till i `req=set`-begäran. Modifierare som bara påverkar bildvisningen fungerar bra. Modifierare som påverkar storleken måste användas i en komplex resurs. Till exempel:

  `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [Utfällbar meny] IE9 finns ibland kvar på skärmen när musen är avstängd.
* Webbläsarskalning leder till fel storleksändring.
* iPad 2: Large eCatalog asset kraschar Safari på iOS.
* Alla visningsprogram

   * Vattenstämplar, förvrängning och låsning stöds inte.
   * Bildförinställningar stöds inte.
   * Det går inte att lägga till eller ta bort visningsprogrammet från DOM med `display:none` CSS eller genom att dynamiskt koppla loss det från den överordnade noden.

* HTML5 Alla visningsprogram

   * Inbäddning av visningsprogram i tabell kan leda till felaktig storlek eller placering av visningsprogrammet i icke-ursprungligt helskärmsläge. Föreslå användning av DIV i stället.
   * Parametrar med explicita instansnamn i koden kräver att instansnamn i URL:en också skrivs över (till exempel `zoomView.iconfeffect=0`).
   * Beskärning av bildserverkommando stöds för närvarande inte.
   * Knappen Stäng fungerar bara om visningsprogrammet är öppet i det underordnade fönstret.
   * Modifieraren `iscommands` stöder inte Image Serving-modifierare som påverkar bildstorleken.

* HTML5 eCatalog

   * Om du navigerar till en annan HTML-sida och återgår till den första sidan återställs visningsprogrammet ibland.
   * Sidlayouten visas ibland felaktigt efter att iOS-enheten roterats. När du zoomar in på sidan korrigeras layouten.
   * Interna länkar endast till vänstersidan i flersidiga uppslag. Påverkar mobila enheter i stående läge.
   * InitalFrame länkar endast till den vänstra sidan i flersidiga uppslag. Påverkar mobila enheter i stående läge.
   * På grund av webbläsarbegränsningar är utskriftsfunktionen inte tillgänglig i IE9.

* HTML5 MixedMedia

   * Ljudspårets uppspelning stöds inte.

* HTML5 Social

   * För att miniatyrerna ska kunna återges korrekt i utgående e-post måste modifieraren `serverurl` ha en absolut URL.

* HTML5-video

   * Det kan uppstå ett fel med maximal storlek i förhandsvisningsbilden. Företaget måste öka begränsningsinställningen för Image Serving Publish.
   * Videoklipp kräver en företagsregeluppsättning om värdtjänsten för HTML-sidan hanteras från en extern server (inte en Scene7-server). Kontakta supporten för Adobe om du behöver hjälp.
   * Analysspårning kan rapportera felaktig uppspelningsprocent på grund av buffring
   * Svarta bildrutor i stället för förhandsvisningsbilder kan visas på iPad- eller Android™-enheter.
   * Svart bildruta kan blinka på skärmen när visningsprogrammet läses in på iPad- eller Android™-enheter.
   * Svarta kantlinjer visas bredvid VideoPlayer-komponenten när bakgrunden är inställd på vit/genomskinlig på iPad-enheter.
   * Den sista videobildrutan kan förvrängas i iPad med iOS 7.
   * Ibland kan makroblockering förekomma under videosökning i HLS-direktuppspelningsläge i Chrome-, Firefox- och Internet Explorer-webbläsare.
      * Förhandsvisningsbilden kanske inte visas i Microsoft® Edge webbläsare för första gången.
      * Posterbilden kan döljas efter att videon har lästs in i Internet Explorer 9 när progressiv uppspelning används.

## Scene7 HTML 5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

Användarhandboken finns i Adobe HTML5 Viewer SDK-mappen för klientinstallationen. Komponent-API-dokumentationen finns i undermappen docs i klientinstallationen.

**Felkorrigeringar för 3.0.2**

* VideoPlayer - Det gick inte att spela upp video i Internet Explorer 11 i Windows 7.
* TableOfContents - `initialframe` påverkade inte stående läge på mobila enheter för HTML5 eCatalog-visningsprogrammet.

**Nya funktioner, förbättringar och felkorrigeringar för 3.0.1**

* Allmänt

   * HLS-direktuppspelad videouppspelning har lagts till som standardmetod för videoleverans i de flesta datorsystem. Flash-baserad HDS-videoströmning är fortfarande tillgängligt som ett alternativt uppspelningsalternativ.
   * Komponenterna SearchManager, SearchPanel, SearchEffect och SearchButton har lagts till som stöd för den nya sökfunktionen i visningsprogram för eCatalog.
   * Stöd för enheter med både mus- och pekrörelser som körs i Chrome webbläsare.
   * Avsaknad av Android™-version som stöd för framtida versioner av operativsystemet.
   * Lägg till stöd för höger till vänster-orientering i eCatalog-specifika SDK-komponenter.

* ControlBar

   * Tillagd valfri rullning för ControlBar-innehåll om det inte passar in i den tillgängliga bredden.

* FlyoutzoomView

   * Korrigerat fall där `tip=0,-1,0` orsakade ett fel utanför intervallet.

**Kompatibilitetsinformation**

* Android™ 4.x

   * Om du vill inaktivera standardinställningen måste följande CSS-regel läggas till för komponenten:

     `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * Videouppspelningen kan upphöra när bithastighetsströmmar ändras i AVS-uppsättningar.

* Chrome

   * Alla API-anrop som framtvingar komponentåterskapande kan ignoreras på grund av Chrome interna cachning.

* Galaxy SIII

   * Visningsprogrammet kan ibland inte läsas in i helskärmsläge.
   * Sidvyn har för närvarande ett minnesläckage på enheten.
   * Dubbeltryck på gest zoomar in visningsprogrammet och sidan när sidskalning på webbläsaren är aktiv.

* Galaxy Nexus

   * Artefakter som visas över vissa vykomponenter.
   * Dubbeltryck på gest zoomar in visningsprogrammet och sidan när sidskalning på webbläsaren är aktiv.

* IPAD 3

   * IPad 3 har en inbyggd upplösning på 2 048 x 1 536. Upplösningen kan orsaka visningsproblem om företagets IS-publicering, bildstorleksgränsen är lägre.

* iPhone4

   * Ikoneffektens repetitionsikon ersatt med en uppspelningsikon efter bläddring.

* Internet Explorer

   * I IE 10 och äldre helskärmsläge upptar inte hela skärmen, utan ändrar bara storlek på programmet till webbläsarfönstrets storlek.
   * Renderingsläget Kickor stöds inte.
   * Internet Explorer på mobilen stöds för närvarande inte.
   * Util.js kanske inte kan läsas in om det inkluderas asynkront.
   * Ikonen IconEffect blockerar klickningshändelser i komponenterna SpinView och ZoomView.

* Videospelare för inbyggd enhet

   * Gränssnittskomponenter i lager över VideoPlayer stöds inte när VideoPlayer används för att anropa enhetens inbyggda spelare.
   * Videouppspelning i inbyggt läge är inkonsekvent i Safari 6.
   * Inbyggd uppspelning ersätter repetitionsikonen med uppspelningsikonen efter bläddring.

* Pekskärmar

   * helskärmsläget upptar inte hela enhetsskärmen, utan ändrar bara storlek på programmet till webbläsarfönstrets storlek.
   * Anpassade markörer fungerar inte på pekenheter.
   * Sidskalning på pekenheter stöds för närvarande inte. Om du vill bädda in visningsprogram för HTML5 måste du ha en meta-tagg för visningsområdet med lämpliga inställningar.

* Xoom

   * Dubbeltryck på gest zoomar in visningsprogrammet och sidan när sidskalning på webbläsaren är aktiv.

**Kända fel och begränsningar**

* Alla komponenter

   * I version 2.7.2 och tidigare lades vissa komponenter till i DOM med API:t `insertBefore()`. Det innebär att sådana komponenter placeras längst ned i staplingsordningen, oavsett när komponentinstansen skapas i förhållande till andra komponenter. I version 2.8.1 använder alla komponenter `appendChild()` API nu, vilket innebär att komponentens staplingsordning skulle matcha ordningen när instansen skapades.

   * Det går inte att använda modifieraren `iscommand` för att ange bildens alfakanalformat. Använd parametern `FMT` i stället.
   * CSS-transformationsegenskapen stöds för närvarande inte.

* Pekskärmar

   * Fästningsgest på touchenheter genererar ingen zoomhändelse

* Behållare

   * Kantlinje, utfyllnad och marginaler i behållaren stöds inte. Adobe föreslår att du lägger till formatelement i överordnad DIV.
   * Du måste ange behållarstorleken explicit, annars kan komponenterna storleksändras korrekt.

* Utskriftskomponent

   * På grund av webbläsarbegränsningar kan det hända att utskriftskomponenten inte skalar innehållet korrekt på papperet i Internet Explorer 9.

* IconEffect-komponent

   * IconEffect genererar ett skriptfel i Internet Explorer om `autohide` är inaktiverat (inställt på `0`).

* ImageMapEffect-komponent

   * Fördröj med ompositionsikonen när du panorerar bilden på en visningskomponent.

* MediaSet-komponent

   * Textbundna resurser kräver samma kodning som på URL:en.

* NavigationView-komponent

   * Komponenten stöder för närvarande inte storleksändring.

* PageScrubber-komponent

   * När PageScrubber-bubblan är inställd på text i iPhone 5 visas artefakter när knappen dras längs spåret. Det går att använda `-webkit-background-clip: content;` i formatet runt problemet.

* SpinView-komponent

   * SpinView verkar ibland frysa när svepningsgesten och enheten roteras medan bilden snurras.

* Färgrutekomponent

   * När du markerar en färgruta som ligger utanför intervallet visas två högdagrar.
   * Automatisk rullning med metoden `selectSwatch()` fungerar felaktigt.

* VideoPlayer

   * Videobildrutan uppdateras inte om sökningen är inställd på 100 procent med återställningen inställd på auto.
   * Ibland kan makroblockering inträffa vid videosökning i HLS-direktuppspelningsläge i Chrome-, Firefox- och Internet Explorer-webbläsare.
   * Förhandsvisningsbilden kanske inte visas i Microsoft® Edge webbläsare för första gången.
   * Posterbilden kan döljas efter att videon har lästs in i Internet Explorer 9 när progressiv uppspelning används.

## Dynamic Media Image Serving 6.3.2 och Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC-verktyg - flaggan `downsample2x2` stöds inte längre. Den här flaggan var en 2x2-nedsampling med låg kvalitet som inte längre används av IPS.
* CORS-huvud - CORS-huvudet är för närvarande konfigurerat för `/is/content/` begäranden.
