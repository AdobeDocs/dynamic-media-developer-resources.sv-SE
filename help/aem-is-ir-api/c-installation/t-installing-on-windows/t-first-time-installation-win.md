---
description: Följ de här stegen för att installera Image Serving för första gången på Windows.
seo-description: Följ de här stegen för att installera Image Serving för första gången på Windows.
seo-title: Installerar för första gången
solution: Experience Manager
title: Installerar för första gången
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Installerar för första gången{#installing-for-the-first-time}

Följ de här stegen för att installera Image Serving för första gången på Windows.

1. Logga in på servervärden med administratörsbehörighet.
1. Om du redan har fått en licens kopierar du den till servern och kör sedan licensinstallationen genom att dubbelklicka på filen.

   Om du ännu inte har någon licens kan du fortsätta med installationen och installera licensen senare.
1. Extrahera innehållet i ZIP-filen Image Serving distribution.
1. Kör [!DNL setup]/ [!DNL setup.exe] för att starta installationsguiden.
1. Klicka på Nästa om du vill gå vidare till slutanvändaravtalet (EULA), läsa licensavtalet och klicka på **[!UICONTROL Ja]**.

   Dialogrutan [!DNL Authentication] visas.
1. Om en licens redan är installerad och licensinformationen visas i [!DNL Authentication] dialogrutan klickar du på **[!UICONTROL Nästa]** för att fortsätta.

   Om du inte har någon licens klickar du på **[!UICONTROL Begär licens]**. I nästa dialogruta visas en av datorns MAC-adresser för nätverkskort. Skicka den här MAC-adressen, ditt företagsnamn och den produkt du installerar enligt instruktionerna i meddelandet.

   **Viktigt:** Licensen baseras på MAC-adressen för ett av de nätverkskort som är installerade på värden. Om du inaktiverar, tar bort eller byter ut kortet kommer licensen inte längre att godkännas. Var noga med att skaffa en licens för den maskinvarukonfiguration som du ska använda för IS.

   Du kan fortsätta installera IS utan giltig licens och installera licensen senare. Klicka på **[!UICONTROL Bakåt]** för att gå tillbaka till [!DNL Authentication] dialogrutan och klicka sedan på **[!UICONTROL Nästa]**.
1. Gå till sidan Inställningar för plattformsserveradministratör. Ange nya värden efter behov eller godkänn standardvärdena.

   Du kan konfigurera följande objekt:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> HTTP-anslutningsport för plattformsserver </p> </td> 
   <td> <p>HTTP-huvudavlyssningsporten för bildservrar och bildåtergivning </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Admin Listingport </p> </td> 
   <td> <p>Admin Listingport </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Plattformsserverns cachestorlek i MB </p> </td> 
   <td> <p>Startstorlek för cachen för huvudsvar </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Plats för Plattform för servercache </p> </td> 
   <td> <p>PS-cachemapp </p> </td> 
  </tr> 
 </tbody> 
</table>

De angivna portnumren måste vara unika och inte användas av andra program eller tjänster.

På nästa skärm kan du granska de valda inställningarna.
1. Klicka på **[!UICONTROL Bakåt]** för att göra ändringar eller klicka på **[!UICONTROL Nästa]** för att starta installationen.
1. Klicka på **[!UICONTROL Slutför]** för att avsluta installationsguiden.
