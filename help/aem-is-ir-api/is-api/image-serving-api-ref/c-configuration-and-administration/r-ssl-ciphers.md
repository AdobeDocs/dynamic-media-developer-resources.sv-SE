---
description: Taggen Connector i server.xml har stöd för ett ciphers-attribut som begränsar antalet ciphers som kan väljas för en SSL-anslutning.
solution: Experience Manager
title: Definiera SSL-skrivare
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Definiera SSL-skrivare{#defining-ssl-ciphers}

Taggen Connector i server.xml har stöd för ett ciphers-attribut som begränsar antalet ciphers som kan väljas för en SSL-anslutning.

Som standard är alla ciphers tillgängliga. Listan är kommaavgränsad och kan innehålla något av följande värden:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

<!-- WEAK CQDOC-19433 `SSL_RSA_WITH_3DES_EDE_CBC_SHA` -->

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

<!-- WEAK CQDOC-19433 `TLS_RSA_WITH_AES_128_CBC_SHA` -->

Om något av värdena är fel aktiverar Tomcat alla klipp. Därför är det viktigt att du kontrollerar med ett externt verktyg efter konfigurationen för att se vilka utbildare som är aktiverade.

Som ett exempel aktiverar följande konfiguration endast chiffersviterna &quot;128 bitar&quot; och högre:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA"`
