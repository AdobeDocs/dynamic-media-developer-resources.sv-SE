---
description: Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).
seo-description: Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).
seo-title: Översikt
solution: Experience Manager
title: Översikt
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '296'
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

Det här dokumentet beskriver bildkatalogsfilformatet för Scene7 Image Serving-systemet. Den avsedda målgruppen är erfarna programmerare och webbutvecklare som vill använda Scene7 Image Serving för en webb- eller anpassad applikation.

Det antas att läsaren i allmänhet känner till Scene7 Image Serving-systemet, allmänna HTTP-protokollstandarder och konventioner samt grundläggande bildterminologi.
