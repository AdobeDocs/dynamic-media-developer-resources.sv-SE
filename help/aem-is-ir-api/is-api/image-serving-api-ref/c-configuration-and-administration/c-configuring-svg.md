---
description: SVgRender-komponenten är ett oberoende Java-program.
solution: Experience Manager
title: Konfigurerar SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# Konfigurerar SVG{#configuring-svg}

SVgRender-komponenten är ett oberoende Java-program.

Konfigurationsinställningarna för SVG finns i [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] och [!DNL ServerSupervisorRegistry.xml].

En socketanslutning används för att kommunicera mellan SVGRender och Image Server. Portnumret är 27346. Om det behövs kan det ändras genom att ställa in `SVGRender.port` i [!DNL svg.conf] och `<SVGTcpPort>` i [!DNL ImageServerRegistry.xml] på ett nytt värde.

## Se även {#section-c085b47d54d44059bdaa67fd5e226e91}

[Konfigurationsinställningar för SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
