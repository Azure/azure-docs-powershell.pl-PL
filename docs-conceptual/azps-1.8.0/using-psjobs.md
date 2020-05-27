---
title: Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell
description: Dowiedz się, jak uruchamiać polecenia cmdlet środowiska Azure PowerShell równolegle lub jako zadania w tle przy użyciu opcji -AsJob i Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: 36fcfc42fed91c5a0c8eff200c662e1e31cacfb9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387738"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="a8ac6-103">Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8ac6-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="a8ac6-104">Środowisko Azure PowerShell polega na nawiązywaniu połączenia z chmurą platformy Azure i oczekiwaniu na odpowiedzi, dlatego większość tych poleceń cmdlet blokuje sesję programu PowerShell do czasu uzyskania odpowiedzi z chmury.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="a8ac6-105">Zadania programu PowerShell umożliwiają uruchamianie poleceń cmdlet w tle lub jednoczesne wykonywanie wielu zadań na platformie Azure w ramach jednej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="a8ac6-106">Ten artykuł zawiera krótkie omówienie sposobu uruchamiania poleceń cmdlet środowiska Azure PowerShell jako zadań programu PowerShell i sprawdzania, czy zostały one ukończone.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="a8ac6-107">Uruchamianie poleceń w środowisku Azure PowerShell wymaga używania kontekstów środowiska Azure PowerShell, które szczegółowo opisano w sekcji [Poświadczenia logowania i konteksty platformy Azure](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a8ac6-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="a8ac6-108">Aby dowiedzieć się więcej na temat zadań programu PowerShell, zobacz [Informacje o zadaniach programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="a8ac6-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="a8ac6-109">Konteksty platformy Azure z zadaniami programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8ac6-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="a8ac6-110">Zadania programu PowerShell są uruchamiane jako oddzielne procesy bez dołączonej sesji programu PowerShell, dlatego Twoje poświadczenia platformy Azure muszą być im udostępnione.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="a8ac6-111">Poświadczenia są przekazywane jako obiekty kontekstu platformy Azure przy użyciu jednej z tych metod:</span><span class="sxs-lookup"><span data-stu-id="a8ac6-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="a8ac6-112">Automatyczna trwałość kontekstu.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-112">Automatic context persistence.</span></span> <span data-ttu-id="a8ac6-113">Trwałość kontekstu jest domyślnie włączona i zachowuje informacje logowania w wielu sesjach.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="a8ac6-114">Po włączeniu trwałości kontekstu bieżący kontekst platformy Azure jest przenoszony do nowego procesu:</span><span class="sxs-lookup"><span data-stu-id="a8ac6-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="a8ac6-115">Użyj parametru `-AzContext` z dowolnymi poleceniami cmdlet środowiska Azure PowerShell, aby udostępnić obiekt kontekstu platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="a8ac6-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="a8ac6-116">Jeśli trwałość kontekstu jest wyłączona, wymagany jest argument `-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="a8ac6-117">Użyj przełącznika `-AsJob` dostarczanego przez niektóre polecenia cmdlet środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a8ac6-118">Ten przełącznik automatycznie uruchamia polecenie cmdlet jako zadanie programu PowerShell przy użyciu obecnie aktywnego kontekstu platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="a8ac6-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="a8ac6-119">Aby sprawdzić, czy polecenie cmdlet obsługuje przełącznik `-AsJob`, zapoznaj się z jego dokumentacją referencyjną.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="a8ac6-120">Przełącznik `-AsJob` nie wymaga, aby automatyczne zapisywanie kontekstu było włączone.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="a8ac6-121">Stan uruchomionego zadania można sprawdzić przy użyciu polecenia cmdlet [Get-Job](/powershell/module/microsoft.powershell.core/get-job).</span><span class="sxs-lookup"><span data-stu-id="a8ac6-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="a8ac6-122">Aby pobrać dane wyjściowe z zadania do tej pory, użyj polecenia cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).</span><span class="sxs-lookup"><span data-stu-id="a8ac6-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="a8ac6-123">Aby sprawdzić postęp operacji zdalnie na platformie Azure, użyj poleceń cmdlet `Get-` skojarzonych z typem zasobu modyfikowanym przez zadanie:</span><span class="sxs-lookup"><span data-stu-id="a8ac6-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="a8ac6-124">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="a8ac6-124">See Also</span></span>

* [<span data-ttu-id="a8ac6-125">Konteksty środowiska Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8ac6-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="a8ac6-126">Informacje o zadaniach programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8ac6-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="a8ac6-127">Dokumentacja polecenia Get-Job</span><span class="sxs-lookup"><span data-stu-id="a8ac6-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="a8ac6-128">Dokumentacja polecenia Receive-Job</span><span class="sxs-lookup"><span data-stu-id="a8ac6-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
