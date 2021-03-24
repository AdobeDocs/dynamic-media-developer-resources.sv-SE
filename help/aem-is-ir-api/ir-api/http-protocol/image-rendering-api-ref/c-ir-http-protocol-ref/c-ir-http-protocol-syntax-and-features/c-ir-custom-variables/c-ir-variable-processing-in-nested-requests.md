---
description: $var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om '?' avgränsar sökvägen från frågan.
solution: Experience Manager
title: Variabel bearbetning i kapslade begäranden
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Variabel bearbetning i kapslade begäranden{#variable-processing-in-nested-requests}

$var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om &#39;?&#39; avgränsar sökvägen från frågan.

Servern ersätter dessa referenser med värden (antingen från url eller `catalog::Modifier` i huvudbildkatalogen) innan den kapslade begäran analyseras och bearbetas ytterligare.

Dessutom vidarebefordras alla `$ *[!DNL var]*=`-definitioner från URL:en och `catalog::Modifier` till alla kapslade begäranden om bildservering och bildåtergivning. Detta garanterar att alla variabeldefinitioner är tillgängliga för alla mallar, oavsett kapslingsnivå.

Oavsett kapslingsnivån måste bara HTTP-kodning i ett enda steg användas för variabelvärden som ska ersättas var som helst i en kapslad begäran om bildåtergivning eller bildservning.
