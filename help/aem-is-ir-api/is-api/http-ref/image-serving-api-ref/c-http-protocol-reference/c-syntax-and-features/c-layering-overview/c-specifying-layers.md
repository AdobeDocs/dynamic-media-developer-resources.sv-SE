---
description: I kommandosekvensen URL eller katalogmodifierare börjar en lagerdefinitionssekvens med kommandot layer= och slutar med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.
seo-description: I kommandosekvensen URL eller katalogmodifierare börjar en lagerdefinitionssekvens med kommandot layer= och slutar med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.
seo-title: Ange lager
solution: Experience Manager
title: Ange lager
topic: Scene7 Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ange lager{#specifying-layers}

I URL:en eller katalogen::Modifier-kommandosekvensen startar en lagerdefinitionssekvens med kommandot layer= och avslutas med ett annat layer=-kommando, ett effect=-kommando eller slutet av URL:en.

Alla kommandon i lagerdefinitionssekvensen är kopplade till lagret.

Kommandot `layer=` anger ett lagernummer som måste vara ett heltal som är 0 eller större. Alla kommandon i lagerdefinitionssekvenser med samma lagernummer används på samma lager. Om samma kommando förekommer mer än en gång gäller den sista förekomsten.
