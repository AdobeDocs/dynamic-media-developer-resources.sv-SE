---
description: $var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om '?' avgränsar sökvägen från frågan.
solution: Experience Manager
title: Variabel bearbetning i kapslade begäranden
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Variabel bearbetning i kapslade begäranden{#variable-processing-in-nested-requests}

$var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om &#39;?&#39; avgränsar sökvägen från frågan.

Servern ersätter dessa referenser med värden (antingen från url eller `catalog::Modifier` i huvudbildkatalogen) innan den kapslade begäran analyseras och bearbetas ytterligare.

Dessutom vidarebefordras alla `$ *[!DNL var]*=`-definitioner från URL:en och `catalog::Modifier` till alla kapslade begäranden om bildservering och bildåtergivning. Detta garanterar att alla variabeldefinitioner är tillgängliga för alla mallar, oavsett kapslingsnivå.

Oavsett kapslingsnivån måste bara HTTP-kodning i ett enda steg användas för variabelvärden som ska ersättas var som helst i en kapslad begäran om bildåtergivning eller bildservning.
