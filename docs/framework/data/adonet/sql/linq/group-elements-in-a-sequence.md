---
title: "시퀀스의 요소 그룹화 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-ado"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1d50c8b4-f550-4775-bbb6-eab6e874cb43
caps.latest.revision: 2
author: "JennieHubbard"
ms.author: "jhubbard"
manager: "jhubbard"
caps.handback.revision: 2
---
# 시퀀스의 요소 그룹화
<xref:System.Linq.Enumerable.GroupBy%2A> 연산자는 시퀀스의 요소를 그룹화합니다.  다음 예제에서는 Northwind 데이터베이스를 사용합니다.  
  
> [!NOTE]
>  <xref:System.Linq.Enumerable.GroupBy%2A> 쿼리의 Null 열 값은 종종 <xref:System.InvalidOperationException>을 throw합니다.  자세한 내용은 [문제 해결](../../../../../../docs/framework/data/adonet/sql/linq/troubleshooting.md)의 "GroupBy InvalidOperationException" 단원을 참조하세요.  
  
## 예제  
 다음 예제에서는 `CategoryID`에 따라 `Products`를 구분합니다.  
  
 [!code-csharp[DLinqQueryExamples#27](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#27)]
 [!code-vb[DLinqQueryExamples#27](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#27)]  
  
## 예제  
 다음 예제에서는 <xref:System.Linq.Enumerable.Max%2A>를 사용하여 각 `CategoryID`에 대한 최대 단가를 검색합니다.  
  
 [!code-csharp[DLinqQueryExamples#28](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#28)]
 [!code-vb[DLinqQueryExamples#28](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#28)]  
  
## 예제  
 다음 예제에서는 Average를 사용하여 각 `CategoryID`에 대한 평균 `UnitPrice`를 검색합니다.  
  
 [!code-csharp[DLinqQueryExamples#29](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#29)]
 [!code-vb[DLinqQueryExamples#29](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#29)]  
  
## 예제  
 다음 예제에서는 <xref:System.Linq.Queryable.Sum%2A>을 사용하여 각 `CategoryID`에 대한 총 `UnitPrice`를 검색합니다.  
  
 [!code-csharp[DLinqQueryExamples#30](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#30)]
 [!code-vb[DLinqQueryExamples#30](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#30)]  
  
## 예제  
 다음 예제에서는 <xref:System.Linq.Queryable.Count%2A>를 사용하여 각 `CategoryID`에서 할인된 `Products`의 수를 검색합니다.  
  
 [!code-csharp[DLinqQueryExamples#31](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#31)]
 [!code-vb[DLinqQueryExamples#31](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#31)]  
  
## 예제  
 다음 예제에서는 아래의 `where` 절을 사용하여 최소 10개의 제품이 있는 범주를 모두 검색합니다.  
  
 [!code-csharp[DLinqQueryExamples#32](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#32)]
 [!code-vb[DLinqQueryExamples#32](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#32)]  
  
## 예제  
 다음 예제에서는 `CategoryID` 및 `SupplierID`에 따라 제품을 그룹화합니다.  
  
 [!code-csharp[DLinqQueryExamples#33](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#33)]
 [!code-vb[DLinqQueryExamples#33](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#33)]  
  
## 예제  
 다음 예제에서는 두 가지 제품 시퀀스를 반환합니다.  첫 번째 시퀀스에는 단가가 10 이하인 제품이 들어 있습니다.  두 번째 시퀀스에는 단가가 10보다 큰 제품이 들어 있습니다.  
  
 [!code-csharp[DLinqQueryExamples#34](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#34)]
 [!code-vb[DLinqQueryExamples#34](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#34)]  
  
## 예제  
 <xref:System.Linq.Queryable.GroupBy%2A> 연산자는 하나의 키 인수만을 받아들일 수 있습니다.  둘 이상의 키로 그룹화해야 하는 경우 다음 예제처럼 익명 형식을 만들어야 합니다.  
  
 [!code-csharp[DLinqQueryExamples#35](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#35)]
 [!code-vb[DLinqQueryExamples#35](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#35)]  
  
## 참고 항목  
 [쿼리 예제](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)   
 [샘플 데이터베이스 다운로드](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)