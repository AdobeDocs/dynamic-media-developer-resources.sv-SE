---
description: De flesta material kan färgas dynamiskt.
seo-description: De flesta material kan färgas dynamiskt.
seo-title: Färga material
solution: Experience Manager
title: Färga material
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Färga material{#colorizing-materials}

De flesta material kan färgas dynamiskt.

Färgningsalgoritmen är mycket enkel och fungerar bäst för materialbilder som har ett begränsat nyansintervall. Om du vill färglägga ett material subtraherar renderaren bara `bgc=`-värdet och lägger till `color=`-värdet till varje pixelvärde.

Färgläggning är inaktiverat om `color=` inte anges. `bgc=` ignoreras av kabinettmaterial, basfärgvärdet som är inbäddat i  [!DNL vnc] filen används i stället.
