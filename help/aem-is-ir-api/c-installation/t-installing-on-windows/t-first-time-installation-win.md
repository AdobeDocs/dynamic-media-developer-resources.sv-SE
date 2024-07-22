---
title: Installerar för första gången
description: Följ de här stegen för att installera Image Serving för första gången på Windows.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Installerar för första gången{#installing-for-the-first-time}

Följ de här stegen för att installera Image Serving för första gången på Windows.

1. Logga in på servervärden med administratörsbehörighet.
1. Om du redan har fått en licens kopierar du den till servern och kör sedan licensinstallationen genom att dubbelklicka på filen.

   Om du ännu inte har någon licens kan du fortsätta med installationen och installera licensen senare.

1. Extrahera innehållet i ZIP-filen Image Serving distribution.
1. Starta installationsguiden genom att köra [!DNL setup]/ [!DNL setup.exe].
1. Välj **[!UICONTROL Next]** om du vill gå vidare till slutanvändarlicensavtalet (EULA), läsa licensavtalet och välja **[!UICONTROL Yes]**.

   Dialogrutan [!DNL Authentication] visas härnäst.
1. Om en licens redan är installerad och licensinformationen visas i dialogrutan [!DNL Authentication] väljer du **[!UICONTROL Next]** för att fortsätta.

   Om du inte har någon licens väljer du **[!UICONTROL Request License]**. I nästa dialogruta visas en av datorns MAC-adresser för nätverkskort. Mejla den här MAC-adressen, ditt företagsnamn och den produkt du installerar enligt anvisningarna i meddelandet.

   **Viktigt!** Licensen baseras på MAC-adressen för ett av de nätverkskort som är installerade på värden. Om du inaktiverar, tar bort eller byter ut kortet känns inte licensen längre som giltig. Se till att du får en licens för den maskinvarukonfiguration som du använder för Image Serving.

   Du kan fortsätta installera IS utan giltig licens och installera licensen senare. Om du vill fortsätta väljer du **[!UICONTROL Back]** för att återgå till dialogrutan [!DNL Authentication] och väljer sedan **[!UICONTROL Next]**.
1. Gå till sidan [!DNL Platform Server] Administratörsinställningar. Ange nya värden efter behov eller godkänn standardvärdena.

   Du kan konfigurera följande objekt:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP-anslutningsport </p> </td>
      <td> <p>HTTP-huvudavlyssningsporten för bildservrar och bildåtergivning </p> </td>
   </tr> 
   <tr> 
      <td> <p> Admin Listingport </p> </td>
      <td> <p>Admin Listingport </p> </td>
   </tr> 
   <tr> 
      <td> <p> Cachestorlek för [!DNL Platform Server] i MB </p> </td>
      <td> <p>Startstorlek för cachen för huvudsvar </p> </td>
   </tr>
   <tr> 
      <td> <p> Cacheplats för [!DNL Platform Server] </p> </td>
      <td> <p>PS-cachemapp </p> </td>
   </tr>
   </tbody>
   </table>

   De angivna portnumren måste vara unika och inte användas av andra program eller tjänster.

   På nästa skärm kan du granska de valda inställningarna.

1. Välj **[!UICONTROL Back]** om du vill göra ändringar eller välj **[!UICONTROL Next]** om du vill starta installationen.

1. Välj **[!UICONTROL Finish]** om du vill avsluta installationsguiden.
