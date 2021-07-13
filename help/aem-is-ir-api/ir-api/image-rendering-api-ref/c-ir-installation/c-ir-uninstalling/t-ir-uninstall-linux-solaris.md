---
description: Följ dessa anvisningar för att avinstallera bildåtergivning på ett Linux- eller Solaris-system.
solution: Experience Manager
title: Avinstallation på Linux och Solaris
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Avinstallation på Linux och Solaris{#uninstalling-on-linux-and-solaris}

Följ dessa anvisningar för att avinstallera bildåtergivning på ett Linux- eller Solaris-system.

Det finns två sätt att avinstallera bildåtergivning på ett Linux- eller Solaris-system.

**Metod 1**

1. Sök [!DNL uninstall.sh].

   Den finns i den katalog som ImageRendering installerades från. Om den här katalogen har tagits bort måste det ursprungliga installationspaketet vara okomprimerat och obearbetat för att kunna extrahera [!DNL uninstall.sh].
1. Kör [!DNL uninstall.sh] och följ instruktionerna på skärmen.

>**Metod 2**
>
>1. Stoppa ImageRendering med: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Ta bort ImageRendering från datorn.

>
>   
Kommandot för att ta bort ImageRendering beror på datorn:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Ta bort kataloger eller filer som inte har tagits bort i steg 2.

>


