---
UID: NN:tsvirtualchannels.IWTSVirtualChannelCallback
title: IWTSVirtualChannelCallback (tsvirtualchannels.h)
description: Receives notifications about channel state changes or data received.helpviewer_keywords: ["IWTSVirtualChannelCallback","IWTSVirtualChannelCallback interface [Remote Desktop Services]","IWTSVirtualChannelCallback interface [Remote Desktop Services]","described","termserv.iwtsvirtualchannelcallback","tsvirtualchannels/IWTSVirtualChannelCallback"]
old-location: termserv\iwtsvirtualchannelcallback.htm
tech.root: TermServ
ms.assetid: d90c6f80-ed4c-4b99-af85-d2c5816ade85
ms.date: 12/05/2018
ms.keywords: IWTSVirtualChannelCallback, IWTSVirtualChannelCallback interface [Remote Desktop Services], IWTSVirtualChannelCallback interface [Remote Desktop Services],described, termserv.iwtsvirtualchannelcallback, tsvirtualchannels/IWTSVirtualChannelCallback
f1_keywords:
- tsvirtualchannels/IWTSVirtualChannelCallback
dev_langs:
- c++
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- TsVirtualChannels.h
api_name:
- IWTSVirtualChannelCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSVirtualChannelCallback interface


## -description


Receives notifications about channel state changes or data received. This interface is implemented by the user. Each instance of this interface is associated with one instance of <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannel">IWTSVirtualChannel</a>.

Implementation of this interface should not block these calls, because this may suppress other callbacks. It is not guaranteed that these calls will always arrive on the same thread, even for in-process COM implementation of the plug-in. Calls to the <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-write">Write</a> and <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-close">Close</a> methods of <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannel">IWTSVirtualChannel</a> are permitted within these callbacks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSVirtualChannelCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSVirtualChannelCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSVirtualChannelCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannelcallback-onclose">OnClose</a>
</td>
<td align="left" width="63%">
Notifies the user that the channel has been closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannelcallback-ondatareceived">OnDataReceived</a>
</td>
<td align="left" width="63%">
Notifies the user about data that is being received.

</td>
</tr>
</table> 

