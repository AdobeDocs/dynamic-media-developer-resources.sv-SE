---
description: Interactive Video Viewer stöder återgivning av interaktiva färgrutor baserat på interaktiva data som skickas till visningsprogrammet som en konfigurationsparameter.
seo-description: Interactive Video Viewer stöder återgivning av interaktiva färgrutor baserat på interaktiva data som skickas till visningsprogrammet som en konfigurationsparameter.
seo-title: Stöd för interaktiva data
solution: Experience Manager
title: Stöd för interaktiva data
topic: Dynamic media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Stöd för interaktiva data{#interactive-data-support}

Interactive Video Viewer stöder återgivning av interaktiva färgrutor baserat på interaktiva data som skickas till visningsprogrammet som en konfigurationsparameter.

Den för närvarande synliga färgrutan motsvarar videotidsområdet som den är associerad med. När du klickar eller trycker på den interaktiva färgrutan aktiveras den åtgärd som tilldelats den vid redigeringen.

Interaktiva färgrutor kan antingen aktivera en snabbvy på värdwebbsidan genom att aktivera ett JavaScript-återanrop eller dirigera om användaren till en extern webbsida.

## Om snabbvyn {#section-7990e44f641042d2a38ba20c9413b3f8}

Dessa typer av interaktiva färgrutor bör redigeras med åtgärdstypen&quot;snabbvy&quot; i AEM Assets - on-demand. När en användare aktiverar en sådan färgruta kör visningsprogrammet JavaScript-återanrop `quickViewActivate` och skickar färgrutedata till den. Inbäddningswebbsidan förväntas lyssna på det här återanropet och när det utlöses öppnas en egen snabbvyimplementering.

## Omdirigera till en extern webbsida {#section-32ebe3c3a7f74892a428c5d48801de4d}

Färgrutor som har skrivits för åtgärdstypen&quot;snabbvy&quot; i AEM Assets - dirigera om användaren till en extern URL på begäran. Beroende på inställningarna vid redigeringen kan URL-adressen öppnas antingen på en ny webbläsarflik, i samma fönster eller i namngivet webbläsarfönster.
