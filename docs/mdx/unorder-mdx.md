---
description: Unorder (MDX)
title: Unorder (MDX) | Microsoft-Dokumentation
ms.date: 06/04/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: mdx
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
ms.openlocfilehash: 192f320ebc5257f2e6829e15fc40b8144208a521
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "88341177"
---
# <a name="unorder-mdx"></a>Unorder (MDX)


  Entfernt eine erzwungene Reihenfolge von einer angegebenen Menge.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Unorder(Set_Expression)   
```  
  
## <a name="arguments"></a>Argumente  
 *Set_Expression*  
 Ein gültiger MDX-Ausdruck (Multidimensional Expressions), der eine Menge zurückgibt.  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Unorder** -Funktion entfernt jede Sortierung, die für die Tupel in der Menge durch eine beliebige andere Funktion oder Anweisung, wie z. b. die [Order](../mdx/order-mdx.md) -Funktion, erzwungen wird. Die Reihenfolge der Tupel in der Menge, die von der Unorder-Funktion zurückgegeben wird, ist **unbestimmt** .  
  
 Die **Unorder** -Funktion wird als Hinweis für die Abfrageoptimierung für die festgelegte Verarbeitung verwendet. Wenn die Reihenfolge der Tupel in einer Menge für eine Berechnung oder Abfrage unwichtig ist, kann die Verwendung der **Unorder** -Funktion in solchen Fällen einen Leistungsvorteil bieten. Beispielsweise kann die [NonEmpty (MDX)](../mdx/nonempty-mdx.md) -Funktion besser funktionieren, wenn der für diese Funktion bereitgestellte Satz ungeordnet ist, als wenn die [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] Reihenfolge beibehalten muss, obwohl mit [!INCLUDE[ssASCurrent](../includes/ssascurrent-md.md)] der Abfrage Prozessor versucht, diese Funktion für viele Funktionen, wie z. b. **Sum** und **Aggregate**, automatisch auszuführen. Der Leistungsvorteil der Verwendung von " **Unorder** " ist nur bei sehr großen Mengen, die aus Millionen von Tupeln bestehen, wahrscheinlich erkennbar.  
  
## <a name="example"></a>Beispiel  
 Der folgende Pseudocode veranschaulicht die Syntax für diese Funktion.  
  
```  
NonEmpty (UnOrder (<set_expression>))  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [MDX-Funktionsreferenz &#40;MDX&#41;](../mdx/mdx-function-reference-mdx.md)  
  
  
