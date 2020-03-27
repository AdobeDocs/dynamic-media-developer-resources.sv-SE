---
description: $var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om '?' avgränsar sökvägen från frågan.
seo-description: $var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om '?' avgränsar sökvägen från frågan.
seo-title: Variabel bearbetning i kapslade begäranden
solution: Experience Manager
title: Variabel bearbetning i kapslade begäranden
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Variabel bearbetning i kapslade begäranden{#variable-processing-in-nested-requests}

$var$ referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om &#39;?&#39; avgränsar sökvägen från frågan.

Servern ersätter dessa referenser med värden (antingen från url eller från huvudbildkatalogen) innan `catalog::Modifier` den kapslade begäran analyseras och bearbetas ytterligare.

Dessutom vidarebefordras alla `$ *[!DNL var]*=` definitioner från URL:en och `catalog::Modifier` till alla kapslade förfrågningar om Image Serving och Image Rendering. Detta garanterar att alla variabeldefinitioner är tillgängliga för alla mallar, oavsett kapslingsnivå.

Oavsett kapslingsnivån måste bara HTTP-kodning i ett enda steg användas för variabelvärden som ska ersättas var som helst i en kapslad begäran om bildåtergivning eller bildservning.
