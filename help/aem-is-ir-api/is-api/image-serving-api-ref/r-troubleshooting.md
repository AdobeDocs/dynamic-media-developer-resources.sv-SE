---
description: Det här avsnittet innehåller lösningar på problem som ibland har uppstått med Image Serving.
seo-description: Det här avsnittet innehåller lösningar på problem som ibland har uppstått med Image Serving.
seo-title: Felsökning
solution: Experience Manager
title: Felsökning
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---


# Felsökning{#troubleshooting}

Det här avsnittet innehåller lösningar på problem som ibland har uppstått med Image Serving.

**Allmänt**

ImageServer sparar nu en installationslogg och en säkerhetskopiemapp med alla filer som ändrats under en uppgraderingsinstallation. Den här filen och mappen finns i roten av installationskatalogen för Image Serving.

**När du startar Image Server stoppas startskriptet med meddelandet &quot;start pending&quot; (endast LINUX)**

Detta kan tyda på ett problem med Image Serving License, t.ex. en saknad licensfil eller en utgången tillfällig licens. En giltig licensfil måste finnas i [!DNL /usr/local/scene7/licenses].

**Image Server stoppas eller kraschar och loggfilen för Image Server anger inte tillräckligt med utrymme eller &quot;resursen är tillfälligt otillgänglig i filen  [!DNL IgcVirtualMemory.cpp]&quot;**

Orsaken till det här felmeddelandet är att det inte gick att tilldela den mängd minne som Image Server konfigurerats att använda.

* Kontrollera inställningen Fysiskt minne i [!DNL ImageServerRegistry.xml]. Det får inte vara mer än 50 %, vilket är mindre om andra minnesintensiva program körs på samma system. Standardvärdet är 20 %.
* Kontrollera att växlingsutrymmet på servern är minst dubbelt så stort som det fysiska RAM-minnet. Låga inställningar för växlingsbart utrymme kan orsaka det här problemet.

**Det faktiska diskutrymme som används av cachemappen överskrider  ` *[!DNL cache.maxSize]*`inställningen[!DNL PlatformServer.conf]**

Detta tyder inte på något problem. Filsystemsrubriken ingår inte i plattformsserverns inställning för diskcache. Det totala belopp som rapporteras av systemet kan vara betydligt större än inställningen. Vi rekommenderar att du reserverar dubbelt så mycket diskutrymme som du har angett i ` *[!DNL cache.maxSize]*`.

**Brutna bilder i exemplen i is-docs**

Detta inträffar om Image Server inte körs. Det inträffar också om katalogrotsökvägen eller bildrotsökvägen har ändrats från standardinställningen för installation, men exempelbilderna och katalogerna har inte flyttats till de nya platserna. Kontrollera bildserverns rotsökväg i konfigurationsfilerna. Om det behövs flyttar du demomappen som innehåller exempelbilderna till den aktuella bildroten och flyttar [!DNL sample*.*] till den aktuella katalogroten.

Exemplen förutsätter också att vissa inställningar i [!DNL default.ini] är standard (t.ex. att döljning eller låsning inte får vara aktiverat).

**För många cachemissar efter omfattande drifttid**

Beroende på serveranvändningen kan prestanda förbättras genom att storleken på plattformsserverns diskcache ökas om det finns tillgängligt diskutrymme. Du kan ändra inställningarna genom att redigera konfigurationsfiler manuellt. Se dokumentationen.

**Loggfiler tar upp för mycket diskutrymme**

Image Server och Platform Server startar en ny loggfil varje dag. Som standard placeras dessa i [!DNL *[!DNL install_root]*/ImageServing/logs]. Loggfilens storlek, antal lagrade loggar och logginnehåll kan konfigureras. Se dokumentationen.

**Om du har ett antivirusprogram installerat på servern**

Vi rekommenderar att du inaktiverar skanning för Image Serving-kataloger. I annat fall uppstår problem om du skannar läs-/skrivkataloger med stora volymer (till exempel cache, bilder, teckensnitt, profiler och kataloger).

**Digimarc orsakar prestandaproblem för zoombilder**

Använd inte Digimarc på bilder som ska zoomas. Prestandan är inte acceptabel. Om det behövs skapar du en separat katalog för bilder som ska användas för zoomning och inaktiverar Digimarc för den här katalogen.
