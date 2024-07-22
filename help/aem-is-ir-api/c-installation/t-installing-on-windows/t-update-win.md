---
title: Uppdaterar från IS 4.7.4 eller senare
description: Använd den här proceduren när du uppgraderar Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
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
1. Starta installationsguiden genom att köra `setup/setup.exe`.
1. Välj **[!UICONTROL Next]** om du vill gå vidare till slutanvändarlicensavtalet (EULA), läsa licensavtalet och välja **[!UICONTROL Yes]**.

   På nästa sida visas tidigare konfigurationsinställningar.
1. Klicka på **[!UICONTROL Next]** för att starta uppdateringsinstallationen.

   >[!NOTE]
   >
   >Installationsprogrammet säkerhetskopierar de gamla serverkonfigurationsfilerna till mappen [!DNL BACKUP/].

1. När installationen är klar väljer du **[!UICONTROL Finish]** för att avsluta installationsguiden.

   Ibland kan installationsguiden be dig starta om systemet.

Under en uppdatering uppdateras filen [!DNL ImageServing/conf/server.xml] till de senaste inställningarna. Om du har ändrat eller lagt till några värden bör du spara dina befintliga [!DNL server.xml] och implementera ändringarna igen efter uppgraderingen.

Efter en uppdateringsinstallation bör du överväga att värma upp HTTP-svarscachen innan servern aktiveras. Mer information finns i beskrivningen av verktyget `playlog`.
