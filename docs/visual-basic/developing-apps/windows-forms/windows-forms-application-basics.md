---
title: "Windows Forms 응용 프로그램 기초 (Visual Basic) | Microsoft 문서"
ms.date: 2015-07-20
ms.prod: .net
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
dev_langs:
- VB
helpviewer_keywords:
- Windows applications
- Windows Forms, Visual Basic
ms.assetid: 0b919d30-7fd6-42db-85c8-543d15312441
caps.latest.revision: 20
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 8275d3c06ebd89254a07127b4850d32ef0580830
ms.lasthandoff: 03/13/2017

---
# <a name="windows-forms-application-basics-visual-basic"></a>Windows Forms 응용 프로그램 기초(Visual Basic)
중요 한 부분이 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 사용자의 컴퓨터에서 로컬로 실행 되는 Windows Forms 응용 프로그램을 만들 수 있다는 것입니다. Visual Studio를 사용 하 여 Windows Forms를 사용 하 여 응용 프로그램 및 사용자 인터페이스를 만들 수 있습니다. Windows Forms 응용 프로그램의 클래스를 기반으로 <xref:System.Windows.Forms>네임 스페이스.</xref:System.Windows.Forms>  
  
## <a name="designing-windows-forms-applications"></a>디자인 Windows Forms 응용 프로그램  
 Windows Forms 및 Windows 서비스 응용 프로그램을 만들 수 있습니다 [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)]합니다. 자세한 내용은 다음 항목을 참조하세요.  
  
