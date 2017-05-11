---
title: "역할 기반 보안 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-standard"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "인증[.NET Framework], 보안 주체"
  - "사용 권한[.NET Framework], 보안 주체"
  - "주체[.NET Framework]"
  - "역할 기반 보안, 역할 기반 보안 정보"
  - "역할 기반 보안, 보안 주체"
  - "보안[.NET Framework], 역할 기반"
  - "사용자 인증, 보안 주체"
ms.assetid: 578cc32b-5654-4d8b-9d8c-ebcbc5c75390
caps.latest.revision: 13
author: "mairaw"
ms.author: "mairaw"
manager: "wpickett"
caps.handback.revision: 13
---
# 역할 기반 보안
역할은 재무 또는 비즈니스 응용 프로그램에서 정책을 적용하는 데 자주 사용됩니다.  예를 들어 요청을 수행하는 사용자가 지정된 역할의 멤버인지 여부에 따라 응용 프로그램이 처리되는 트랜잭션의 크기에 제한을 적용할 수 있습니다.  점원은 지정된 임계값보다 작은 트랜잭션을 처리할 수 있는 권한이 있고, 관리자는 더 높은 한도가 적용될 수 있고, 부사장은 이보다 더 높은 한도\(또는 제한 없음\)가 적용될 수 있습니다.  응용 프로그램에서 작업을 완료하는 데 여러 승인이 필요한 경우에도 역할 기반 보안을 사용할 수 있습니다.  이러한 경우로 모든 직원이 구매 요청을 생성할 수 있지만 구매 담당자만 해당 요청을 공급자에게 보낼 수 있는 구매 주문으로 변환할 수 있는 구매 시스템이 있습니다.  
  
 .NET framework 역할 기반 보안은 관련된 ID에서 생성된 보안 주체에 대한 정보를 현재 스레드에서 사용할 수 있도록 하여 권한 부여를 지원합니다.  ID\(및 이 ID를 통해 정의되는 보안 주체\)는 Windows 계정을 기반으로 하거나 Windows 계정과 관련이 없는 사용자 지정 ID일 수 있습니다.  .NET framework 응용 프로그램은 보안 주체의 ID, 역할 멤버 자격 또는 둘 다에 따라 권한 부여 결정을 내릴 수 있습니다.  역할은 보안과 관련해서 동일한 권한을 가진 명명된 보안 주체 집합\(예: 계산원 또는 관리자\)입니다.  보안 주체는 하나 이상 역할의 멤버일 수 있습니다.  따라서 응용 프로그램은 역할 멤버 자격을 사용하여 보안 주체가 요청된 작업을 수행할 수 있는 권한이 있는지 확인할 수 있습니다.  
  
 코드 액세스 보안을 사용하여 사용 편의성 및 일관성을 제공하기 위해 .NET Framework 역할 기반 보안은 공용 언어 런타임이 코드 액세스 보안 검사와 비슷한 방식으로 권한 부여를 수행할 수 있게 해주는 <xref:System.Security.Permissions.PrincipalPermission?displayProperty=fullName> 개체를 제공합니다.  <xref:System.Security.Permissions.PrincipalPermission> 클래스는 보안 주체가 일치해야 하는 ID 또는 역할을 나타내며 선언적 보안 검사 및 명령적 보안 검사 둘 다와 호환됩니다.  필요한 경우 보안 주체의 ID 정보에 직접 액세스하고 코드에서 역할 및 ID 검사를 수행할 수도 있습니다.  
  
 .NET Framework는 다양한 응용 프로그램의 요구를 충족할 수 있을 만큼 유연하고 확장 가능한 역할 기반 보안 지원을 제공합니다.  COM \+ 1.0 서비스와 같은 기존 인증 인프라와 상호 운용되거나 사용자 지정 인증 시스템을 만들도록 선택할 수 있습니다.  역할 기반 보안은 주로 서버에서 처리되는 ASP.NET 웹 응용 프로그램에서 사용하기에 특히 적합합니다.  그러나.NET Framework 역할 기반 보안은 클라이언트 또는 서버 중 하나에서 사용할 수 있습니다.  
  
 이 섹션을 읽기 전에 [주요 보안 개념](../../../docs/standard/security/key-security-concepts.md)에 제공된 내용을 이해해야 합니다.  
  
## 관련 항목  
  
|제목|설명|  
|--------|--------|  
|[Principal 개체 및 Identity 개체](../../../docs/standard/security/principal-and-identity-objects.md)|Windows 및 제네릭 ID와 보안 주체를 설정 및 관리하는 방법을 설명합니다.|  
|[주요 보안 개념](../../../docs/standard/security/key-security-concepts.md)|.NET Framework 보안을 사용하기 전에 이해해야 할 기본 개념을 소개합니다.|  
  
## 참조  
 <xref:System.Security.Permissions.PrincipalPermission?displayProperty=fullName>