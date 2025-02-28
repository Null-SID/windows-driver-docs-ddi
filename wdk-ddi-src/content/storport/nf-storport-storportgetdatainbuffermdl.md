---
UID: NF:storport.StorPortGetDataInBufferMdl
title: StorPortGetDataInBufferMdl function (storport.h)
description: Returns an MDL associated with the input data buffer of a SCSI request block (SRB).
old-location: storage\storportgetdatainbuffermdl.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["StorPortGetDataInBufferMdl function"]
ms.keywords: StorPortGetDataInBufferMdl, StorPortGetDataInBufferMdl routine [Storage Devices], storage.storportgetdatainbuffermdl, storport/StorPortGetDataInBufferMdl
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Storport.lib
req.dll: 
req.irql: Any
targetos: Windows
req.typenames: 
f1_keywords:
 - StorPortGetDataInBufferMdl
 - storport/StorPortGetDataInBufferMdl
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Storport.lib
 - Storport.dll
api_name:
 - StorPortGetDataInBufferMdl
---

# StorPortGetDataInBufferMdl function


## -description

Returns an MDL associated with the input data buffer  of a SCSI request block (SRB).

## -parameters

### -param HwDeviceExtension [in]


A pointer to the hardware device extension for the host bus adapter (HBA).

### -param Srb [in]


The request block to containing the data described by the MDL pointed to by <i>Mdl</i>.

### -param Mdl [out]


A pointer to  an MDL address to receive the MDL for <i>Srb</i>.

## -returns

A status value indicating the result of the notification. This can be one of these values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The MDL for <i>Srb</i> was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STOR_STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The pointer value in <i>Mdl</i> is NULL.

</td>
</tr>
</table>

## -see-also

<a href="/windows-hardware/drivers/ddi/storport/nf-storport-storportgetdatainbufferscattergatherlist">StorPortGetDataInBufferScatterGatherList</a>



<a href="/windows-hardware/drivers/ddi/storport/nf-storport-storportgetdatainbuffersystemaddress">StorPortGetDataInBufferSystemAddress</a>
