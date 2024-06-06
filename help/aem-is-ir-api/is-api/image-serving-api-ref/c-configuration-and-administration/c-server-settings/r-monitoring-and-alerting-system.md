---
description: Använd de här serverinställningarna för att konfigurera övervaknings- och varningssystemet.
solution: Experience Manager
title: Övervaknings- och varningssystem
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Övervaknings- och varningssystem{#monitoring-and-alerting-system}

Använd de här serverinställningarna för att konfigurera övervaknings- och varningssystemet.

## AS::monitorAlertGenerator.enableGlobalAlerting - Aktivera varningssystemet {#section-612f8ea61794426ab205e22e5f665fa9}

Aktivera e-postmeddelanden genom att ange true och konfigurera inställningarna för e-postmeddelanden. Inställning till `false` stänger av alla e-postaviseringar - det kan vara användbart när en server är offline för att underhållas. Boolean.

## AS::mailSender.host - SMTP Host {#section-151df07e7b44446581339bb7abeeba7a}

IP-adressen för SMTP-e-postservern.

## AS::mailSender.port - SMTP-port {#section-4b25efca8fd84d5c92dafacd0555e99d}

Lyssnarporten för SMTP-e-postservern.

## AS::monitorAlertGenerator.messageTo - meddelandemottagare {#section-0017bbaa15434117a70900c3f1163960}

En eller flera e-postadresser dit aviseringar ska skickas. Använd semikolon som avgränsare.

## AS::monitorAlertGenerator.messageFrom - meddelandeavsändare {#section-db320cba4ac2438ca1cfe6abce4aed87}

E-postadressen som ska användas i **[!UICONTROL From]** e-postfält.

## AS::monitorAlertGenerator.alertInterval - övervakningsintervall {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Övervakningssystemet samlar in aviseringsvillkor under aviseringsintervallet och skickar ett e-postmeddelande med alla ackumulerade aviseringar i slutet av varje intervall. Millisekunder, heltalsvärde, 60000 eller mer. Vanligtvis inställt på 5 eller 10 minuter.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Varningsintervall för heap-space {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Minimitid efter att ett heap space-varningsmeddelande har skickats innan ett annat skickas. Intervalltid i ms. Heltalsvärde, 0 eller större.

## AS::monitorAlertGenerator.minTrafficForAlerts - Minsta trafik för att aktivera larm {#section-8b4db2d6f96642309ca35c49eb3ab230}

Begäranden per sekund. Ingen svarstid och felmeddelanden skickas om trafiken faller under detta tröskelvärde. Ange 0 om du vill skicka svarstid och felmeddelanden oavsett trafikvolym. Verkligt värde 0 eller större.
