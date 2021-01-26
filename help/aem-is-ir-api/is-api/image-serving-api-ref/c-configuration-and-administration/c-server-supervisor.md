---
description: Image Serving-komponenterna hanteras av Server Supervisor, som är en Linux-daemon eller Windows-tjänst (S7Supervisor.exe, som listas som "Dynamic Media Image Serving" på kontrollpanelen för tjänster).
seo-description: Image Serving-komponenterna hanteras av Server Supervisor, som är en Linux-daemon eller Windows-tjänst (S7Supervisor.exe, som listas som "Dynamic Media Image Serving" på kontrollpanelen för tjänster).
seo-title: Serveransvarig
solution: Experience Manager
title: Serveransvarig
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Serveransvarig{#server-supervisor}

Image Serving-komponenterna hanteras av Server Supervisor, som är en Linux-daemon eller Windows-tjänst (S7Supervisor.exe, som listas som &quot;Dynamic Media Image Serving&quot; på kontrollpanelen för tjänster).

Förutom att starta och stoppa andra Image Serving-komponenter ansvarar Server Supervisor för att säkerställa de övriga komponenternas hälsa. Om en komponent kraschar startas den om automatiskt för att minimera eventuella avbrott i tjänsten.

## Starta och stoppa {#section-061d28d74e034a30adc39ea3e2031cd0}

Serverhanteraren startas, stoppas och startas om med Image Serving-verktygsskriptet. Mer information finns i [Verktygsdokumentationen](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f).

När du startar och stoppar Server Supervisor startas och stoppas alla andra Image Serving-komponenter automatiskt.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
