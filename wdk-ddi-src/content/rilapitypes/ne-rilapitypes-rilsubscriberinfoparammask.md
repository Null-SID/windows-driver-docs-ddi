---
UID: NE:rilapitypes.RILSUBSCRIBERINFOPARAMMASK
title: RILSUBSCRIBERINFOPARAMMASK (rilapitypes.h)
description: "Microsoft reserves the RILSUBSCRIBERINFOPARAMMASK enumeration for internal use only. Don't use this enumeration in your code."
old-location: netvista\rilsubscriberinfoparammask_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILSUBSCRIBERINFOPARAMMASK enumeration"]
ms.keywords: RILSUBSCRIBERINFOPARAMMASK, RILSUBSCRIBERINFOPARAMMASK enumeration [Network Drivers Starting with Windows Vista], RIL_PARAM_SI_ALL, RIL_PARAM_SI_DESCRIPTION, RIL_PARAM_SI_SERVICE, netvista.rilsubscriberinfoparammask_2, rilapitypes/RILSUBSCRIBERINFOPARAMMASK, rilapitypes/RIL_PARAM_SI_ALL, rilapitypes/RIL_PARAM_SI_DESCRIPTION, rilapitypes/RIL_PARAM_SI_SERVICE
req.header: rilapitypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RILSUBSCRIBERINFOPARAMMASK
req.product: Windows 10 or later.
f1_keywords:
 - RILSUBSCRIBERINFOPARAMMASK
 - rilapitypes/RILSUBSCRIBERINFOPARAMMASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILSUBSCRIBERINFOPARAMMASK
---

# RILSUBSCRIBERINFOPARAMMASK enumeration (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -enum-fields

### -field RIL_PARAM_SI_ADDRESS

### -field RIL_PARAM_SI_DESCRIPTION

### -field RIL_PARAM_SI_SERVICE

### -field RIL_PARAM_SI_ALL

## -syntax

```cpp
typedef enum _RILSUBSCRIBERINFOPARAMMASK {
  RIL_PARAM_SI_DESCRIPTION,
  RIL_PARAM_SI_SERVICE,
  RIL_PARAM_SI_ALL
} RILSUBSCRIBERINFOPARAMMASK;
```

