---
title: Uppdaterar från IS 4.7.4 eller senare
description: Gör så här när du uppgraderar Dynamic Media Image Serving på Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Uppdaterar från IS 4.7.4 eller senare{#updating-from-is-or-later}

Gör så här när du uppgraderar Dynamic Media Image Serving på Linux®.

Om du uppgraderar från en äldre version av Image Serving kontaktar du supporten för rätt process.

The [!DNL webapps] kan tas bort vid uppgradering. Säkerhetskopiera [!DNL webapps] mapp före uppgradering.

1. Logga in på servervärden med rotprivilegier.
1. Ta bort komprimeringen och ta bort kontrollen för Image Serving-distributionens tjärfil.
1. I [!DNL setup] mapp, köra [!DNL `./install-is`] för att starta installationsguiden.

   Installationsprogrammet för uppdateringen kontrollerar det installerade paketets integritet och version. Om det lyckas visas slutanvändaravtalet (&quot;EULA&quot;).
1. Läs licensavtalet och ange **[!UICONTROL y]** för att fortsätta med installationen.

   Installationsprogrammet säkerhetskopierar de gamla serverkonfigurationsfilerna till [!DNL BACKUP/] mapp.

   När installationen är klar visas följande meddelande:

   `Image Server was started successfully`

Under en uppdatering [!DNL ImageServing/conf/server.xml] filen uppdateras till de senaste inställningarna. Om du har ändrat eller lagt till värden sparar du dina befintliga [!DNL server.xml] och implementera ändringarna igen efter uppgraderingen.

Efter en uppdateringsinstallation bör du överväga att värma upp HTTP-svarscachen innan servern aktiveras. Se beskrivningen av [!DNL playlog] verktyg för mer information.
