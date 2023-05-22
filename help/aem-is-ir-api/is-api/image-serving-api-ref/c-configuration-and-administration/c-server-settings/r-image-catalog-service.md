---
description: Använd de här serverinställningarna för tjänsten Image catalog.
solution: Experience Manager
title: Tjänsten Bildkatalog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# Tjänsten Bildkatalog{#image-catalog-service}

Använd de här serverinställningarna för tjänsten Image catalog.

## CS::catalog.rootPath - Mappen Bildkatalog {#section-02d107f157384b18835f884f24fea3aa}

Sökväg till bildkatalogsmappen (där alla [!DNL catalog.ini] filer måste finnas). Kan vara en absolut filsökväg eller en relativ sökväg till *[!DNL install_folder]*. Servern övervakar den här mappen kontinuerligt och läser in eller läser in kataloger igen när en ny huvudkatalogfil (med [!DNL .ini] filsuffix) identifieras eller när den senaste ändringstiden för en befintlig huvudkatalogfil har ändrats.

## CS::catalog.cacheRoot - katalogcachemapp {#section-73e499c3a5974f1aa4251e70272ff503}

Rotmappen för katalogsystemets cache. Kan anges till samma som en av mapparna i `PS::cache.rootPaths`. Mappen måste skapas manuellt innan den här inställningen ändras.

## CS::catalog.modificationWaitTime - analysfördröjning för katalogfil {#section-7348065bcc124cb68ea947bf1b9b0845}

Tid i msek som katalogtjänsten väntar efter en [!DNL catalog.ini] filen ändras tills den läser in de sekundära katalogfilerna. Med den här fördröjningen kan du säkerställa att alla sekundära katalogfiler är uppdaterade innan katalogtjänsten försöker läsa in dem. Heltalsvärde i msek.

## CS::catalog.refreshInterval - kontrollfrekvens för katalogfil {#section-517fefc1d8784777a1026abec8630d58}

Hur ofta katalogtjänsten söker efter ändringar i bildkataloger. Heltalsvärde i msek.
