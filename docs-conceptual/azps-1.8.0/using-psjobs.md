---
title: Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell
description: Dowiedz się, jak uruchamiać polecenia cmdlet środowiska Azure PowerShell równolegle lub jako zadania w tle przy użyciu opcji -AsJob i Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b76e310e1677e539927ebc4746df67c1d1accc16
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407993"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell

Środowisko Azure PowerShell polega na nawiązywaniu połączenia z chmurą platformy Azure i oczekiwaniu na odpowiedzi, dlatego większość tych poleceń cmdlet blokuje sesję programu PowerShell do czasu uzyskania odpowiedzi z chmury.
Zadania programu PowerShell umożliwiają uruchamianie poleceń cmdlet w tle lub jednoczesne wykonywanie wielu zadań na platformie Azure w ramach jednej sesji programu PowerShell.

Ten artykuł zawiera krótkie omówienie sposobu uruchamiania poleceń cmdlet środowiska Azure PowerShell jako zadań programu PowerShell i sprawdzania, czy zostały one ukończone. Uruchamianie poleceń w środowisku Azure PowerShell wymaga używania kontekstów środowiska Azure PowerShell, które szczegółowo opisano w sekcji [Poświadczenia logowania i konteksty platformy Azure](context-persistence.md).
Aby dowiedzieć się więcej na temat zadań programu PowerShell, zobacz [Informacje o zadaniach programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>Konteksty platformy Azure z zadaniami programu PowerShell

Zadania programu PowerShell są uruchamiane jako oddzielne procesy bez dołączonej sesji programu PowerShell, dlatego Twoje poświadczenia platformy Azure muszą być im udostępnione. Poświadczenia są przekazywane jako obiekty kontekstu platformy Azure przy użyciu jednej z tych metod:

* Automatyczna trwałość kontekstu. Trwałość kontekstu jest domyślnie włączona i zachowuje informacje logowania w wielu sesjach. Po włączeniu trwałości kontekstu bieżący kontekst platformy Azure jest przenoszony do nowego procesu:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Użyj parametru `-AzContext` z dowolnymi poleceniami cmdlet środowiska Azure PowerShell, aby udostępnić obiekt kontekstu platformy Azure:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Jeśli trwałość kontekstu jest wyłączona, wymagany jest argument `-AzContext`.

* Użyj przełącznika `-AsJob` dostarczanego przez niektóre polecenia cmdlet środowiska Azure PowerShell. Ten przełącznik automatycznie uruchamia polecenie cmdlet jako zadanie programu PowerShell przy użyciu obecnie aktywnego kontekstu platformy Azure:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Aby sprawdzić, czy polecenie cmdlet obsługuje przełącznik `-AsJob`, zapoznaj się z jego dokumentacją referencyjną. Przełącznik `-AsJob` nie wymaga, aby automatyczne zapisywanie kontekstu było włączone.

Stan uruchomionego zadania można sprawdzić przy użyciu polecenia cmdlet [Get-Job](/powershell/module/microsoft.powershell.core/get-job). Aby pobrać dane wyjściowe z zadania do tej pory, użyj polecenia cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).

Aby sprawdzić postęp operacji zdalnie na platformie Azure, użyj poleceń cmdlet `Get-` skojarzonych z typem zasobu modyfikowanym przez zadanie:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Zobacz też

* [Konteksty środowiska Azure PowerShell](context-persistence.md)
* [Informacje o zadaniach programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Dokumentacja polecenia Get-Job](/powershell/module/microsoft.powershell.core/get-job)
* [Dokumentacja polecenia Receive-Job](/powershell/module/microsoft.powershell.core/receive-job)
