---
description: Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.
solution: Experience Manager
title: Utskriftsfunktion
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Utskriftsfunktion{#print-feature}

Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.

Utskriftsfunktionen aktiveras av en dedikerad knapp i verktygsfältet. Genom att klicka på knappen kan användaren välja ett utskriftsintervall och antalet sidor per ark.

Utskriftens kvalitet kan justeras med konfigurationsparametern `printquality`. Observera att det inte är rekommenderat att ställa in `printquality` på värden som är betydligt högre än standardvärdet. Orsaken är att den leder till mycket hög minnesförbrukning i webbläsaren på klientens system. Kontrollera också att den maximala bildsvarsstorleken som angetts för ditt Dynamic Media Classic-företag är större än det konfigurerade `printquality`-värdet.

>[!NOTE]
>
>Utskriftsfunktionen är bara tillgänglig på stationära datorer, förutom Internet Explorer 9.

