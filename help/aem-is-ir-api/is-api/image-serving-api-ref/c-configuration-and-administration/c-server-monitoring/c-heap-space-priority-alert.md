---
description: En prioritetsvarning skickas när det kostnadsfria Java-heap-utrymmet ligger under det angivna tröskelvärdet omedelbart efter en Java-skräpinsamlingscykel.
solution: Experience Manager
title: Prioritetsvarning för heap-space
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Varning om prioritetsordning för heap-space{#heap-space-priority-alert}

En prioritetsvarning skickas när det kostnadsfria Java-heap-utrymmet ligger under det angivna tröskelvärdet omedelbart efter en Java-skräpinsamlingscykel.

Upprepade varningar bör åtgärdas genom att Java-heap-utrymmet ökas. Efterföljande förekomster av det här villkoret resulterar inte i någon e-postavisering förrän den fördröjningsperiod som har angetts med `AS::monitorAlertGenerator.heapSpaceResetInterval` har gått ut.
