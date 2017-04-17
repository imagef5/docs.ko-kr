---
title: "워크플로 유지 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "프로그래밍 [WF], 유지"
ms.assetid: 39e69d1f-b771-4c16-9e18-696fa43b65b2
caps.latest.revision: 26
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 26
---
# 워크플로 유지
워크플로 지속성은 프로세스 또는 시스템 정보에 독립적인 영구 워크플로 인스턴스 상태 캡처입니다.이 작업은 시스템 오류가 발생한 경우에 워크플로 인스턴스에 대한 잘 알려진 복구 지점을 제공하거나, 현재 작업 중이 아닌 워크플로 인스턴스를 언로드하여 메모리를 보존하거나, 워크플로 인스턴스의 상태를 서버 팜의 한 노드에서 다른 노드로 이동하기 위해 수행합니다.  
  
 지속성은 프로세스의 신속성, 확장성, 오류 복구, 효율적인 메모리 관리를 가능하게 해줍니다.지속성 프로세스는 유지 지점을 식별하고, 저장할 데이터를 수집하며, 마지막으로 지속성 공급자에게 실제 데이터 저장소를 위임하는 과정으로 구성됩니다.  
  
 워크플로에 대한 지속성을 사용하려면 [방법: 워크플로 및 워크플로 서비스에 지속성 사용](../../../docs/framework/windows-workflow-foundation//how-to-enable-persistence-for-workflows-and-workflow-services.md)에 설명된 대로 인스턴스 저장소를 **WorkflowApplication** 또는 **WorkflowServiceHost**에 연결해야 합니다.**WorkflowApplication** 및 **WorkflowServiceHost**는 연결된 인스턴스 저장소를 사용하여 지속성 저장소에 워크플로 인스턴스를 유지하고 지속성 저장소에 저장된 워크플로 인스턴스 데이터를 기반으로 워크플로 인스턴스를 메모리에 로드합니다.  
  
 [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)]에서는 **SqlWorkflowInstanceStore** 클래스를 제공하여 워크플로 인스턴스에 대한 데이터와 메타데이터를 SQL Server 2005 또는 SQL Server 2008 데이터베이스에 유지할 수 있도록 합니다.자세한 내용은 [SQL 워크플로 인스턴스 저장소](../../../docs/framework/windows-workflow-foundation//sql-workflow-instance-store.md)를 참조하십시오.  
  
 워크플로 인스턴스 관련 정보와 함께 응용 프로그램별 데이터를 저장하고 로드하려면 <xref:System.Activities.Persistence.PersistenceParticipant> 클래스를 확장하는 지속성 참석자를 만들 수 있습니다.지속성 참석자는 지속성 프로세스에 참여하여 serialize 가능한 사용자 지정 데이터를 지속성 저장소에 저장하고, 인스턴스 저장소의 데이터를 메모리로 로드하며, 지속성 트랜잭션에서 추가 논리를 수행합니다.자세한 내용은 [지속성 참석자](../../../docs/framework/windows-workflow-foundation//persistence-participants.md)를 참조하십시오.  
  
 Windows Server App Fabric은 지속성의 구성 프로세스를 단순화합니다.[!INCLUDE[crdefault](../../../includes/crdefault-md.md)][Windows Server App Fabric의 지속성 개념](http://go.microsoft.com/fwlink/?LinkId=201200)  
  
## 암시적 유지 지점  
 다음 목록에는 인스턴스 저장소가 워크플로에 연결되어 있을 때 워크플로가 유지되는 조건에 대한 예제가 포함되어 있습니다.  
  
-   **TransactionScope** 활동이 완료되거나 **TransactedReceiveScope** 활동이 완료된 경우  
  
-   워크플로 인스턴스가 유휴 상태가 되고 워크플로 호스트에 대한 **WorkflowIdleBehavior**가 설정된 경우.예를 들어 메시징 활동 또는 **Delay** 활동을 사용하는 경우에 이런 상태가 됩니다.  
  
-   WorkflowApplication이 유휴 상태가 되고 응용 프로그램의 **PersistableIdle** 속성이 **PersistableIdleAction.Persist**로 설정된 경우  
  
-   워크플로 인스턴스를 유지하거나 언로드하도록 호스트 응용 프로그램에 지시할 경우  
  
-   워크플로 인스턴스가 종료되거나 완료되는 경우  
  
-   **Persist** 활동을 실행할 경우  
  
-   이전 버전의 Windows Workflow Foundation을 사용하여 개발된 워크플로 인스턴스에서 상호 운용 가능한 방식으로 실행되는 동안 유지 지점을 발견한 경우  
  
## 단원 내용  
  
-   [SQL 워크플로 인스턴스 저장소](../../../docs/framework/windows-workflow-foundation//sql-workflow-instance-store.md)  
  
-   [인스턴스 저장소](../../../docs/framework/windows-workflow-foundation//instance-stores.md)  
  
-   [지속성 참석자](../../../docs/framework/windows-workflow-foundation//persistence-participants.md)  
  
-   [지속성 최선의 구현 방법](../../../docs/framework/windows-workflow-foundation//persistence-best-practices.md)  
  
-   [비지속형 워크플로 인스턴스](../../../docs/framework/windows-workflow-foundation//non-persisted-workflow-instances.md)  
  
-   [워크플로 일시 중지 및 다시 시작](../../../docs/framework/windows-workflow-foundation//pausing-and-resuming-a-workflow.md)