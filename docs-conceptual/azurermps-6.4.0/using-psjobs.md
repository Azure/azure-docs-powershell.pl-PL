---
title: Równoczesne uruchamianie poleceń cmdlet przy użyciu zadań programu PowerShell
description: Sposób równoległego uruchamiania poleceń cmdlet za pomocą parametru -AsJob.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: a986824d952ccf6cd52dc86418899f3805a38973
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406526"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="b201f-103">Równoczesne uruchamianie poleceń cmdlet przy użyciu zadań programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="b201f-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="b201f-104">Program PowerShell obsługuje akcję asynchroniczną przy użyciu [zadań programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="b201f-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="b201f-105">Program Azure PowerShell w znacznej mierze zależy od wykonywania wywołań sieci do platformy Azure i oczekiwania na nie.</span><span class="sxs-lookup"><span data-stu-id="b201f-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="b201f-106">Jako deweloper możesz często wykonywać wiele nieblokujących wywołań do platformy Azure w skrypcie lub tworzyć zasoby platformy Azure w rozwiązaniu REPL bez blokowania bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="b201f-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="b201f-107">Aby zaspokoić te potrzeby, program Azure PowerShell oferuje najwyższej jakości obsługę zadań [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="b201f-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="b201f-108">Stan trwały kontekstu i zadania PSJob</span><span class="sxs-lookup"><span data-stu-id="b201f-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="b201f-109">Zadania PSJob są uruchamiane w ramach osobnych procesów, co oznacza, że informacje o połączeniu z platformą Azure muszą zostać prawidłowo udostępnione tworzonym zadaniom.</span><span class="sxs-lookup"><span data-stu-id="b201f-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="b201f-110">Po połączeniu konta platformy Azure z sesją programu PowerShell przy użyciu polecenia `Connect-AzureRmAccount` można przekazać kontekst do zadania.</span><span class="sxs-lookup"><span data-stu-id="b201f-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="b201f-111">Jeśli jednak kontekst ma być zapisywany automatycznie przy użyciu polecenia `Enable-AzureRmContextAutosave`, będzie on automatycznie udostępniany wszystkim tworzonym zadaniom.</span><span class="sxs-lookup"><span data-stu-id="b201f-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="b201f-112">Zadania automatyczne z parametrem `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="b201f-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="b201f-113">Dla wygody w przypadku niektórych długotrwałych poleceń cmdlet program Azure PowerShell oferuje również przełącznik `-AsJob`.</span><span class="sxs-lookup"><span data-stu-id="b201f-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="b201f-114">Przełącznik `-AsJob` sprawia, że tworzenie zadań PSJob jest jeszcze łatwiejsze.</span><span class="sxs-lookup"><span data-stu-id="b201f-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="b201f-115">W dowolnym momencie można przeprowadzić inspekcję zadania i postępu przy użyciu poleceń `Get-Job` i `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="b201f-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="b201f-116">Następnie po ukończeniu można uzyskać wynik zadania przy użyciu polecenia `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="b201f-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="b201f-117">Polecenie `Receive-Job` zwraca wynik z polecenia cmdlet tak, jakby flaga `-AsJob` nie istniała.</span><span class="sxs-lookup"><span data-stu-id="b201f-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="b201f-118">Na przykład wynik polecenia `Receive-Job` dla polecenia `Do-Action -AsJob` jest taki sam jak wynik polecenia `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="b201f-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
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

## <a name="example-scenarios"></a><span data-ttu-id="b201f-119">Przykładowe scenariusze</span><span class="sxs-lookup"><span data-stu-id="b201f-119">Example Scenarios</span></span>

<span data-ttu-id="b201f-120">Utwórz równocześnie wiele maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="b201f-120">Create multiple VMs at once.</span></span>

```azurepowershell-interactive
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

<span data-ttu-id="b201f-121">W tym przykładzie polecenie cmdlet `Wait-Job` powoduje wstrzymanie skryptu w czasie działania zadań.</span><span class="sxs-lookup"><span data-stu-id="b201f-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="b201f-122">Wykonywanie skryptu jest kontynuowane po ukończeniu wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="b201f-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="b201f-123">Dzięki temu możesz utworzyć kilka zadań uruchamianych równolegle, a następnie zaczekać na ukończenie przed kontynuowaniem.</span><span class="sxs-lookup"><span data-stu-id="b201f-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

```output
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
