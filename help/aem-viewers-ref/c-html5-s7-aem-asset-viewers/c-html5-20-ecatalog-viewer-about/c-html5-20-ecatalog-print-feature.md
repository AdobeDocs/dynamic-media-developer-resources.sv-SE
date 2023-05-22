---
title: Utskriftsfunktion
description: Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Utskriftsfunktion{#print-feature}

Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.

Utskriftsfunktionen aktiveras av en dedikerad knapp i verktygsfältet. Genom att klicka på knappen kan användaren välja ett utskriftsintervall och antalet sidor per ark.

Kvaliteten på utskriften kan justeras med `printquality` konfigurationsparameter. Inställning `printquality` till värden som är högre än standardvärdet rekommenderas inte. Orsaken är att det leder till hög minnesförbrukning i webbläsaren på klientens system. Kontrollera också att den maximala bildsvarsstorleken som angetts för ditt Dynamic Media Classic-företag är större än den konfigurerade `printquality` värde.

>[!NOTE]
>
>Utskriftsfunktionen är bara tillgänglig på stationära datorer, förutom Internet Explorer 9.
