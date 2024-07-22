---
title: Variabel bearbetning i inbäddade externa begäranden
description: $var$ referenser som förekommer var som helst inom klammerparenteserna för en inbäddad extern begäran ersätts med matchande variabeldefinitionsvärden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Variabel bearbetning i inbäddade externa begäranden{#variable-processing-in-embedded-foreign-requests}

Alla `$var$`-referenser som förekommer var som helst inom klammerparenteserna för en inbäddad extern begäran ersätts med matchande variabeldefinitionsvärden.

Tillåter inbäddade externa begäranden att placeras i en mall i en bildkatalog.

Variabelvärden som ska ersättas i externa begäranden måste vanligtvis dubbelkodas, eftersom ingen omkodning används innan servern försöker överföra den slutliga externa URL:en.
