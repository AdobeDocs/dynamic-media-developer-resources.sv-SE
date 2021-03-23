---
description: SVgRender-komponenten är ett oberoende Java-program.
seo-description: SVgRender-komponenten är ett oberoende Java-program.
seo-title: Konfigurera SVG
solution: Experience Manager
title: Konfigurera SVG
uuid: f6e131af-283e-4649-b349-123489c0838d
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Konfigurera SVG{#configuring-svg}

SVgRender-komponenten är ett oberoende Java-program.

SVG-konfigurationsinställningarna finns i [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] och [!DNL ServerSupervisorRegistry.xml].

En socketanslutning används för att kommunicera mellan SVGRender och Image Server. Portnumret är 27346. Om det behövs kan det ändras genom att ställa in `SVGRender.port` i [!DNL svg.conf] och `<SVGTcpPort>` i [!DNL ImageServerRegistry.xml] på ett nytt värde.

## Se även {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-konfigurationsinställningar](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
