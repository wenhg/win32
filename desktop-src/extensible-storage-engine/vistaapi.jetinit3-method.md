---
title: VistaApi.JetInit3 method  (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name: 
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type: 
- kbSyntax
- apiref
api_type: 
- Managed
api_location: 
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW

---

# VistaApi.JetInit3 method

Initialize the ESENT database engine.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](hh558039\(v=exchg.10\).md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## Syntax

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### Parameters

  - instance  
    Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](hh564593\(v=exchg.10\).md)  
    
    The instance to initialize. If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.

<!-- end list -->

  - recoveryOptions  
    Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](dn335235\(v=exchg.10\).md)  
    
    Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.

<!-- end list -->

  - grbit  
    Type: [Microsoft.Isam.Esent.Interop.InitGrbit](hh596658\(v=exchg.10\).md)  
    
    Initialization options.

#### Return value

Type: [Microsoft.Isam.Esent.Interop.JET_wrn](hh557250\(v=exchg.10\).md)  
A warning code.  

## See also

#### Reference

[VistaApi class](dn335321\(v=exchg.10\).md)

[VistaApi members](dn335317\(v=exchg.10\).md)

[Microsoft.Isam.Esent.Interop.Vista namespace](hh558039\(v=exchg.10\).md)

