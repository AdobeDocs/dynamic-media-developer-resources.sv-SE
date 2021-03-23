---
description: I kommandosekvensen URL eller katalogmodifierare börjar en lagerdefinitionssekvens med kommandot layer= och slutar med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.
seo-description: I kommandosekvensen URL eller katalogmodifierare börjar en lagerdefinitionssekvens med kommandot layer= och slutar med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.
seo-title: Ange lager
solution: Experience Manager
title: Ange lager
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Ange lager{#specifying-layers}

I URL:en eller katalogen::Modifier-kommandosekvensen startar en lagerdefinitionssekvens med kommandot layer= och avslutas med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.

Alla kommandon i lagerdefinitionssekvensen är kopplade till lagret.

Kommandot `layer=` anger ett lagernummer som måste vara ett heltal som är 0 eller större. Alla kommandon i lagerdefinitionssekvenser med samma lagernummer används på samma lager. Om samma kommando förekommer mer än en gång gäller den sista förekomsten.
