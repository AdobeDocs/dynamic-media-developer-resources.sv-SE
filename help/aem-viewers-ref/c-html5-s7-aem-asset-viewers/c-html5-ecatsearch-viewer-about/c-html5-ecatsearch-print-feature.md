---
description: Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.
solution: Experience Manager
title: Utskriftsfunktion
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Utskriftsfunktion{#print-feature}

Med visningsprogrammet kan du skriva ut kataloginnehållet till en skrivare.

Utskriftsfunktionen aktiveras av en dedikerad knapp i verktygsfältet. Genom att klicka på knappen kan användaren välja ett utskriftsintervall och antalet sidor per ark.

Utskriftens kvalitet kan justeras med konfigurationsparametern `printquality`. Observera att det inte är rekommenderat att ställa in `printquality` på värden som är betydligt högre än standardvärdet. Orsaken är att den leder till mycket hög minnesförbrukning i webbläsaren på klientens system. Kontrollera också att den maximala bildsvarsstorleken som angetts för ditt Dynamic Media Classic-företag är större än det konfigurerade `printquality`-värdet.

>[!NOTE]
>
>Utskriftsfunktionen är bara tillgänglig på stationära datorer, förutom Internet Explorer 9.
