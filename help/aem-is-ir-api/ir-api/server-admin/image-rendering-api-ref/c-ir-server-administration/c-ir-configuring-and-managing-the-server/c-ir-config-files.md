---
description: Konfigurationsinställningarna för bildåtergivning lagras i konfigurationsfilen för plattformsservern.
seo-description: Konfigurationsinställningarna för bildåtergivning lagras i konfigurationsfilen för plattformsservern.
seo-title: Konfigurationsfiler
solution: Experience Manager
title: Konfigurationsfiler
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Konfigurationsfiler{#configuration-files}

Konfigurationsinställningarna för bildåtergivning lagras i konfigurationsfilen för plattformsservern.

Konfigurationsfilen för plattformsservern finns på [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Filen är en JAVA-egenskapsfil. Du måste följa gällande regler, annars kan det hända att Platform Server inte startar. Ett dubbelt omvänt snedstreck (`\\`) eller ett enkelt snedstreck (/) måste användas i stället för ett enkelt omvänt snedstreck (\) i Windows-filsökvägar, eftersom det omvända snedstrecket används som ett escape-tecken i den här filtypen. Filen innehåller odokumenterade egenskaper som är avsedda för intern serveranvändning och får inte ändras.

Se [Referens för konfigurationsinställningar](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) för en lista över alla konfigurationsinställningar för bildåtergivning.
