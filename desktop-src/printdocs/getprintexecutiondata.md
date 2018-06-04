---
Description: The GetPrintExecutionData retrieves the current print context.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: GetPrintExecutionData function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# GetPrintExecutionData function

The **GetPrintExecutionData** retrieves the current print context.

> [!Note]  
> This function is intended for use by printer drivers that are running in the context of the print spooler.

 

## Syntax


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## Parameters

<dl> <dt>

*pData* \[out\]
</dt> <dd>

A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.

</dd> </dl>

## Return value

Returns **TRUE** if the function succeeds; otherwise **FALSE**. If the return value is **FALSE**, call [**GetLastError**](https://msdn.microsoft.com/library/windows/desktop/ms679360) to get the error status.

## Remarks

Printer drivers should call [**GetProcAddress**](https://msdn.microsoft.com/library/windows/desktop/ms683212) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.

**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.

The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**. If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.

## Requirements



|                                     |                                                                                                           |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008 R2 \[desktop apps only\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## See also

<dl> <dt>

[**GetLastError**](https://msdn.microsoft.com/library/windows/desktop/ms679360)
</dt> <dt>

[**GetProcAddress**](https://msdn.microsoft.com/library/windows/desktop/ms683212)
</dt> <dt>

[**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md)
</dt> <dt>

[**PRINT\_EXECUTION\_DATA**](print-execution-data.md)
</dt> </dl>

 

 



