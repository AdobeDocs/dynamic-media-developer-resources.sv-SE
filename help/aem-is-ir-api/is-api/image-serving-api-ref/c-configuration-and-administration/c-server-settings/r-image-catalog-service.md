---
description: Använd de här serverinställningarna för tjänsten Image catalog.
solution: Experience Manager
title: Tjänsten Bildkatalog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Tjänsten Bildkatalog{#image-catalog-service}

Använd de här serverinställningarna för tjänsten Image catalog.

## CS::catalog.rootPath - Mappen Bildkatalog {#section-02d107f157384b18835f884f24fea3aa}

Sökväg till bildkatalogsmappen (där alla [!DNL catalog.ini] filer måste finnas). Kan vara en absolut filsökväg eller en relativ sökväg till *[!DNL install_folder]*. Servern övervakar den här mappen kontinuerligt och läser in eller läser in kataloger igen när en ny huvudkatalogfil (med filsuffixet [!DNL .ini]) identifieras eller när den senaste ändringstiden för en befintlig huvudkatalogfil har ändrats.

## CS::catalog.cacheRoot - katalogcachemapp {#section-73e499c3a5974f1aa4251e70272ff503}

Rotmappen för katalogsystemets cache. Kan anges till samma som en av mapparna i `PS::cache.rootPaths`. Mappen måste skapas manuellt innan den här inställningen ändras.

## CS::catalog.modificationWaitTime - analysfördröjning för katalogfil {#section-7348065bcc124cb68ea947bf1b9b0845}

Tid i msek som katalogtjänsten väntar efter att en [!DNL catalog.ini]-fil har ändrats tills den läser in de sekundära katalogfilerna. Den här fördröjningen säkerställer att alla sekundära katalogfiler är uppdaterade innan katalogtjänsten försöker läsa in dem. Heltalsvärde i ms.

## CS::catalog.refreshInterval - kontrollfrekvens för katalogfil {#section-517fefc1d8784777a1026abec8630d58}

Hur ofta katalogtjänsten söker efter ändringar i bildkataloger. Heltalsvärde i ms.
