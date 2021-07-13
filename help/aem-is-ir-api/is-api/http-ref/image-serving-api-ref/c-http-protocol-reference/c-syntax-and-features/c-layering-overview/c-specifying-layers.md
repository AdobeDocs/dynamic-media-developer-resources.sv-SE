---
description: I kommandosekvensen URL eller katalogmodifierare börjar en lagerdefinitionssekvens med kommandot layer= och slutar med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.
solution: Experience Manager
title: Ange lager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Ange lager{#specifying-layers}

I URL:en eller katalogen::Modifier-kommandosekvensen startar en lagerdefinitionssekvens med kommandot layer= och avslutas med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.

Alla kommandon i lagerdefinitionssekvensen är kopplade till lagret.

Kommandot `layer=` anger ett lagernummer som måste vara ett heltal som är 0 eller större. Alla kommandon i lagerdefinitionssekvenser med samma lagernummer används på samma lager. Om samma kommando förekommer mer än en gång gäller den sista förekomsten.
