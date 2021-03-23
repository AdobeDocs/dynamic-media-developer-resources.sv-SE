---
description: Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).
seo-description: Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).
seo-title: Översikt
solution: Experience Manager
title: Översikt
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---


# Översikt{#overview}

Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).

Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).

Varje bildkatalog består av en nödvändig katalogattributfil och en uppsättning valfria katalogdatafiler:

* Bilddatafilen som specificerar bilder och mallar och tillhörande metadata.
* SVG-datafilen som specificerar SVG-filer och tillhörande metadata.
* Makrodefinitionsfilen som innehåller definitioner för begärandemakron.
* Teckensnittsmappningsfilen som håller reda på teckensnitt.
* Profilmappningsfilen som specificerar ICC-färgprofiler.
* Regeluppsättningsfilen som definierar förbearbetningsregler för HTTP-begäran.

Katalogdatafiler associeras med bildkataloger utifrån filreferenser i katalogattributfilen. Samma katalogdatafil kan delas av flera bildkataloger.

Katalogattributfiler måste ha ett [!DNL .ini]-filsuffix och måste finnas i plattformsserverns katalogmapp ( `PlatformServer::catalog.rootPath`). Katalogdatafiler kan finnas i samma mapp eller i en annan mapp som är tillgänglig för plattformsservern.

Det här dokumentet beskriver bildkatalogsfilformatet för Dynamic Media Image Serving-systemet. Den avsedda målgruppen är erfarna programmerare och webbutvecklare som vill använda Dynamic Media Image Serving för en webb- eller anpassad applikation.

Det antas att läsaren i allmänhet känner till Dynamic Media Image Serving-systemet, allmänna HTTP-protokollstandarder och konventioner samt grundläggande bildterminologi.
