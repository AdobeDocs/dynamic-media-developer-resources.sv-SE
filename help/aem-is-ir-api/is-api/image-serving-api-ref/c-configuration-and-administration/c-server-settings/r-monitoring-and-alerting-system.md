---
description: Använd de här serverinställningarna för att konfigurera övervaknings- och varningssystemet.
seo-description: Använd de här serverinställningarna för att konfigurera övervaknings- och varningssystemet.
seo-title: Övervaknings- och varningssystem
solution: Experience Manager
title: Övervaknings- och varningssystem
topic: Scene7 Image Serving - Image Rendering API
uuid: 944c7d53-09ec-443e-ac8c-85684d8fda0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Övervaknings- och varningssystem{#monitoring-and-alerting-system}

Använd de här serverinställningarna för att konfigurera övervaknings- och varningssystemet.

## AS::monitorAlertGenerator.enableGlobalAlerting - Aktivera varningssystemet {#section-612f8ea61794426ab205e22e5f665fa9}

Aktivera e-postmeddelanden genom att ange true och konfigurera inställningarna för e-postmeddelanden. Inställning för att `false` inaktivera alla e-postaviseringar - det kan vara användbart när en server är offline för underhåll. Boolean.

## AS::mailSender.host - SMTP Host {#section-151df07e7b44446581339bb7abeeba7a}

IP-adressen för SMTP-e-postservern.

## AS::mailSender.port - SMTP-port {#section-4b25efca8fd84d5c92dafacd0555e99d}

Lyssnarporten för SMTP-e-postservern.

## AS::monitorAlertGenerator.messageTo - meddelandemottagare {#section-0017bbaa15434117a70900c3f1163960}

En eller flera e-postadresser dit aviseringar ska skickas. Använd semikolon som avgränsare.

## AS::monitorAlertGenerator.messageFrom - meddelandeavsändare {#section-db320cba4ac2438ca1cfe6abce4aed87}

E-postadressen som ska användas i fältet **[!UICONTROL Från]** e-post.

## AS::monitorAlertGenerator.alertInterval - övervakningsintervall {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Övervakningssystemet kommer att samla in aviseringsvillkor under aviseringsintervallet och skicka ett e-postmeddelande med alla ackumulerade aviseringar i slutet av varje intervall. Millisekunder, heltalsvärde, 60000 eller mer. Vanligtvis inställt på 5 eller 10 minuter.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Varningsintervall för heap-space {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Minimitid efter att ett heap space-varningsmeddelande har skickats innan ett annat skickas. Intervalltid i msek. Heltalsvärde, 0 eller större.

## AS::monitorAlertGenerator.minTrafficForAlerts - Minsta trafik för att aktivera larm {#section-8b4db2d6f96642309ca35c49eb3ab230}

Begäranden per sekund. Ingen svarstid och felmeddelanden kommer att utlösas om trafiken faller under detta tröskelvärde. Ange 0 om du vill skicka svarstid och felmeddelanden oavsett trafikvolym. Verkligt värde 0 eller större.
