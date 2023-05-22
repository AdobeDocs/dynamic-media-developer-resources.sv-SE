---
title: Stöd för interaktiva data
description: Interactive Video Viewer stöder återgivning av interaktiva färgrutor baserat på interaktiva data som skickas till visningsprogrammet som en konfigurationsparameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Stöd för interaktiva data{#interactive-data-support}

Interactive Video Viewer stöder återgivning av interaktiva färgrutor baserat på interaktiva data som skickas till visningsprogrammet som en konfigurationsparameter.

Den för närvarande synliga färgrutan motsvarar videotidsområdet som den är associerad med. När du klickar eller trycker på den interaktiva färgrutan aktiveras den åtgärd som tilldelats den vid redigeringen.

Interaktiv färgruta kan antingen aktivera en snabbvy på värdwebbsidan genom att aktivera ett JavaScript-återanrop eller dirigera om användaren till en extern webbsida.

## Om Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

Dessa typer av interaktiva färgrutor bör redigeras med åtgärdstypen&quot;snabbvy&quot; i Adobe Experience Manager Assets - On-demand. När en användare aktiverar en sådan färgruta körs visningsprogrammet `quickViewActivate` JavaScript-återanrop och skickar färgrutedata till den. Inbäddningswebbsidan förväntas lyssna på återanropet och när den utlöses öppnas en egen QuickView-implementering.

## Omdirigera till en extern webbsida {#section-32ebe3c3a7f74892a428c5d48801de4d}

Färgrutor som har skrivits för åtgärdstypen&quot;snabbvy&quot; i Experience Manager Assets - dirigera om användaren till en extern URL på begäran. Beroende på inställningarna vid redigeringen kan URL-adressen öppnas antingen på en ny webbläsarflik, i samma fönster eller i namngivet webbläsarfönster.
