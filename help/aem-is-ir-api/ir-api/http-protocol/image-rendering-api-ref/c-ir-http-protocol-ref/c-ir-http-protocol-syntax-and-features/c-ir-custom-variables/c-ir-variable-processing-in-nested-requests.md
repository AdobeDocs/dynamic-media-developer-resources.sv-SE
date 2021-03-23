---
description: $var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om '?' avgränsar sökvägen från frågan.
seo-description: $var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om '?' avgränsar sökvägen från frågan.
seo-title: Variabel bearbetning i kapslade begäranden
solution: Experience Manager
title: Variabel bearbetning i kapslade begäranden
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Variabel bearbetning i kapslade begäranden{#variable-processing-in-nested-requests}

$var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om &#39;?&#39; avgränsar sökvägen från frågan.

Servern ersätter dessa referenser med värden (antingen från url eller `catalog::Modifier` i huvudbildkatalogen) innan den kapslade begäran analyseras och bearbetas ytterligare.

Dessutom vidarebefordras alla `$ *[!DNL var]*=`-definitioner från URL:en och `catalog::Modifier` till alla kapslade begäranden om bildservering och bildåtergivning. Detta garanterar att alla variabeldefinitioner är tillgängliga för alla mallar, oavsett kapslingsnivå.

Oavsett kapslingsnivån måste bara HTTP-kodning i ett enda steg användas för variabelvärden som ska ersättas var som helst i en kapslad begäran om bildåtergivning eller bildservning.
