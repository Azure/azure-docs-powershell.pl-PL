---
title: Często zadawane pytania
description: Często zadawane pytania dotyczące usługi Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239387"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Często zadawane pytania dotyczące usługi Azure PowerShell

## <a name="what-is-azure-powershell"></a>Co to jest Azure PowerShell?

Azure PowerShell to zestaw poleceń cmdlet, który umożliwia zarządzanie zasobami platformy Azure bezpośrednio przy użyciu programu PowerShell. W grudniu 2018 r. moduł Az programu PowerShell stał się ogólnie dostępny. Jest to teraz zalecany moduł programu PowerShell na potrzeby interakcji z platformą Azure. Aby dowiedzieć się więcej na temat modułu Az programu PowerShell, zobacz [Wprowadzenie do nowego modułu Az usługi Azure PowerShell](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Jak mogę wyłączyć komunikaty ostrzegawcze o zmianach powodujących niezgodność w usłudze Azure PowerShell?

Aby pomijać komunikaty ostrzegawcze o zmianach powodujących niezgodność w usłudze Azure PowerShell, należy ustawić zmienną środowiskową `SuppressAzurePowerShellBreakingChangeWarnings` na wartość `true`.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
