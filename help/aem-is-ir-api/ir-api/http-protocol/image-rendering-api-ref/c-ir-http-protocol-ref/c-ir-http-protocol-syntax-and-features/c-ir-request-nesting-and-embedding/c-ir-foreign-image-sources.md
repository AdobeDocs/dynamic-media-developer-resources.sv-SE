---
description: Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.
seo-description: Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.
seo-title: Externa bildkällor
solution: Experience Manager
title: Externa bildkällor
uuid: 28a17400-4807-4e14-937a-80309be53d55
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Externa bildkällor{#foreign-image-sources}

Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.

Om du vill ange en extern URL för ett `src=`- eller `mask=`-kommando; Avgränsa bara hela den inbäddade URL:en med klammerparenteser:

` …&src={ *[!DNL foreignUrl]*}&…`

Fullständiga absoluta URL:er (om `attribute::AllowDirectUrls` har angetts) och URL:er i förhållande till `attribute::RootUrl` tillåts. Ett fel inträffar om en absolut URL är inbäddad och attributet: `AllowDirectUrls` är 0 eller om en relativ URL har angetts och `attribute::RootUrl` är tom.

Externa bilder cachelagras av servern enligt de cachelagringsrubriker som ingår i HTTP-svaret.
