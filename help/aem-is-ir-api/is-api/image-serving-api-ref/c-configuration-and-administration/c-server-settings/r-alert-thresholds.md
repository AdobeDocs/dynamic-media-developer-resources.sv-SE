---
description: Använd de här serverinställningarna för att konfigurera tröskelvärden för aviseringar.
solution: Experience Manager
title: Varningströsklar
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Varningströsklar{#alert-thresholds}

Använd de här serverinställningarna för att konfigurera tröskelvärden för aviseringar.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

En svarstidsvarning skickas när den genomsnittliga tiden för behandling av en begäran under samplingsintervallet överskrider det tröskelvärde som anges här. Uttryckt i msek; heltal 0 eller större. Typiska värden är mellan 100 och 1000 msek, beroende på hur komplexa åtgärderna är.

>[!NOTE]
>
>Begäranden som resulterar i svarsstatus 4xx eller 5xx beaktas inte för den här aviseringen.

## AS::monitorAlertGenerator.maxErrorRate - Tröskelvärde för felsvar AS::monitorAlertGenerator.maxErrorRate - Svarsfrekvens för fel {#section-76ba77fd3102419395e0f86719a1f3ec}

En felvarning utfärdas när förhållandet mellan HTTP-felsvar och totalt antal svar under samplingsintervallet överskrider det angivna tröskelvärdet.

Reellt värde mellan 0,0 och 1,0. Vanligtvis inställt på mellan 0,005 och 0,1. Ange 1 om du vill inaktivera felaviseringar.

## AS::monitorAlertGenerator.minRequestRate - Lågt tröskelvärde för trafik {#section-8dfb89ed138640fd86f5ce1dae2a533e}

En minsta trafikvarning skickas när det genomsnittliga antalet begäranden per sekund som tagits emot under det aktuella provtagningsintervallet underskrider detta tröskelvärde. Inaktivera varningen genom att ange värdet 0. Uttryckt i begäranden per sekund. Verkligt värde 0 eller större.

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space Threshold {#section-ce6705045f6842769030ccb1894594cc}

Anger det minsta lediga Java-heap-utrymmet. En prioritetsvarning skickas omedelbart efter en skräpinsamlingscykel för Java när det lediga stackutrymmet är under detta tröskelvärde. 50 MB rekommenderas för säker användning av [!DNL Platform Server]. Om du behåller det kostnadsfria stackutrymmet ovanför det här värdet minskas frekvensen för skräpinsamlingscykler, vilket kan förbättra serverprestanda generellt. Heltalsvärde i byte, 0 eller större.

## AS::monitorAlertGenerator.maxOverlap - Maximalt antal samtidiga begäranden {#section-ddc6925bff944758ab19bcc9cf3f2589}

En överlappningsvarning utlöses när det genomsnittliga antalet begäranden som behandlas samtidigt under det genomsnittliga intervallet överskrider detta tröskelvärde. En hög överlappning kan tyda på ett möjligt serveröverlagringsvillkor.

Heltalsvärde 1 eller högre. Normalt intervall är 20 till 50, beroende på cachens träffhastighet och begäranens komplexitet.

## AS::monitorAlertGenerator.lockedThreshold - låst begärandetröskelvärde {#section-012a1c9937d445708380339279c62d80}

Anger hur många sekunder en begäran måste vara väntande innan den betraktas som låst eller avbruten. En varning om låst begäran utfärdas om minst en begäran har varit väntande längre än den angivna tidsperioden i slutet av ett genomsnittligt intervall. Positivt heltalsvärde i ms.

Om du vill ta hänsyn till komplexa återgivningsbegäranden och begäranden som kräver att data hämtas från externa HTTP-servrar, bör du ange det här värdet till minst 30 sekunder (om inte ett sådant villkor identifieras av den här varningen).
