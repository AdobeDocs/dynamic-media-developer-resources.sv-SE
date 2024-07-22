---
title: Händelseåteranrop
description: Händelseåteranrop
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Händelseåteranrop{#event-callbacks}

Visningsprogrammet har stöd för JavaScript händelsereferenser som används på webbsidan för att spåra visningsprogrammets initieringsprocess eller körningsbeteende.

Återanropshanterare tilldelas genom att händelsenamn och motsvarande hanterarfunktioner skickas med egenskapen `handlers` till JSON-objektet `config` i visningsprogrammets konstruktor. Du kan också använda API-metoden `setHandlers()`.

Visningsprogramhändelser som stöds är bland annat följande:

* `initComplete` - utlöses när visningsprogrammets initiering är klar och alla interna komponenter skapas, så att det går att använda `getComponent()` API. Callback-hanteraren tar inga argument.
* `trackEvent` - utlöses varje gång en händelse inträffar i visningsprogrammet som kan hanteras av ett händelsespårningssystem, till exempel Adobe Analytics. Callback-hanteraren har följande argument:

   * `objID {String}` används inte just nu.
   * `compClass {String}` används inte just nu.
   * `instName {String}` ett instansnamn för HTML5 Viewer SDK-komponenten som utlöste händelsen.
   * `timeStamp {Number}`-händelsens tidsstämpel.
   * `eventInfo {String}` händelsenyttolast.

