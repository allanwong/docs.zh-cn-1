---
title: 检索元数据
ms.date: 03/30/2017
helpviewer_keywords:
- metadata [WCF], retrieving
ms.assetid: 18d8ba4c-af0f-4827-a50b-4202d767bacc
ms.openlocfilehash: bb415d88c2bae75cb16aa137bdf867eb463afa63
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59152394"
---
# <a name="retrieving-metadata"></a>检索元数据
元数据检索是从元数据终结点（如 WS-MetadataExchange (MEX) 元数据终结点或 HTTP/GET 元数据终结点）请求和检索元数据的过程。  
  
## <a name="retrieving-metadata-from-the-command-line-using-svcutilexe"></a>从命令行使用 Svcutil.exe 检索元数据  
 您可以检索服务元数据通过使用 Ws-metadataexchange 或 HTTP/GET 请求[ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)工具并传递`/target:metadata`开关和地址。 Svcutil.exe 在指定地址下载元数据并将文件保存到磁盘上。 Svcutil.exe 在内部使用一个 <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 实例，并从配置中加载名称与作为输入传递给 Svcutil.exe 的地址方案相匹配的 <xref:System.ServiceModel.Description.IMetadataExchange> 终结点配置。  
  
## <a name="retrieving-metadata-programmatically-using-the-metadataexchangeclient"></a>使用 MetadataExchangeClient 以编程方式检索元数据  
 Windows Communication Foundation (WCF) 可以检索服务元数据使用标准的协议如 Ws-metadataexchange 和 HTTP/GET 请求。 这两种协议均受 <xref:System.ServiceModel.Description.MetadataExchangeClient> 类型支持。 您可以通过提供元数据终结点的地址和一个可选绑定，使用 <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 类型来检索服务元数据。 由 <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 实例使用的绑定可以是 <xref:System.ServiceModel.Description.MetadataExchangeBindings> 静态类中的默认绑定之一、用户提供的绑定或从 `IMetadataExchange` 协定的终结点配置加载的绑定。 <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 也可以使用 <xref:System.Net.HttpWebRequest> 类型来解析 HTTP URL 对元数据的引用。  
  
 默认情况下，<xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 实例与单个 <xref:System.ServiceModel.ChannelFactory> 实例关联。 通过重写 <xref:System.ServiceModel.ChannelFactory?displayProperty=nameWithType> 虚拟方法，您可以更改或替换由 <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 使用的 <xref:System.ServiceModel.Description.MetadataExchangeClient.GetChannelFactory%2A> 实例。 同样，通过重写 <xref:System.Net.HttpWebRequest> 虚拟方法，可以更改或替换由 <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 使用的 <xref:System.ServiceModel.Description.MetadataExchangeClient.GetWebRequest%2A?displayProperty=nameWithType> 实例以发出 HTTP/GET 请求。  
  
## <a name="in-this-section"></a>本节内容  
 [如何：使用 Svcutil.exe 下载元数据文档](../../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)  
 演示如何使用 Svcutil.exe to 下载元数据文档。  
  
 [如何：使用 MetadataResolver 动态获取绑定元数据](../../../../docs/framework/wcf/feature-details/how-to-use-metadataresolver-to-obtain-binding-metadata-dynamically.md)  
 演示如何使用 <xref:System.ServiceModel.Description.MetadataResolver?displayProperty=nameWithType> 在运行时动态获取绑定元数据。  
  
 [如何：使用 MetadataExchangeClient 检索元数据](../../../../docs/framework/wcf/feature-details/how-to-use-metadataexchangeclient-to-retrieve-metadata.md)  
 演示如何使用 <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> 类将元数据文件下载到包含要写入到文件或用于其他用途的 <xref:System.ServiceModel.Description.MetadataSet?displayProperty=nameWithType> 对象的 <xref:System.ServiceModel.Description.MetadataSection?displayProperty=nameWithType> 对象。  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Description.MetadataExchangeClient>
