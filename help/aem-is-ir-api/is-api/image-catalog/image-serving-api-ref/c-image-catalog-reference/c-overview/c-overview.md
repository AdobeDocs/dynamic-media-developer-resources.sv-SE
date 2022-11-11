---
description: Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).
solution: Experience Manager
title: Översikt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Översikt{#overview}

Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).

Bildkataloger används för att ge servern information om bilder och stöddata (som teckensnitt och ICC-profiler).

Varje bildkatalog består av en nödvändig katalogattributfil och en uppsättning valfria katalogdatafiler:

* Bilddatafilen som specificerar bilder och mallar och tillhörande metadata.
* Datafilen SVG, som specificerar SVG-filer och tillhörande metadata.
* Makrodefinitionsfilen som innehåller definitioner för begärandemakron.
* Teckensnittsmappningsfilen som håller reda på teckensnitt.
* Profilmappningsfilen som specificerar ICC-färgprofiler.
* Regeluppsättningsfilen som definierar förbearbetningsregler för HTTP-begäran.

Katalogdatafiler associeras med bildkataloger utifrån filreferenser i katalogattributfilen. Samma katalogdatafil kan delas av flera bildkataloger.

Katalogattributfiler måste ha en [!DNL .ini] filsuffixet och måste finnas i [!DNL Platform Server]Katalogmapp ( `PlatformServer::catalog.rootPath`). Katalogdatafiler kan finnas i samma mapp eller i andra mappar som är tillgängliga för [!DNL Platform Server].

Det här dokumentet beskriver bildkatalogsfilformatet för Dynamic Media Image Serving-systemet. Den avsedda målgruppen är erfarna programmerare och webbutvecklare som vill använda Dynamic Media Image Serving för en webb- eller anpassad applikation.

Det antas att läsaren i allmänhet känner till Dynamic Media Image Serving-systemet, allmänna HTTP-protokollstandarder och konventioner samt grundläggande bildterminologi.
