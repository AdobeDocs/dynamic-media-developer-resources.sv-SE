---
description: Följ dessa anvisningar för att avinstallera bildåtergivning på ett Linux- eller Solaris-system.
solution: Experience Manager
title: Avinstallation på Linux och Solaris
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Avinstallerar Linux och Solaris{#uninstalling-on-linux-and-solaris}

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



