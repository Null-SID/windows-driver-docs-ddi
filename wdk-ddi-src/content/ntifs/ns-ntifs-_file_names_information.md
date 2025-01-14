---
UID: NS:ntifs._FILE_NAMES_INFORMATION
title: FILE_NAMES_INFORMATION (ntifs.h)
description: A FILE_NAMES_INFORMATION structure used to query detailed information about the names of files in a directory.
old-location: ifsk\file_names_information.htm
tech.root: ifsk
ms.date: 07/26/2022
keywords: ["FILE_NAMES_INFORMATION structure"]
ms.keywords: "*PFILE_NAMES_INFORMATION, FILE_NAMES_INFORMATION, FILE_NAMES_INFORMATION structure [Installable File System Drivers], PFILE_NAMES_INFORMATION, PFILE_NAMES_INFORMATION structure pointer [Installable File System Drivers], _FILE_NAMES_INFORMATION, fileinformationstructures_8349a2eb-ffeb-4050-9084-b09474079415.xml, ifsk.file_names_information, ntifs/FILE_NAMES_INFORMATION, ntifs/PFILE_NAMES_INFORMATION"
req.header: ntifs.h
req.include-header: Ntifs.h, Fltkernel.h
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
req.irql: 
targetos: Windows
req.typenames: FILE_NAMES_INFORMATION, *PFILE_NAMES_INFORMATION
f1_keywords:
 - _FILE_NAMES_INFORMATION
 - ntifs/_FILE_NAMES_INFORMATION
 - PFILE_NAMES_INFORMATION
 - ntifs/PFILE_NAMES_INFORMATION
 - FILE_NAMES_INFORMATION
 - ntifs/FILE_NAMES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - _FILE_NAMES_INFORMATION
 - PFILE_NAMES_INFORMATION
 - FILE_NAMES_INFORMATION
---

# FILE_NAMES_INFORMATION structure

## -description

A **FILE_NAMES_INFORMATION** structure used to query detailed information about the names of files in a directory.

## -struct-fields

### -field NextEntryOffset

Byte offset for the next FILE_NAMES_INFORMATION entry, if multiple entries are present in a buffer. This member is zero if no other entries follow this one.

### -field FileIndex

Byte offset of the file within the parent directory. This member is undefined for file systems, such as NTFS, in which the position of a file within the parent directory is not fixed and can be changed at any time to maintain sort order.

### -field FileNameLength

Specifies the length of the file name string.

### -field FileName

Specifies the first character of the file name string. This is followed in memory by the remainder of the string.

## -remarks

This information can be queried in either of the following ways:

* Call [**ZwQueryDirectoryFile**](nf-ntifs-zwqueryvirtualmemory.md), passing FileNamesInformation as the value of **FileInformationClass** and passing a caller-allocated, FILE_NAMES_INFORMATION-structured buffer as the value of **FileInformation**.

* Create an IRP with major function code IRP_MJ_DIRECTORY_CONTROL and minor function code IRP_MN_QUERY_DIRECTORY.

No specific access rights are required to query this information.

This structure must be aligned on a LONG (4-byte) boundary. If a buffer contains two or more of these structures, the **NextEntryOffset** value in each entry, except the last, falls on a 4-byte boundary.

## -see-also

[**FsRtlNotifyFullChangeDirectory**](nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlnotifyfullchangedirectory.md)

[**IRP_MJ_DIRECTORY_CONTROL**](/windows-hardware/drivers/ifs/irp-mj-directory-control)

[**ZwQueryDirectoryFile**](nf-ntifs-zwqueryvirtualmemory.md)
