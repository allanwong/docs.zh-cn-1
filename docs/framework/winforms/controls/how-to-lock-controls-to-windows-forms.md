---
title: 如何：将控件锁定到 Windows 窗体
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, locking
- controls [Windows Forms], locking
ms.assetid: 94efe0d2-c14e-4d14-b903-63ea9b07e290
ms.openlocfilehash: ac5fbf33564ed2dd1a030132a35b36164f777519
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59301693"
---
# <a name="how-to-lock-controls-to-windows-forms"></a>如何：将控件锁定到 Windows 窗体
设计 Windows 应用程序用户界面 (UI)，便可锁定控件后它们正确定位，以便不会无意中执行移动或调整其大小设置其他属性时。  
  
 此外，可以锁定和解锁所有窗体控件，这适用于许多控件与窗体，也可以解锁各个控件。 一旦已放置的所有控件在窗体上所需的位置，其所有进行锁定以防止错误的移动。  
  
> [!NOTE]
>  显示的对话框和菜单命令可能会与“帮助”中的描述不同，具体取决于你现用的设置或版本。 若要更改设置，请在 **“工具”** 菜单上选择 **“导入和导出设置”** 。 有关详细信息，请参阅[个性化设置 Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide)。  
  
### <a name="to-lock-a-control"></a>若要锁定控件  
  
1. 在中**属性**窗口中，单击**锁定**属性，然后选择`true`。 （双击名称切换属性设置。）  
  
     或者，右键单击该控件，选择**锁定控件**。  
  
    > [!NOTE]
    >  锁定控件可以防止它们在设计图面上拖动到新的大小或位置。 但是，你仍可以更改的大小或通过控件的位置**属性**窗口或代码中。  
  
### <a name="to-lock-all-the-controls-on-a-form"></a>若要在窗体上的所有控件都锁定  
  
1. 从**格式**菜单中，选择**锁定控件**。  
  
    > [!NOTE]
    >  此命令将锁定窗体的大小，因为窗体是一个控件。  
  
### <a name="to-unlock-all-locked-controls-on-a-form"></a>若要解锁窗体上的所有已锁定的控件  
  
1. 从**格式**菜单中，选择**锁定控件**。  
  
     在窗体上的所有以前锁定的控件现在是解锁。  
  
### <a name="to-unlock-locked-controls-individually"></a>若要单独解锁锁定的控件  
  
1. 在中**属性**窗口中，单击**锁定**属性，然后选择`false`。 （双击名称切换属性设置。）  
  
## <a name="see-also"></a>请参阅

- [Windows 窗体控件](index.md)
- [在 Windows 窗体上排列控件](arranging-controls-on-windows-forms.md)
- [标记各个 Windows 窗体控件并创建它们的快捷键](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [在 Windows 窗体上使用的控件](controls-to-use-on-windows-forms.md)
- [按功能列出的 Windows 窗体控件](windows-forms-controls-by-function.md)
