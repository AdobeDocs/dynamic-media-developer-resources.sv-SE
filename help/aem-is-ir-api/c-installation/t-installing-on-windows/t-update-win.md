---
description: Använd den här proceduren när du uppgraderar Dynamic Media Image Serving.
solution: Experience Manager
title: Uppdaterar från IS 4.7.4 eller senare
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Uppdaterar från IS 4.7.4 eller senare{#updating-from-is-or-later}

Använd den här proceduren när du uppgraderar Dynamic Media Image Serving.

Om du uppgraderar från en äldre version av Image Serving kontaktar du supporten för rätt process.

>[!NOTE]
>
>Mappen [!DNL webapps] kan tas bort vid uppgradering. Säkerhetskopiera mappen [!DNL webapps] innan du uppgraderar.

1. Logga in på servervärden med administratörsbehörighet.
1. Extrahera innehållet i ZIP-filen Image Serving distribution.
1. Kör setup/setup.exe för att starta installationsguiden.
1. Klicka på **[!UICONTROL Next]** om du vill gå vidare till slutanvändaravtalet (EULA), läsa licensavtalet och klicka på **[!UICONTROL Yes]**.

   På nästa sida visas de tidigare konfigurationsinställningarna.
1. Klicka på **[!UICONTROL Next]** för att starta uppdateringsinstallationen.

   >[!NOTE]
   >
   >Installationsprogrammet säkerhetskopierar de gamla serverkonfigurationsfilerna till mappen [!DNL BACKUP/].

1. När installationen är klar klickar du på Slutför för att avsluta installationsguiden.

   I vissa fall kan installationsguiden be om att starta om systemet.

Under en uppdatering uppdateras [!DNL ImageServing/conf/server.xml]-filen till de senaste inställningarna. Om du har ändrat eller lagt till värden bör du spara dina befintliga [!DNL server.xml] och implementera ändringarna igen efter uppgraderingen.

Efter en uppdateringsinstallation bör du överväga att värma upp HTTP-svarscachen innan servern aktiveras. Mer information finns i beskrivningen av verktyget `playlog`.
