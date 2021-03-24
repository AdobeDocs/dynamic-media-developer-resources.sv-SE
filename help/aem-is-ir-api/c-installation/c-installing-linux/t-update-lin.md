---
description: Använd den här proceduren när du uppgraderar Dynamic Media Image Serving i Linux.
solution: Experience Manager
title: Uppdaterar från IS 4.7.4 eller senare
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Uppdaterar från IS 4.7.4 eller senare{#updating-from-is-or-later}

Använd den här proceduren när du uppgraderar Dynamic Media Image Serving i Linux.

Om du uppgraderar från en äldre version av Image Serving kontaktar du supporten för rätt process.

Mappen [!DNL webapps] kan tas bort vid uppgradering. Säkerhetskopiera mappen [!DNL webapps] innan du uppgraderar.

1. Logga in på servervärden med rotprivilegier.
1. Ta bort komprimeringen och ta bort kontrollen för Image Serving-distributionens tjärfil.
1. Kör [!DNL ./install-is] för att starta installationsguiden som finns i mappen [!DNL setup].

   Installationsprogrammet för uppdateringen kontrollerar det installerade paketets integritet och version. Om det lyckas visas slutanvändaravtalet (&quot;EULA&quot;).
1. Läs licensavtalet och ange **[!UICONTROL y]** för att fortsätta med installationen.

   Installationsprogrammet säkerhetskopierar de gamla serverkonfigurationsfilerna till mappen [!DNL BACKUP/].

   När installationen är klar visas följande meddelande:

   `Image Server was started successfully`

Under en uppdatering uppdateras [!DNL ImageServing/conf/server.xml]-filen till de senaste inställningarna. Om du har ändrat eller lagt till värden bör du spara dina befintliga [!DNL server.xml] och implementera ändringarna igen efter uppgraderingen.

Efter en uppdateringsinstallation bör du överväga att värma upp HTTP-svarscachen innan servern aktiveras. Mer information finns i beskrivningen av verktyget [!DNL playlog].
