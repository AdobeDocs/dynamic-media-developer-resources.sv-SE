---
description: En prioritetsvarning skickas när det kostnadsfria Java-heap-utrymmet ligger under det angivna tröskelvärdet omedelbart efter en Java-skräpinsamlingscykel.
solution: Experience Manager
title: Prioritetsvarning för heap-space
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Prioritetsvarning för heap-space{#heap-space-priority-alert}

En prioritetsvarning skickas när det kostnadsfria Java-heap-utrymmet ligger under det angivna tröskelvärdet omedelbart efter en Java-skräpinsamlingscykel.

Upprepade varningar bör åtgärdas genom att Java-heap-utrymmet ökas. Efterföljande förekomster av det här villkoret resulterar inte i någon e-postavisering förrän den fördröjningsperiod som har angetts med `AS::monitorAlertGenerator.heapSpaceResetInterval` har gått ut.
