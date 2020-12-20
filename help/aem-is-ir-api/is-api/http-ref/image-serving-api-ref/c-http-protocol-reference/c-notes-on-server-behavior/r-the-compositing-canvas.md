---
description: Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.
seo-description: Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.
seo-title: Den sammansatta arbetsytan
solution: Experience Manager
title: Den sammansatta arbetsytan
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# Den sammansatta arbetsytan{#the-compositing-canvas}

Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.

Om `size=` för lager 0 inte anges explicit används lageromformningarna för att beräkna storleken på den sammansatta arbetsytan (se nedan).

Om `req=tmb` bestäms storleken på den sammansatta arbetsytan av `size=` som anges för lager 0, eller, om storlek inte anges, ställs storleken på den sammansatta arbetsytan in på vyrektangeln (se nedan).
