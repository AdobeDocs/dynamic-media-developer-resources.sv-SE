---
description: Använd de här serverinställningarna för cacheklustring.
seo-description: Använd de här serverinställningarna för cacheklustring.
seo-title: Cacheklustring
solution: Experience Manager
title: Cacheklustring
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Cacheklustring{#cache-clustering}

Använd de här serverinställningarna för cacheklustring.

## PS::cacheCluster.hosts - värdar {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Lista med IP-adresser, avgränsade med semikolon. Inkludera IP-adresserna för alla peer-servrar som den här värden ska hämta cachedata från. Den lokala värddatorns IP-adress kan inkluderas av praktiska skäl. Detta tillåter samma konfigurationsinställningar för alla servrar i klustret.

## PS::cacheCluster.updateLocalCache - Uppdatera lokal cache {#section-154c2c0af4544200a3499232bb130dde}

Ange Ja om en cachepost från en peer-server ska kopieras till den lokala svarscachen.

## PS::cacheCluster.queryTimeout - Frågetimeout {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

När servern begär en cachepost från peer-servrar väntar den tills en server svarar att den har det här dataobjektet, eller tills alla peer-servrar har svarat att de inte har dataobjektet, eller tills den tid som anges med den här inställningen (i msek) har gått ut.

## PS::cacheCluster.fetchTimeout - Hämtningstimeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Anger det maximala antal msek som servern väntar på att faktiska cachedata ska levereras från peer-servern. Om fullständiga data inte har levererats innan tidsgränsen har löpt ut, antar servern att peer-datorn inte är tillgänglig. Cacheposten genereras sedan lokalt.
