---
description: Image Serving-komponenterna hanteras av Server Supervisor, som är en Linux-daemon eller Windows-tjänst (S7Supervisor.exe, som listas som "Dynamic Media Image Serving" på kontrollpanelen för tjänster).
solution: Experience Manager
title: Serveransvarig
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Serveransvarig{#server-supervisor}

Image Serving-komponenterna hanteras av Server Supervisor, som är en Linux-daemon eller Windows-tjänst (S7Supervisor.exe, som listas som &quot;Dynamic Media Image Serving&quot; på kontrollpanelen för tjänster).

Förutom att starta och stoppa andra Image Serving-komponenter ansvarar Server Supervisor för att säkerställa de övriga komponenternas hälsa. Om en komponent kraschar startas den om automatiskt för att minimera eventuella avbrott i tjänsten.

## Starta och stoppa {#section-061d28d74e034a30adc39ea3e2031cd0}

Serverhanteraren startas, stoppas och startas om med Image Serving-verktygsskriptet. Mer information finns i [Verktygsdokumentationen](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f).

När du startar och stoppar Server Supervisor startas och stoppas alla andra Image Serving-komponenter automatiskt.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
