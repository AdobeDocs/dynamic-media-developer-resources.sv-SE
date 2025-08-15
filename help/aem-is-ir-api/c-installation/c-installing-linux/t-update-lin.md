---
title: Uppdaterar från IS 4.7.4 eller senare
description: Använd den här proceduren när du uppgraderar Dynamic Media Image Serving i Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Uppdaterar från IS 4.7.4 eller senare{#updating-from-is-or-later}

Använd den här proceduren när du uppgraderar Dynamic Media Image Serving i Linux®.

Om du uppgraderar från en äldre version av Image Serving kontaktar du supporten för rätt process.

Mappen [!DNL webapps] kan tas bort vid uppgradering. Säkerhetskopiera mappen [!DNL webapps] innan du uppgraderar.

1. Logga in på servervärden med rotprivilegier.
1. Ta bort komprimeringen och ta bort kontrollen för Image Serving-distributionens tjärfil.
1. Kör [!DNL setup] i mappen [!DNL `./install-is`] för att starta installationsguiden.

   Installationsprogrammet för uppdateringen kontrollerar det installerade paketets integritet och version. Om det lyckas visas slutanvändaravtalet (&quot;EULA&quot;).
1. Läs licensavtalet och ange sedan **[!UICONTROL y]** för att fortsätta med installationen.

   Installationsprogrammet säkerhetskopierar de gamla serverkonfigurationsfilerna till mappen [!DNL BACKUP/].

   När installationen är klar visas följande meddelande:

   `Image Server was started successfully`

Under en uppdatering uppdateras filen [!DNL ImageServing/conf/server.xml] till de senaste inställningarna. Om du har ändrat eller lagt till några värden sparar du dina befintliga [!DNL server.xml] och implementerar ändringarna igen efter uppgraderingen.

Efter en uppdateringsinstallation bör du överväga att värma upp HTTP-svarscachen innan servern aktiveras. Mer information finns i beskrivningen av verktyget [!DNL playlog].
