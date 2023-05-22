---
description: Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.
solution: Experience Manager
title: Utskriftsfunktion
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# Utskriftsfunktion{#print-feature}

Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.

Utskriftsfunktionen aktiveras av en dedikerad knapp i verktygsfältet. Genom att klicka på knappen kan användaren välja ett utskriftsintervall och antalet sidor per ark.

Kvaliteten på utskriften kan justeras med `printquality` konfigurationsparameter. Observera den inställningen `printquality` till värden som är betydligt högre än standardvärdet rekommenderas inte. Orsaken är att den leder till mycket hög minnesförbrukning i webbläsaren på klientens system. Kontrollera också att den maximala bildsvarsstorleken som angetts för ditt Dynamic Media Classic-företag är större än den konfigurerade `printquality` värde.

>[!NOTE]
>
>Utskriftsfunktionen är bara tillgänglig på stationära datorer, förutom Internet Explorer 9.
