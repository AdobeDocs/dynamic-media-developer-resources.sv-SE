---
description: Den här proceduren visar hur du installerar Image Serving för första gången i Linux.
solution: Experience Manager
title: Installerar för första gången
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Installerar för första gången{#installing-for-the-first-time}

Den här proceduren visar hur du installerar Image Serving för första gången i Linux.

1. Logga in på servervärden med rotbehörigheter.
1. Skapa mappen [!DNL /usr/local/scene7/licenses].

   Om licensnyckelfilen för Image Serving och/eller Image Rendering (med filsuffixet [!DNL .sc8]) är tillgänglig kopierar du den till den här mappen. Annars fortsätter du med installationen och installerar licensnyckeln senare.
1. Ta bort komprimeringen och ta bort kontrollen för Image Serving-distributionens tjärfil.
1. Kör [!DNL ./install-is] i mappen [!DNL Setup] för att starta installationsguiden.

   Om ingen licensnyckel hittas visas instruktioner som beskriver hur du hämtar en licensfil. Gör det nu eller fortsätt med installationen av Image Serving och installera licensnyckeln senare.
1. När slutanvändarlicensavtalet (EULA) visas läser du licensavtalet och anger `y` för att fortsätta.

   Installationsprogrammet visar de uppmaningar som anges i följande tabell.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Huvudavlyssningsport [8080]:</span> </p> </td> 
   <td colname="col2"> <p>HTTP-huvudavlyssningsporten för Image Serving och Image Rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Admin Listening Port [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Admin-lyssningsporten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximal storlek för HTTP-cache (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Startstorlek för cachen för huvudsvar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cacherotmapp [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS-cachemapp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Owner ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>Det användarkonto som Image Serving-servrar ska installeras under. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Group ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>Det gruppkonto som Image Serving-servrar ska installeras under. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Tryck på **[!UICONTROL Enter]** om du vill acceptera standardvärdet eller ange ett annat värde.

   Kontrollera att alla angivna portnummer är unika och inte används på annat sätt på den här värden.

   >[!IMPORTANT]
   >
   >Om ett annat konto än roten anges måste du se till att åtkomstbehörigheterna för alla filer och mappar som Image Server behöver för att läsa och/eller skriva är korrekt konfigurerade när dessa mappar konfigureras om i konfigurationsfilerna.
   >
   >Image Serving är nu installerat på [!DNL /usr/local/Scene7/ImageServing]. Visst bildåtergivningsinnehåll är installerat på [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Installationsguiden försöker starta Image Server mot slutet av installationen. Om ingen giltig licensnyckel hittas kan inte Image Server starta. Om det finns en giltig licens och Image Server fortfarande inte startas, bör du läsa loggfilerna.

>[!NOTE]
>
>Om licensen har installerats efter installation av Image Serving måste Image Server startas manuellt innan den används.
