---
UID: NS:wdm._PCI_EXPRESS_ROOT_ERROR_STATUS
title: _PCI_EXPRESS_ROOT_ERROR_STATUS (wdm.h)
description: The _PCI_EXPRESS_ROOT_ERROR_STATUS structure (wdm.h) describes a PCI Express (PCIe) root error status register for advanced error reporting.
old-location: pci\pci_express_root_error_status.htm
tech.root: PCI
ms.date: 02/24/2018
keywords: ["PCI_EXPRESS_ROOT_ERROR_STATUS structure"]
ms.keywords: "*PPCI_EXPRESS_ROOT_ERROR_STATUS, PCI.pci_express_root_error_status, PCI_EXPRESS_ROOT_ERROR_STATUS, PCI_EXPRESS_ROOT_ERROR_STATUS union [Buses], PPCI_EXPRESS_ROOT_ERROR_STATUS, PPCI_EXPRESS_ROOT_ERROR_STATUS union pointer [Buses], _PCI_EXPRESS_ROOT_ERROR_STATUS, pci_struct_8b730780-dc4a-4873-8efd-fb6df47f7c8f.xml, wdm/PCI_EXPRESS_ROOT_ERROR_STATUS, wdm/PPCI_EXPRESS_ROOT_ERROR_STATUS"
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h, Miniport.h
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
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL (see Remarks section)
targetos: Windows
req.typenames: PCI_EXPRESS_ROOT_ERROR_STATUS, *PPCI_EXPRESS_ROOT_ERROR_STATUS
req.product: Windows 10 or later.
f1_keywords:
 - _PCI_EXPRESS_ROOT_ERROR_STATUS
 - wdm/_PCI_EXPRESS_ROOT_ERROR_STATUS
 - PPCI_EXPRESS_ROOT_ERROR_STATUS
 - wdm/PPCI_EXPRESS_ROOT_ERROR_STATUS
 - PCI_EXPRESS_ROOT_ERROR_STATUS
 - wdm/PCI_EXPRESS_ROOT_ERROR_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - _PCI_EXPRESS_ROOT_ERROR_STATUS
 - PPCI_EXPRESS_ROOT_ERROR_STATUS
 - PCI_EXPRESS_ROOT_ERROR_STATUS
---

# _PCI_EXPRESS_ROOT_ERROR_STATUS structure (wdm.h)


## -description

The PCI_EXPRESS_ROOT_ERROR_STATUS structure describes a PCI Express (PCIe) root error status register of a PCIe advanced error reporting capability structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_ROOT_ERROR_STATUS structure.


### -field DUMMYSTRUCTNAME.AdvancedErrorInterruptMessageNumber

The MSI/MSI-X vector that is used for the interrupt messages that are generated in association with any of the status bits of the advanced error reporting capability.


### -field DUMMYSTRUCTNAME.CorrectableErrorReceived

A single bit that indicates that a correctable error message has been received.


### -field DUMMYSTRUCTNAME.FatalErrorMessagesReceived

A single bit that indicates that one or more non-fatal uncorrectable error messages have been received.


### -field DUMMYSTRUCTNAME.FirstUncorrectableFatal

A single bit that indicates that the first uncorrectable error message that was received was for a fatal error.


### -field DUMMYSTRUCTNAME.MultipleCorrectableErrorsReceived

A single bit that indicates that multiple correctable error messages have been received.


### -field DUMMYSTRUCTNAME.MultipleUncorrectableErrorsReceived

A single bit that indicates that multiple uncorrectable error messages have been received.


### -field DUMMYSTRUCTNAME.NonFatalErrorMessagesReceived

A single bit that indicates that one or more non-fatal uncorrectable error messages have been received.


### -field DUMMYSTRUCTNAME.Reserved

Reserved.


### -field DUMMYSTRUCTNAME.UncorrectableErrorReceived

A single bit that indicates that an uncorrectable error message has been received.

## -syntax

```cpp
typedef union _PCI_EXPRESS_ROOT_ERROR_STATUS {
  struct {
    ULONG CorrectableErrorReceived  :1;
    ULONG MultipleCorrectableErrorsReceived  :1;
    ULONG UncorrectableErrorReceived  :1;
    ULONG MultipleUncorrectableErrorsReceived  :1;
    ULONG FirstUncorrectableFatal  :1;
    ULONG NonFatalErrorMessagesReceived  :1;
    ULONG FatalErrorMessagesReceived  :1;
    ULONG Reserved  :20;
    ULONG AdvancedErrorInterruptMessageNumber  :5;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_ROOT_ERROR_STATUS, *PPCI_EXPRESS_ROOT_ERROR_STATUS;
```

## -remarks

The PCI_EXPRESS_ROOT_ERROR_STATUS structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_ROOT_ERROR_STATUS structure is contained in the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_rootport_aer_capability">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_rootport_aer_capability">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>

