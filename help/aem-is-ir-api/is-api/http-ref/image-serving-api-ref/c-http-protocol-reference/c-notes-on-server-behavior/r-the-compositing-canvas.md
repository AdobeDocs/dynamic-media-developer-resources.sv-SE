---
description: Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.
solution: Experience Manager
title: Den sammansatta arbetsytan
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Den sammansatta arbetsytan{#the-compositing-canvas}

Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.

Om `size=` för lager 0 inte anges uttryckligen, används lageromformningarna för att beräkna storleken på den sammansatta arbetsytan (se nedan).

Om det är `req=tmb` bestäms storleken på den sammansatta arbetsytan av `size=` som anges för lager 0, eller, om storlek inte anges, så ställs storleken på arbetsytan för sammansättning in på vyrektangeln (se nedan).
