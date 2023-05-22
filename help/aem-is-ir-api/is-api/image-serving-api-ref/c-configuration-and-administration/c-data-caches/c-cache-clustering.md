---
description: Cacheklustring gör att flera belastningsutjämnade servrar kan utbyta cacheposter i det primära svarscacheminnet och det sekundära datacacheminnet (för kapslade/inbäddade begäranden), vilket kan göra servern betydligt mer responsiv genom att eliminera behovet av att generera samma cachepost på flera servrar.
solution: Experience Manager
title: Cacheklustring
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Cacheklustring{#cache-clustering}

Cacheklustring gör att flera belastningsutjämnade servrar kan utbyta cacheposter i det primära svarscacheminnet och det sekundära datacacheminnet (för kapslade/inbäddade begäranden), vilket kan göra servern betydligt mer responsiv genom att eliminera behovet av att generera samma cachepost på flera servrar.

Om detta är konfigurerat och en server tar emot en begäran för ett objekt som inte finns i det lokala cacheminnet, kontaktar den peer-servrarna i klustret. Den kontrollerar om de redan har det dataobjektet innan de ber Image Server att generera objektet.

Cacheklustring är främst till fördel för program som innehåller mycket cachelagrat innehåll. Serverbelastningen bör reduceras avsevärt under den initiala driftsättningen och vid publicering med nytt innehåll.

Timeout och andra säkerhetsåtgärder säkerställer att systemet fortsätter att fungera med full kapacitet även när en eller flera peer-servrar är offline.

Cacheklustret kan fungera i en av två grundläggande konfigurationer:

* När `PS::cacheCluster.updateLocalCache` är aktiverat (standard) kopieras alla cacheposter som finns på en peer-server till det lokala cacheminnet.

   Den här konfigurationen minskar trafiken mellan peer-servrarna. Den ger också de snabbaste svarstiderna på bekostnad av att alla cacheposter replikeras till alla servrar i klustret. Detta är den rekommenderade konfigurationen.

* När `PS::cacheCluster.updateLocalCache` är inaktiverat, data från andra servrar kopieras inte till det lokala cacheminnet.

   Detta multiplicerar det tillgängliga diskutrymmet för cachedata. Det ökar dock trafiken mellan peer-servrarna och minskar de totala svarstiderna. Använd bara den här konfigurationen när du ser låga träfffrekvenser för cacheminnet.
