---
title: Równoczesne uruchamianie poleceń cmdlet przy użyciu zadań programu PowerShell
description: Sposób równoległego uruchamiania poleceń cmdlet za pomocą parametru -AsJob.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: cf5e9d6e461ee7fde1e307db885c37e31decb510
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/23/2018
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="69bb9-103">Równoczesne uruchamianie poleceń cmdlet przy użyciu zadań programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="69bb9-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="69bb9-104">Program PowerShell obsługuje akcję asynchroniczną przy użyciu [zadań programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="69bb9-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="69bb9-105">Program Azure PowerShell w znacznej mierze zależy od wykonywania wywołań sieci do platformy Azure i oczekiwania na nie.</span><span class="sxs-lookup"><span data-stu-id="69bb9-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="69bb9-106">Jako deweloper możesz często wykonywać wiele nieblokujących wywołań do platformy Azure w skrypcie lub tworzyć zasoby platformy Azure w rozwiązaniu REPL bez blokowania bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="69bb9-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="69bb9-107">Aby zaspokoić te potrzeby, program Azure PowerShell oferuje najwyższej jakości obsługę zadań [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="69bb9-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="69bb9-108">Stan trwały kontekstu i zadania PSJob</span><span class="sxs-lookup"><span data-stu-id="69bb9-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="69bb9-109">Zadania PSJob są uruchamiane w ramach osobnych procesów, co oznacza, że informacje o połączeniu z platformą Azure muszą zostać prawidłowo udostępnione tworzonym zadaniom.</span><span class="sxs-lookup"><span data-stu-id="69bb9-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="69bb9-110">Po połączeniu konta platformy Azure z sesją programu PowerShell przy użyciu polecenia `Connect-AzureRmAccount` można przekazać kontekst do zadania.</span><span class="sxs-lookup"><span data-stu-id="69bb9-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```powershell
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="69bb9-111">Jeśli jednak kontekst ma być zapisywany automatycznie przy użyciu polecenia `Enable-AzureRmContextAutosave`, będzie on automatycznie udostępniany wszystkim tworzonym zadaniom.</span><span class="sxs-lookup"><span data-stu-id="69bb9-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```powershell
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="69bb9-112">Zadania automatyczne z parametrem `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="69bb9-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="69bb9-113">Dla wygody w przypadku niektórych długotrwałych poleceń cmdlet program Azure PowerShell oferuje również przełącznik `-AsJob`.</span><span class="sxs-lookup"><span data-stu-id="69bb9-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="69bb9-114">Przełącznik `-AsJob` sprawia, że tworzenie zadań PSJob jest jeszcze łatwiejsze.</span><span class="sxs-lookup"><span data-stu-id="69bb9-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```powershell
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="69bb9-115">W dowolnym momencie można przeprowadzić inspekcję zadania i postępu przy użyciu poleceń `Get-Job` i `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="69bb9-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

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

<span data-ttu-id="69bb9-116">Następnie po ukończeniu można uzyskać wynik zadania przy użyciu polecenia `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="69bb9-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="69bb9-117">Polecenie `Receive-Job` zwraca wynik z polecenia cmdlet tak, jakby flaga `-AsJob` nie istniała.</span><span class="sxs-lookup"><span data-stu-id="69bb9-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="69bb9-118">Na przykład wynik polecenia `Receive-Job` dla polecenia `Do-Action -AsJob` jest taki sam jak wynik polecenia `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="69bb9-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="69bb9-119">Przykładowe scenariusze</span><span class="sxs-lookup"><span data-stu-id="69bb9-119">Example Scenarios</span></span>

<span data-ttu-id="69bb9-120">Utwórz równocześnie wiele maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="69bb9-120">Create multiple VMs at once.</span></span>

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

<span data-ttu-id="69bb9-121">W tym przykładzie polecenie cmdlet `Wait-Job` powoduje wstrzymanie skryptu w czasie działania zadań.</span><span class="sxs-lookup"><span data-stu-id="69bb9-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="69bb9-122">Wykonywanie skryptu jest kontynuowane po ukończeniu wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="69bb9-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="69bb9-123">Dzięki temu możesz utworzyć kilka zadań uruchamianych równolegle, a następnie zaczekać na ukończenie przed kontynuowaniem.</span><span class="sxs-lookup"><span data-stu-id="69bb9-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

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
