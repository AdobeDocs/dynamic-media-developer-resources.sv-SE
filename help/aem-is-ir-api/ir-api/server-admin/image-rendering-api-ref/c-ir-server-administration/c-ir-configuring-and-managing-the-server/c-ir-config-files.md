---
description: Konfigurationsinställningarna för bildåtergivning lagras i konfigurationsfilen  [!DNL Platform Server] .
solution: Experience Manager
title: Konfigurationsfiler
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Konfigurationsfiler{#configuration-files}

Konfigurationsinställningarna för bildåtergivning lagras i konfigurationsfilen [!DNL Platform Server].

Konfigurationsfilen för plattformsservern finns på [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Filen är en JAVA-egenskapsfil. Du måste följa lämpliga konventioner, annars kanske [!DNL Platform Server] inte kan startas. Ett dubbelt omvänt snedstreck (`\\`) eller ett enkelt snedstreck (/) måste användas i stället för ett enkelt omvänt snedstreck (\) i Windows-filsökvägar, eftersom det omvända snedstrecket används som ett escape-tecken i den här typen av fil. Filen innehåller odokumenterade egenskaper som är avsedda för intern serveranvändning och får inte ändras.

Se [Konfigurationsinställningsreferens](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) för en lista över alla konfigurationsinställningar för bildåtergivning.
