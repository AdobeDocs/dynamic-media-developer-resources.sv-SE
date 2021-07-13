---
description: Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.
solution: Experience Manager
title: Externa bildkällor
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Externa bildkällor{#foreign-image-sources}

Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.

Om du vill ange en extern URL för ett `src=`- eller `mask=`-kommando; Avgränsa bara hela den inbäddade URL:en med klammerparenteser:

` …&src={ *[!DNL foreignUrl]*}&…`

Fullständiga absoluta URL:er (om `attribute::AllowDirectUrls` har angetts) och URL:er i förhållande till `attribute::RootUrl` tillåts. Ett fel inträffar om en absolut URL är inbäddad och attributet: `AllowDirectUrls` är 0 eller om en relativ URL har angetts och `attribute::RootUrl` är tom.

Externa bilder cachelagras av servern enligt de cachelagringsrubriker som ingår i HTTP-svaret.
