---
description: En prioritetsvarning skickas när det kostnadsfria Java-heap-utrymmet ligger under det angivna tröskelvärdet omedelbart efter en Java-skräpinsamlingscykel.
seo-description: En prioritetsvarning skickas när det kostnadsfria Java-heap-utrymmet ligger under det angivna tröskelvärdet omedelbart efter en Java-skräpinsamlingscykel.
seo-title: Prioritetsvarning för heap-space
solution: Experience Manager
title: Prioritetsvarning för heap-space
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Varning om prioritetsordning för heap-space{#heap-space-priority-alert}

En prioritetsvarning skickas när det kostnadsfria Java-heap-utrymmet ligger under det angivna tröskelvärdet omedelbart efter en Java-skräpinsamlingscykel.

Upprepade varningar bör åtgärdas genom att Java-heap-utrymmet ökas. Efterföljande förekomster av det här villkoret resulterar inte i någon e-postavisering förrän den fördröjningsperiod som har angetts med `AS::monitorAlertGenerator.heapSpaceResetInterval` har gått ut.
