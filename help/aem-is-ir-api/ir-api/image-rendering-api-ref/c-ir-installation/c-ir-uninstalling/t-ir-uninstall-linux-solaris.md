---
title: Avinstallation på Linux® och Solaris™
description: Följ dessa anvisningar för att avinstallera bildåtergivning i ett Linux®- eller Solaris™-system.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Avinstallation på Linux® och Solaris™{#uninstalling-on-linux-and-solaris}

Följ dessa anvisningar för att avinstallera bildåtergivning i ett Linux®- eller Solaris™-system. Det finns två olika metoder som du kan använda. Gör något av följande:

## Metod 1

1. Sök [!DNL uninstall.sh].

   Den finns i den katalog som ImageRendering installerades från. Om den här katalogen har tagits bort måste det ursprungliga installationspaketet vara okomprimerat och okomprimerat för att kunna extraheras [!DNL uninstall.sh].
1. Kör [!DNL uninstall.sh] och följ instruktionerna på skärmen.

## Metod 2

1. Stoppa ImageRendering med följande:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Ta bort ImageRendering från datorn. Vilket kommando du använder beror på datorn.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Ta bort kataloger eller filer som inte har tagits bort i steg 2.

