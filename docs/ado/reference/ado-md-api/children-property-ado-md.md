---
description: Children-Eigenschaft (ADO MD)
title: Children-Eigenschaft (ADO MD) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Member::Children
- Children
helpviewer_keywords:
- Children property [ADO MD]
ms.assetid: 61d36468-1ccd-467a-9cb5-17d0bfacc766
author: rothja
ms.author: jroth
ms.openlocfilehash: 81cbaddf1db2017384392e20b249b9c1beb3ccd0
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99169919"
---
# <a name="children-property-ado-md"></a>Children-Eigenschaft (ADO MD)
Gibt eine [Members](./members-collection-ado-md.md) -Auflistung zurück, für die [das aktuelle Element](./member-object-ado-md.md) das übergeordnete Element in der Hierarchie ist.  
  
## <a name="return-values"></a>Rückgabewerte  
 Gibt eine **Members** -Auflistung zurück und ist schreibgeschützt.  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Children** -Eigenschaft enthält eine **Members** -Auflistung, für die **das aktuelle Element** das hierarchische übergeordnete Element ist. Element Objekte **auf** Blatt Ebene verfügen über keine untergeordneten Elemente in der **Members** -Auflistung. Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Ebenenobjekt](./level-object-ado-md.md) gehören. Ein Fehler tritt auf, **Wenn von Element** Objekten, die zu einem [Positions](./position-object-ado-md.md) Objekt gehören, auf diese Eigenschaft verwiesen wird.  
  
## <a name="applies-to"></a>Gilt für  
 [Member-Objekt (ADO MD)](./member-object-ado-md.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [ChildCount-Eigenschaft (ADO MD)](./childcount-property-ado-md.md)