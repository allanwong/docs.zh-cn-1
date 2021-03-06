---
title: 如何：绘制单个 B&#233;zier 样条
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines [Windows Forms], drawing
- drawing [Windows Forms], Bezier splines
ms.assetid: f4f3fe30-f0a6-4743-ac91-11310cebea9f
ms.openlocfilehash: ebb53e7df979a553ed4a44deba34345c9ecac772
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59171673"
---
# <a name="how-to-draw-a-single-b233zier-spline"></a>如何：绘制单个 B&#233;zier 样条
由四个点定义的贝塞尔样条： 一个起点，这两个控制点和终结点。  
  
## <a name="example"></a>示例  
 下面的示例绘制使用 （10，100） 的起始点和终结点 （200，100） 的贝塞尔样条。 两个控制点为 （100，10） 和 （150，150）。  
  
 下图显示了生成的贝塞尔样条以及其开始点、 控点和终结点。 该插图还显示自由绘制曲线的凸包，这是通过使用直线连接四个点而形成的多边形。  
  
 ![贝塞尔样条图。](./media/how-to-draw-a-single-bezier-spline/bezier-spline-illustration.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>编译代码  
 前面的示例专用于 Windows 窗体，并且它需要<xref:System.Windows.Forms.PaintEventArgs> `e`，这是一个参数的<xref:System.Windows.Forms.Control.Paint>事件处理程序。  
  
## <a name="see-also"></a>请参阅

- <xref:System.Drawing.Graphics.DrawBezier%2A>
- [GDI+ 中的贝塞尔自由绘制曲线](bezier-splines-in-gdi.md)
- [如何：绘制一系列贝塞尔自由绘制曲线](how-to-draw-a-sequence-of-bezier-splines.md)
