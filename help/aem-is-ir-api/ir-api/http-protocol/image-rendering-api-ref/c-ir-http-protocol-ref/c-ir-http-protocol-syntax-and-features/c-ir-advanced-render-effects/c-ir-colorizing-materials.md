---
description: De flesta material kan färgas dynamiskt.
solution: Experience Manager
title: Färga material
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Färga material{#colorizing-materials}

De flesta material kan färgas dynamiskt.

Färgningsalgoritmen är mycket enkel och fungerar bäst för materialbilder som har ett begränsat nyansintervall. Om du vill färglägga ett material subtraherar renderaren bara `bgc=`-värdet och lägger till `color=`-värdet till varje pixelvärde.

Färgläggning är inaktiverat om `color=` inte anges. `bgc=` ignoreras av kabinettmaterial, basfärgvärdet som är inbäddat i  [!DNL vnc] filen används i stället.
