---
title: "방법: 코드에서 서비스 끝점 만들기 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3fbb22fa-2930-48b8-b437-def1de87c6a0
caps.latest.revision: 14
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 14
---
# 방법: 코드에서 서비스 끝점 만들기
이 예제에서는 계산기 서비스에 대해 `ICalculator` 계약을 정의하고, `CalculatorService` 클래스에서 서비스를 구현한 다음 코드로 끝점을 정의합니다. 이 때 서비스가 <xref:System.ServiceModel.BasicHttpBinding> 클래스를 사용하도록 지정합니다.  
  
 일반적으로 바인딩 및 주소 정보를 코드에서 명령적으로 지정하지 않고 구성에서 선언적으로 지정하는 것이 좋습니다.일반적으로 배포된 서비스의 바인딩과 주소는 서비스를 배포할 때 사용된 바인딩 및 주소와 다르기 때문에 코드로 끝점을 정의하는 것은 효과적이지 않습니다.일반적으로 바인딩 및 주소 지정 정보를 코드와 구분하면 응용 프로그램을 다시 컴파일하거나 다시 배포할 필요 없이 해당 정보를 변경할 수 있습니다.  
  
#### 코드에서 서비스 끝점을 만들려면  
  
1.  서비스 계약을 정의하는 인터페이스를 만듭니다.  
  
     [!code-csharp[c_HowTo_CodeServiceBinding#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeservicebinding/cs/source.cs#1)]
     [!code-vb[c_HowTo_CodeServiceBinding#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeservicebinding/vb/source.vb#1)]  
  
2.  1단계에서 정의한 서비스 계약을 구현합니다.  
  
     [!code-csharp[c_HowTo_CodeServiceBinding#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeservicebinding/cs/source.cs#2)]
     [!code-vb[c_HowTo_CodeServiceBinding#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeservicebinding/vb/source.vb#2)]  
  
3.  호스팅 응용 프로그램에서 서비스에 사용할 바인딩 및 서비스에 대한 기본 주소를 만듭니다.  
  
     [!code-csharp[c_HowTo_CodeServiceBinding#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeservicebinding/cs/source.cs#3)]
     [!code-vb[c_HowTo_CodeServiceBinding#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeservicebinding/vb/source.vb#3)]  
  
4.  호스트를 만들고, 호스트에 대한 서비스 끝점을 추가할 <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%28System.Type%2CSystem.ServiceModel.Channels.Binding%2CSystem.String%29> 또는 다른 오버로드 중 하나를 호출합니다.  
  
     [!code-csharp[c_HowTo_CodeServiceBinding#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeservicebinding/cs/source.cs#6)]
     [!code-vb[c_HowTo_CodeServiceBinding#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeservicebinding/vb/source.vb#6)]  
  
     코드에서 바인딩을 지정하되 런타임에서 제공하는 기본 끝점을 사용하려면 <xref:System.ServiceModel.ServiceHost>를 만들 때 기본 주소를 생성자로 전달하고 <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A>를 호출하지 마십시오.  
  
     [!code-csharp[c_HowTo_CodeServiceBinding#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeservicebinding/cs/source.cs#7)]
     [!code-vb[c_HowTo_CodeServiceBinding#7](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeservicebinding/vb/source.vb#7)]  
  
     기본 끝점[!INCLUDE[crabout](../../../../includes/crabout-md.md)][단순화된 구성](../../../../docs/framework/wcf/simplified-configuration.md) 및 [WCF 서비스를 위한 단순화된 구성](../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)을 참조하십시오.  
  
## 참고 항목  
 [방법: 코드에서 서비스 바인딩 지정](../../../../docs/framework/wcf/how-to-specify-a-service-binding-in-code.md)