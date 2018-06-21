---
title: Równoczesne uruchamianie poleceń cmdlet przy użyciu zadań programu PowerShell
description: Sposób równoległego uruchamiania poleceń cmdlet za pomocą parametru -AsJob.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: dfc1efa752c9c9fa42ad5904adacd83c2dc333b8
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911939"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>Równoczesne uruchamianie poleceń cmdlet przy użyciu zadań programu PowerShell

Program PowerShell obsługuje akcję asynchroniczną przy użyciu [zadań programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).
Program Azure PowerShell w znacznej mierze zależy od wykonywania wywołań sieci do platformy Azure i oczekiwania na nie. Jako deweloper możesz często wykonywać wiele nieblokujących wywołań do platformy Azure w skrypcie lub tworzyć zasoby platformy Azure w rozwiązaniu REPL bez blokowania bieżącej sesji. Aby zaspokoić te potrzeby, program Azure PowerShell oferuje najwyższej jakości obsługę zadań [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="context-persistence-and-psjobs"></a>Stan trwały kontekstu i zadania PSJob

Zadania PSJob są uruchamiane w ramach osobnych procesów, co oznacza, że informacje o połączeniu z platformą Azure muszą zostać prawidłowo udostępnione tworzonym zadaniom. Po połączeniu konta platformy Azure z sesją programu PowerShell przy użyciu polecenia `Connect-AzureRmAccount` można przekazać kontekst do zadania.

```powershell
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

Jeśli jednak kontekst ma być zapisywany automatycznie przy użyciu polecenia `Enable-AzureRmContextAutosave`, będzie on automatycznie udostępniany wszystkim tworzonym zadaniom.

```powershell
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a>Zadania automatyczne z parametrem `-AsJob`

Dla wygody w przypadku niektórych długotrwałych poleceń cmdlet program Azure PowerShell oferuje również przełącznik `-AsJob`.
Przełącznik `-AsJob` sprawia, że tworzenie zadań PSJob jest jeszcze łatwiejsze.

```powershell
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

W dowolnym momencie można przeprowadzić inspekcję zadania i postępu przy użyciu poleceń `Get-Job` i `Get-AzureRmVM`.

```powershell
Get-Job $job
Get-AzureRmVM MyVm
```

```Output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

Następnie po ukończeniu można uzyskać wynik zadania przy użyciu polecenia `Receive-Job`.

> [!NOTE]
> Polecenie `Receive-Job` zwraca wynik z polecenia cmdlet tak, jakby flaga `-AsJob` nie istniała.
> Na przykład wynik polecenia `Receive-Job` dla polecenia `Do-Action -AsJob` jest taki sam jak wynik polecenia `Do-Action`.

```powershell
$vm = Receive-Job $job
$vm
```

```Output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a>Przykładowe scenariusze

Utwórz równocześnie wiele maszyn wirtualnych.

```powershell
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

W tym przykładzie polecenie cmdlet `Wait-Job` powoduje wstrzymanie skryptu w czasie działania zadań. Wykonywanie skryptu jest kontynuowane po ukończeniu wszystkich zadań. Dzięki temu możesz utworzyć kilka zadań uruchamianych równolegle, a następnie zaczekać na ukończenie przed kontynuowaniem.

```Output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
