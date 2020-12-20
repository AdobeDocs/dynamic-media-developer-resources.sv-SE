---
description: Kontrollera att datorn uppfyller systemkraven innan du använder Scene7 Image Serving.
seo-description: Kontrollera att datorn uppfyller systemkraven innan du använder Scene7 Image Serving.
seo-title: Systemkrav och krav
solution: Experience Manager
title: Systemkrav och krav
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# Systemkrav och krav{#system-requirements-and-prerequisites}

Kontrollera att datorn uppfyller systemkraven innan du använder Scene7 Image Serving.

## Servermaskinvara {#section-f3c14a7bc1b745118602659628df779f}

Servern bör uppfylla följande maskinvarukrav.

>[!NOTE]
>
>System med processorer med AMD64 och Intel® EM64T är vanligtvis konfigurerade som NUMA-plattformar (Non-Uniform Memory Architecture). Detta innebär att kärnan konstruerar flera minnesnoder vid start i stället för att konstruera en enda minnesnod. Konstruktionen för flera noder kan resultera i minnesöverbelastning på en eller flera av noderna innan andra noder töms. När minnesöverbelastning inträffar kan kärnan bestämma sig för att avsluta processer (till exempel Image Server eller Platform Server) trots att det finns tillgängligt minne. Därför rekommenderar Adobe Systems att du stänger av NUMA om du kör ett sådant system. Använd startalternativet `numa=off` för att undvika att kärnan stoppar dessa processer.

**Windows**

* Intel Xeon®- eller AMD® Opteron-processor med minst fyra kärnor.
* Minst 16 GB RAM-minne.
* Växla utrymme motsvarande minst dubbelt så mycket fysiskt minne (RAM).
* 2 GB ledigt hårddiskutrymme för installation och grundläggande funktioner. Ytterligare diskutrymme krävs för källbilder, loggar, datacache och manifestfiler.
* Fast Ethernet-nätverkskort.

**Linux**

* Intel Xeon®- eller AMD® Opteron-processor med minst fyra kärnor.
* Minst 16 GB RAM-minne.
* Växling är inaktiverat (rekommenderas).
* 2 GB ledigt hårddiskutrymme för installation och grundläggande funktioner. Ytterligare diskutrymme krävs för källbilder, loggar, datacache och manifestfiler.
* Fast Ethernet-nätverkskort.

**Obs! (Linux):** Bildservrar fungerar inte när SELinux är aktiverat. Det här alternativet är aktiverat som standard. Om du vill inaktivera SELinux redigerar du filen [!DNL /etc/selinux/config] och ändrar SELinux-värdet från:

`SELINUX=enforcing`

till

`SELINUX=disabled`

**Obs! (Linux):** Kontrollera att serverns värdnamn kan matchas till en IP-adress. Om det inte är möjligt lägger du till det fullständiga, kvalificerade värdnamnet och IP-adressen till [!DNL /etc/hosts] som i följande exempel.

`<ip address> <fully qualified hostname>`

## Serverprogramvara {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Scene7 Image Serving kräver följande serverprogramvara.

**Windows**

* Microsoft® Windows 2008 Server.
* 64-bitars operativsystem.

**Linux**

* Red Hat® Enterprise 5 eller CentOS 5.5 och senare, med de senaste korrigeringsfilerna.
* 64-bitars operativsystem.

**Obs!** Om du vill använda Image Serving i Windows måste du installera Microsoft Visual Studio 2010 som kan distribueras om. Den kan distribueras på följande plats:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

