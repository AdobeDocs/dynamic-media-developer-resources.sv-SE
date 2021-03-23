---
description: Cacheklustring gör att flera belastningsutjämnade servrar kan utbyta cacheposter i det primära svarscacheminnet och det sekundära datacacheminnet (för kapslade/inbäddade begäranden), vilket kan göra servern betydligt mer responsiv genom att eliminera behovet av att generera samma cachepost på flera servrar.
seo-description: Cacheklustring gör att flera belastningsutjämnade servrar kan utbyta cacheposter i det primära svarscacheminnet och det sekundära datacacheminnet (för kapslade/inbäddade begäranden), vilket kan göra servern betydligt mer responsiv genom att eliminera behovet av att generera samma cachepost på flera servrar.
seo-title: Cacheklustring
solution: Experience Manager
title: Cacheklustring
uuid: 347165d6-a9e7-406e-81a8-8a91f745ce27
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '359'
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

* När `PS::cacheCluster.updateLocalCache` är inaktiverat kopieras inte data från andra servrar till det lokala cacheminnet.

   Detta multiplicerar det tillgängliga diskutrymmet för cachedata. Det ökar dock trafiken mellan peer-servrarna och minskar de totala svarstiderna. Använd bara den här konfigurationen när du ser låga träfffrekvenser för cacheminnet.

