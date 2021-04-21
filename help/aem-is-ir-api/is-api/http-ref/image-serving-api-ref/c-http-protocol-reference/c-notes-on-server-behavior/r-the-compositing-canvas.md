---
description: Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.
solution: Experience Manager
title: Den sammansatta arbetsytan
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# Den sammansatta arbetsytan{#the-compositing-canvas}

Om req=img bestäms storleken på den sammansatta arbetsytan helt av storleken på lagret 0.

Om `size=` för lager 0 inte anges explicit används lageromformningarna för att beräkna storleken på den sammansatta arbetsytan (se nedan).

Om `req=tmb` bestäms storleken på den sammansatta arbetsytan av `size=` som anges för lager 0, eller, om storlek inte anges, ställs storleken på den sammansatta arbetsytan in på vyrektangeln (se nedan).
