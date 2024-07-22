---
title: Systemkrav och krav
description: Kontrollera att datorn uppfyller systemkraven innan du använder Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Systemkrav och krav{#system-requirements-and-prerequisites}

Kontrollera att datorn uppfyller systemkraven innan du använder Dynamic Media Image Serving.

## Servermaskinvara {#section-f3c14a7bc1b745118602659628df779f}

Servern bör uppfylla följande maskinvarukrav.

>[!NOTE]
>
>System med processorer med AMD64 och Intel® EM64T är vanligtvis konfigurerade som NUMA-plattformar (Non-Uniform Memory Architecture). Detta innebär att kärnan konstruerar flera minnesnoder vid start i stället för att konstruera en enda minnesnod. Konstruktionen för flera noder kan resultera i minnesöverbelastning på en eller flera av noderna innan andra noder töms. När minnesöverbelastning inträffar kan kärnan bestämma sig för att avsluta processer (till exempel Image Server eller [!DNL Platform Server]) trots att det finns tillgängligt minne. Därför rekommenderar Adobe att du stänger av NUMA om du kör ett sådant system. Använd startalternativet `numa=off` för att undvika att kärnan stoppar dessa processer.

**Windows**

* Intel Xeon®- eller AMD® Opteron-processor med minst fyra kärnor.
* Minst 1 GB RAM-minne.
* Växlingsutrymmet är minst dubbelt så stort som mängden fysiskt minne (RAM).
* 2 GB ledigt hårddiskutrymme för installation och grundläggande funktioner. Ytterligare diskutrymme krävs för källbilder, loggar, datacache och manifestfiler.
* Fast Ethernet-nätverkskort.

**Linux®**

* Intel Xeon®- eller AMD® Opteron-processor med minst fyra kärnor.
* Minst 16 GB RAM-minne.
* Växling är inaktiverat (rekommenderas).
* 2 GB ledigt hårddiskutrymme för installation och grundläggande funktioner. Ytterligare diskutrymme krävs för källbilder, loggar, datacache och manifestfiler.
* Fast Ethernet-nätverkskort.

**Obs! (Linux®):** Bildservern fungerar inte med SELinux aktiverat. Det här alternativet är aktiverat som standard. Om du vill inaktivera SELinux redigerar du filen [!DNL /etc/selinux/config] och ändrar SELinux-värdet från:

`SELINUX=enforcing`

Till

`SELINUX=disabled`

**Obs! (Linux®):** Kontrollera att serverns värdnamn kan matchas till en IP-adress. Om det inte är möjligt lägger du till det fullständiga, kvalificerade värdnamnet och IP-adressen till [!DNL /etc/hosts] som i följande exempel.

`<ip address> <fully qualified hostname>`

## Serverprogramvara {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving kräver följande serverprogramvara.

**Windows**

* Microsoft® Windows Server 2008.
* 64-bitars operativsystem.

**Linux®**

* Red Hat® Enterprise 5 eller CentOS 5.5 och senare med de senaste korrigeringsfilerna.
* 64-bitars operativsystem.

**Obs!** Om du vill använda Image Serving i Windows måste du installera Microsoft® Visual Studio 2010.
