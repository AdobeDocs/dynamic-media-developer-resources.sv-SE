---
description: Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.
seo-description: Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.
seo-title: Externa bildkällor
solution: Experience Manager
title: Externa bildkällor
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Externa bildkällor{#foreign-image-sources}

Image Serving stöder åtkomst till källbilder på externa HTTP- och FTP-servrar.

För att ange en extern URL för ett `src=` eller `mask=` kommando. Avgränsa bara hela den inbäddade URL:en med klammerparenteser:

` …&src={ *[!DNL foreignUrl]*}&…`

Fullständiga absoluta URL:er (om `attribute::AllowDirectUrls` har angetts) och URL:er i förhållande till `attribute::RootUrl` tillåts. Ett fel inträffar om en absolut URL är inbäddad och attributet: `AllowDirectUrls` är 0 eller om en relativ URL har angetts och `attribute::RootUrl` är tom.

Externa bilder cachelagras av servern enligt de cachelagringsrubriker som ingår i HTTP-svaret.
