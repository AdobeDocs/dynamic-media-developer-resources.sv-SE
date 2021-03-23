---
description: Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.
seo-description: Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.
seo-title: Den sammansatta arbetsytan
solution: Experience Manager
title: Den sammansatta arbetsytan
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Den sammansatta arbetsytan{#the-compositing-canvas}

Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.

Om `size=` för lager 0 inte anges explicit används lageromformningarna för att beräkna storleken på den sammansatta arbetsytan (se nedan).

Om `req=tmb` bestäms storleken på den sammansatta arbetsytan av `size=` som anges för lager 0, eller, om storlek inte anges, ställs storleken på den sammansatta arbetsytan in på vyrektangeln (se nedan).
