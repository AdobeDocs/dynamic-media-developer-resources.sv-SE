---
description: Följ dessa anvisningar för att avinstallera bildåtergivning på ett Linux- eller Solaris-system.
seo-description: Följ dessa anvisningar för att avinstallera bildåtergivning på ett Linux- eller Solaris-system.
seo-title: Avinstallation på Linux och Solaris
solution: Experience Manager
title: Avinstallation på Linux och Solaris
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
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



