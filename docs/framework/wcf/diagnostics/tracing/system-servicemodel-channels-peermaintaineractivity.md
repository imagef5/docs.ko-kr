---
title: "System.ServiceModel.Channels.PeerMaintainerActivity | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ef28d086-d7fb-4e81-82e9-45a54647783b
caps.latest.revision: 10
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 10
---
# System.ServiceModel.Channels.PeerMaintainerActivity
PeerMaintainer 모듈이 특정 작업을 수행하고 있습니다\(상세 정보는 추적 메시지 본문에 포함\).  
  
## 설명  
 이 추적은 다양한 PeerMaintainer 작업을 수행하는 동안 발생합니다.  
  
 PeerMaintainer는 PeerNode의 내부 구성 요소입니다.  1분마다 또는 메시지 32개를 받을 때마다 PeerMaintainer는 교환된 메시지 수 및 유용한 메시지\(손상되지 않은 비중복 메시지\) 수에 대한 통계가 포함된 LinkUtility 메시지를 인접한 환경에 보냅니다.  이렇게 하면 특정 환경의 링크 유틸리티를 확인하는 데 도움이 됩니다.  약 5분마다 유지 관리자는 환경 연결의 상태를 검사합니다.  환경 연결 수가 이상적인 값을 초과하면 유지 관리자가 가장 덜 유용한 연결을 정리합니다.  연결 수가 충분하지 않으면 유지 관리자가 새 연결을 설정합니다.  
  
## 참고 항목  
 [추적](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)   
 [추적을 사용하여 응용 프로그램 문제 해결](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)   
 [관리 및 진단](../../../../../docs/framework/wcf/diagnostics/index.md)