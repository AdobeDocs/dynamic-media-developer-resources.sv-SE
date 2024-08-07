---
description: Det här avsnittet innehåller lösningar på problem som ibland har uppstått med Image Serving.
solution: Experience Manager
title: Felsökning
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Felsökning{#troubleshooting}

Det här avsnittet innehåller lösningar på problem som ibland har uppstått med Image Serving.

**Allmänt**

ImageServer sparar nu en installationslogg och en säkerhetskopiemapp med alla filer som ändrats under en uppgraderingsinstallation. Den här filen och mappen finns i roten av installationskatalogen för Image Serving.

**När du startar Image Server stoppas startskriptet med meddelandet &quot;start pending&quot; (endast LINUX)**

Detta kan tyda på ett problem med Image Serving License, till exempel en saknad licensfil eller en utgången tillfällig licens. En giltig licensfil måste finnas i [!DNL /usr/local/scene7/licenses].

**Bildservern stoppas eller kraschar och loggfilen för bildservern anger inte tillräckligt med utrymme eller &quot;resursen är tillfälligt otillgänglig i filen [!DNL IgcVirtualMemory.cpp]&quot;**

Orsaken till det här felmeddelandet är att det inte gick att tilldela den mängd minne som Image Server konfigurerats att använda.

* Kontrollera inställningen för fysiskt minne i [!DNL ImageServerRegistry.xml]. Det får inte vara mer än 50 %, vilket är mindre om andra minneskrävande program körs i samma system. Standardvärdet är 20 %.
* Kontrollera att växlingsutrymmet på servern är minst dubbelt så stort som det fysiska RAM-minnet. Låga inställningar för växlingsbart utrymme kan orsaka det här problemet.

**Det faktiska diskutrymme som används av cachemappen överskrider ` *[!DNL cache.maxSize]*`som angetts i[!DNL PlatformServer.conf]**

Detta tyder inte på något problem. Filsystemets overhead ingår inte i diskcacheinställningen för [!DNL Platform Server]. Det totala belopp som rapporteras av systemet kan vara betydligt större än inställningen. Vi rekommenderar att du reserverar dubbelt så mycket diskutrymme som du har angett i ` *[!DNL cache.maxSize]*`.

**Brutna bilder i is-docs-exemplen**

Detta inträffar om Image Server inte körs. Det inträffar också om katalogrotsökvägen eller bildrotsökvägen har ändrats från standardinställningen för installation, men exempelbilderna och katalogerna har inte flyttats till de nya platserna. Kontrollera bildserverns rotsökväg i konfigurationsfilerna. Flytta vid behov demomappen som innehåller exempelbilderna till den aktuella bildroten och flytta [!DNL sample*.*] till den aktuella katalogroten.

Exemplen förutsätter också att vissa inställningar i [!DNL default.ini] är standard (t.ex. får döljning eller låsning inte vara aktiverat).

**För många cachemissar efter omfattande drifttid**

Beroende på serveranvändningen kan prestanda förbättras genom att öka storleken på diskcachen för [!DNL Platform Server] om det finns tillgängligt diskutrymme. Du kan ändra inställningarna genom att redigera konfigurationsfiler manuellt. Mer information finns i dokumentationen.

**Loggfiler tar upp för mycket diskutrymme**

Bildservern och [!DNL Platform Server] startar en ny loggfil varje dag. Som standard placeras dessa i [!DNL *[!DNL install_root]*/ImageServing/logs]. Loggfilens storlek, antal lagrade loggar och logginnehåll kan konfigureras. Mer information finns i dokumentationen.

**Om du har ett antivirusprogram installerat på servern**

Vi rekommenderar att du inaktiverar skanning för Image Serving-kataloger. I annat fall kan en skanning av läs-/skrivkataloger med stora volymer (till exempel cache, bilder, teckensnitt, profiler och kataloger) orsaka problem.

**Digimarc orsakar prestandaproblem för zoombilder**

Använd inte Digimarc på bilder som är zoomade. Prestandan är inte acceptabel. Om det behövs skapar du en separat katalog för bilder som ska användas för zoomning och inaktiverar Digimarc för den här katalogen.