-   [Windows Forms 시작](https://msdn.microsoft.com/library/ms229601.aspx)합니다. 만들고 Windows Forms를 프로그래밍 하는 방법에 대 한 정보를 제공 합니다.  
   
-   [Windows Forms 컨트롤](https://msdn.microsoft.com/library/ettb6e2a.aspx)합니다. Windows Forms 컨트롤의 사용을 자세히 보여 주는 항목의 컬렉션입니다.  
  
-   [Windows 서비스 응용 프로그램](https://msdn.microsoft.com/library/y817hyb6.aspx)합니다. Windows 서비스를 만드는 방법을 설명 하는 항목을 나열 합니다.  
  
## <a name="building-rich-interactive-user-interfaces"></a>풍부한 대화형 사용자 인터페이스 빌드  
 Windows Forms는의 스마트 클라이언트 구성 요소는 [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)], 읽기 및 쓰기 파일 시스템에 같은 일반적인 응용 프로그램 작업을 사용할 수 있는 관리 되는 라이브러리 집합입니다. 같은 개발 환경을 사용 하 여 [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)], 네트워크를 통해 원격 컴퓨터와 정보를 표시 하 고 사용자 로부터 입력을 요청 하 고 전달 하는 Windows Forms 응용 프로그램을 만들 수 있습니다.  
  
 Windows Forms의 양식은 정보 사용자에 게 표시할 수 있는 시각적 화면입니다. 일반적으로 폼에 컨트롤을 배치 하 고 마우스 클릭 또는 키 누름과 같은 사용자 작업에 대 한 응답을 개발 하 여 Windows Forms 응용 프로그램을 빌드합니다. A *제어* 는 데이터를 표시 하거나 데이터 입력을 허용 하는 개별 사용자 인터페이스 (UI) 요소입니다.  
  
### <a name="events"></a>이벤트  
 사용자가 폼 이나 컨트롤 중 하나, 이벤트를 생성 합니다. 응용 프로그램은 코드를 사용하여 이러한 이벤트에 대응하고, 발생 시 이벤트를 처리합니다. 자세한 내용은 참조 [Windows Forms에서 이벤트 처리기 만들기](https://msdn.microsoft.com/library/dacysss4.aspx)합니다.  
  
### <a name="controls"></a>컨트롤  
 다양 한 폼에 배치할 수 있는 컨트롤을 포함 하는 Windows Forms: 텍스트 상자, 단추, 드롭다운 상자, 라디오 단추 및 심지어 웹 페이지를 표시 하는 컨트롤입니다. 폼에서 사용할 수 있는 모든 컨트롤의 목록에 대 한 참조 [Windows Forms에서 사용할 컨트롤](https://msdn.microsoft.com/library/3xdhey7w.aspx)합니다. 기존 컨트롤로 요구 사항에 맞지 않으면, Windows Forms도 지원 <xref:System.Windows.Forms.UserControl>클래스</xref:System.Windows.Forms.UserControl> 를 사용 하 여 사용자 고유의 사용자 지정 컨트롤 만들기  
  
 Windows Forms에는 Microsoft Office와 같은 고급 응용 프로그램의 기능을 에뮬레이트하는 풍부한 UI 컨트롤이 있습니다. 사용 하는 <xref:System.Windows.Forms.ToolStrip>및 <xref:System.Windows.Forms.MenuStrip>컨트롤을 도구 모음 및 메뉴 텍스트와 이미지를 포함 하 고, 하위 메뉴를 표시, 텍스트 상자 및 콤보 상자와 같은 다른 컨트롤을 호스팅하는 만들 수 있습니다.</xref:System.Windows.Forms.MenuStrip> </xref:System.Windows.Forms.ToolStrip>  
  
 와 [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)] 끌어서 놓기 폼 디자이너를 쉽게 만들 수 있습니다 Windows Forms 응용 프로그램: 커서를 사용 하 여 컨트롤을 선택 하 고 폼의 원하는 위치에 배치 합니다. 모눈선 및 "맞춤선"와 같은 도구를 제공 하는 디자이너 컨트롤을 쉽게 배치할 합니다. 사용 하는지 여부 및 [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)] 또는 컴파일, 명령줄에서 사용할 수 있습니다는 <xref:System.Windows.Forms.FlowLayoutPanel>, <xref:System.Windows.Forms.TableLayoutPanel>및 <xref:System.Windows.Forms.SplitContainer>컨트롤을 만드는 고급 폼 레이아웃 최소한의 시간과 노력으로.</xref:System.Windows.Forms.SplitContainer> </xref:System.Windows.Forms.TableLayoutPanel> </xref:System.Windows.Forms.FlowLayoutPanel>  
  
### <a name="custom-ui-elements"></a>사용자 지정 UI 요소  
 마지막으로, 사용자 고유의 사용자 지정 UI 요소를 만들어야 하는 경우는 <xref:System.Drawing>선, 원 및 기타 도형을 폼에 직접 렌더링 해야 하는 클래스의 모든 네임 스페이스 포함.</xref:System.Drawing>  
  
 이러한 기능을 사용 하는 방법에 대 한 단계별 정보는 다음 도움말 항목을 참조 하십시오.  
  
|후|참조|  
|--------|---------|  
|와 새 Windows Forms 응용 프로그램 만들기[!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)]|[연습: 간단한 Windows Form 만들기](http://msdn.microsoft.com/en-us/2d9daec0-0543-41d0-acb1-964f685bddbb)|  
|폼에서 컨트롤 사용|[방법: Windows Forms에 컨트롤 추가](https://msdn.microsoft.com/library/0h5y8567.aspx)|   
|사용 하 여 그래픽 만들기<xref:System.Drawing></xref:System.Drawing>|[그래픽 프로그래밍 시작](https://msdn.microsoft.com/library/da0f23z7.aspx)|  
|사용자 지정 컨트롤 만들기|[방법: UserControl 클래스에서 상속](https://msdn.microsoft.com/library/00ctb4z0.aspx)|  
  
## <a name="displaying-and-manipulating-data"></a>데이터 표시 및 조작  
 많은 응용 프로그램은 데이터베이스, XML 파일, XML Web services 또는 기타 데이터 소스의 데이터를 표시해야 합니다. 라는 유연한 컨트롤을 제공 하는 Windows Forms는 <xref:System.Windows.Forms.DataGridView>이러한 표 형식 데이터를 기존의 행과 열 형식에서 렌더링 하는 모든 데이터의 조각이 해당 셀에 대 한 제어 합니다.</xref:System.Windows.Forms.DataGridView> 사용 하 여 <xref:System.Windows.Forms.DataGridView>개별 셀의 모양을 사용자 지정, 임의의 행과 열을, 잠금 및 다른 기능 중 에서도 셀 안에 복잡 한 컨트롤을 표시 합니다.</xref:System.Windows.Forms.DataGridView>  
  
 네트워크를 통해 데이터 소스에 연결하는 것은 Windows Forms 스마트 클라이언트에서 간단한 작업입니다. <xref:System.Windows.Forms.BindingSource>Windows Forms에 새로 추가 된 구성 요소 [!INCLUDE[vsprvslong](../../../csharp/misc/includes/vsprvslong_md.md)] 및 [!INCLUDE[dnprdnlong](../../../csharp/programming-guide/events/includes/dnprdnlong_md.md)], 데이터 원본에 대 한 연결을 나타내는 및 바인딩 컨트롤, 이전 및 다음 레코드로 이동, 레코드를 편집 및 다시 원래 소스에 변경 내용을 저장 하는 데이터에 대 한 메서드를 노출 합니다.</xref:System.Windows.Forms.BindingSource> <xref:System.Windows.Forms.BindingNavigator>통해 간단한 인터페이스를 제공 하는 컨트롤의 <xref:System.Windows.Forms.BindingSource>레코드를 탐색할 수 있도록 사용자에 대 한 구성 요소.</xref:System.Windows.Forms.BindingSource> </xref:System.Windows.Forms.BindingNavigator>  
  
### <a name="data-bound-controls"></a>데이터 바인딩 컨트롤  
 데이터 바인딩된 컨트롤을 프로젝트에 데이터 원본 데이터베이스, 웹 서비스, 개체 등을 표시 하는 데이터 소스 창을 사용 하 여 쉽게 만들 수 있습니다. 이 창에서 프로젝트의 폼으로 항목을 끌어 데이터 바인딩된 컨트롤을 만들 수 있습니다. 데이터 소스 창에서 기존 컨트롤로 개체를 끌어 기존 컨트롤을 데이터에 바인딩할 수도 있습니다.  
  
### <a name="settings"></a>설정  
 다른 형식의 데이터 바인딩은 Windows Forms에서 관리할 수 있는 설정입니다. 대부분의 스마트 클라이언트 응용 프로그램은 마지막으로 알려진 폼 크기와 같은 해당 런타임 상태에 대 한 일부 정보를 유지 하 고 저장 된 파일에 대 한 기본 위치와 같은 사용자 기본 설정 데이터를 유지 해야 합니다. 응용 프로그램 설정 기능은 클라이언트 컴퓨터에서 두 가지 유형의 설정 저장 하는 간편한 방법을 제공 하 여 이러한 요구 사항을 해결 합니다. 한 번 중 하나를 사용 하 여 정의 된 [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)] 또는 코드 편집기, 이러한 설정은 XML로 유지 되며 런타임에 자동으로 다시 메모리로 읽어옵니다.  
  
 이러한 기능을 사용 하는 방법에 대 한 단계별 정보는 다음 도움말 항목을 참조 하십시오.  
  
|후|참조|  
|--------|---------|  
|<xref:System.Windows.Forms.BindingSource>구성 요소</xref:System.Windows.Forms.BindingSource> 를 사용 하 여|[방법: Windows Forms 컨트롤에 BindingSource 구성 요소 디자이너를 사용 하 여 바인딩](https://msdn.microsoft.com/library/801dxw2t.aspx)|  
|작업할 [!INCLUDE[vstecado](../../../csharp/programming-guide/concepts/linq/includes/vstecado_md.md)] 데이터 원본|[방법: Windows Forms BindingSource 구성 요소와 ADO.NET 데이터 정렬 및 필터링](https://msdn.microsoft.com/library/ya3sah92.aspx)|  
|데이터 소스 창 사용|[연습: Windows Form에 데이터 표시](https://docs.microsoft.com/visualstudio/data-tools/accessing-data-in-visual-studio)|  
  
## <a name="deploying-applications-to-client-computers"></a>클라이언트 컴퓨터에 응용 프로그램 배포  
 응용 프로그램을 작성 한 후 설치 하 고 자신의 클라이언트 컴퓨터에서 실행할 수 있도록 사용자에 게 보낼 해야 있습니다. 사용 하는 [!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)] 기술, 내에서 응용 프로그램을 배포할 수 있습니다 [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)] 에서 간편 하 게 사용 하 고 사용자는 웹에서 응용 프로그램을 가리키는 URL에 제공 합니다. [!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)]모든 요소와 응용 프로그램에서 종속성을 관리 하 고 응용 프로그램이 클라이언트 컴퓨터에 제대로 설치 되어 있는지 확인 합니다.  
  
 사용자가 네트워크에 연결된 경우에만 실행되거나 온라인 및 오프라인 둘 다에서 실행되도록 [!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)] 응용 프로그램을 구성할 수 있습니다. 응용 프로그램이 오프 라인 작업을 지원 하도록 지정 하면 [!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)] 사용자의 응용 프로그램에 대 한 링크를 추가 **시작** 메뉴에서 사용자의 URL을 사용 하지 않고 열 수 있도록 합니다.  
  
 응용 프로그램을 업데이트하는 경우 새 배포 매니페스트와 응용 프로그램의 새 복사본을 웹 서버에 게시합니다. [!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)]사용 가능한 업데이트에 대 한 사용자의 설치, 업그레이드를 검색 합니다. 사용자 지정 프로그래밍 없이 이전 어셈블리를 업데이트 해야 합니다.  
  
 에 대 한 전체 개요에 대 한 [!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)], 참조 [ClickOnce 보안 및 배포](https://docs.microsoft.com/visualstudio/deployment/clickonce-security-and-deployment)합니다. 이러한 기능을 사용 하는 방법에 대 한 단계별 정보는 다음 도움말 항목을 참조 합니다.  
  
|후|참조|  
|--------|---------|  
|응용 프로그램 배포[!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)]|[방법: 게시 마법사를 사용하여 ClickOnce 응용 프로그램 게시](https://docs.microsoft.com/visualstudio/deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard)<br /><br /> [연습: ClickOnce 응용 프로그램 수동 배포](https://docs.microsoft.com/visualstudio/deployment/walkthrough-manually-deploying-a-clickonce-application)|  
|업데이트는 [!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)] 배포|[방법: ClickOnce 응용 프로그램에 대한 업데이트 관리](https://docs.microsoft.com/visualstudio/deployment/how-to-manage-updates-for-a-clickonce-application)|  
|사용 하는 보안 관리[!INCLUDE[ndptecclick](../../../visual-basic/developing-apps/printing/includes/ndptecclick_md.md)]|[방법: ClickOnce 보안 설정 사용](https://docs.microsoft.com/visualstudio/deployment/how-to-enable-clickonce-security-settings)|  
  
## <a name="other-controls-and-features"></a>기타 컨트롤 및 기능  
 Windows Forms에는 대화 상자 만들기, 인쇄, 도움말 및 설명서 추가 및 여러 언어로 응용 프로그램 지역화 지원과 같이 일반적인 작업을 쉽고 빠르게 구현할 수 있게 해주는 다른 여러 기능이 있습니다. Windows Forms의 강력한 보안 시스템에 의존 하는 또한는 [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)], 고객에 게 보다 안전한 응용 프로그램을 해제할 수 있습니다.  
  
 이러한 기능을 사용 하는 방법에 대 한 단계별 정보는 다음 도움말 항목을 참조 합니다.  
  
|후|참조|  
|--------|---------|  
|폼의 콘텐츠 인쇄|[방법: Windows Forms의 그래픽 인쇄](https://msdn.microsoft.com/library/741a0ktc.aspx)<br /><br /> [방법: Windows Forms에서 다중 페이지 텍스트 파일 인쇄](https://msdn.microsoft.com/library/cwbe712d.aspx)|   
|Windows Forms 보안에 대한 자세한 정보|[에서 보안 Windows Forms 개요](https://msdn.microsoft.com/library/90k49ccb.aspx)|  
  
## <a name="see-also"></a>참고 항목  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase></xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>   
 [Windows Forms 개요](https://msdn.microsoft.com/library/8bxxy49h.aspx)   
 [My.Forms 개체](../../../visual-basic/language-reference/objects/my-forms-object.md)
