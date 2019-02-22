---
title: Wykonywanie zapytań względem danych wyjściowych poleceń cmdlet programu Azure PowerShell
description: Jak wykonać zapytanie dotyczące zasobów platformy Azure i sformatować wyniki.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153650"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="7b716-103">Wykonywanie zapytań dotyczących danych wyjściowych programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b716-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="7b716-104">Wyniki każdego polecenia cmdlet programu Azure PowerShell są obiektem programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7b716-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="7b716-105">Nawet polecenia cmdlet, które nie są jawnie operacjami `Get-`, mogą zwracać wartość, którą można zbadać, aby uzyskać informacje o utworzonym lub zmodyfikowanym zasobie.</span><span class="sxs-lookup"><span data-stu-id="7b716-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="7b716-106">Większość poleceń cmdlet zwraca jeden obiekt, ale niektóre zwracają tablicę, na której należy wykonać iterację.</span><span class="sxs-lookup"><span data-stu-id="7b716-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="7b716-107">Prawie we wszystkich przypadkach dane wyjściowe z programu Azure PowerShell bada się za pomocą polecenia cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), które często skraca się do postaci `select`.</span><span class="sxs-lookup"><span data-stu-id="7b716-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="7b716-108">Dane wyjściowe można filtrować za pomocą polecenia [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) lub jego aliasu `where`.</span><span class="sxs-lookup"><span data-stu-id="7b716-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="7b716-109">Wybieranie prostych właściwości</span><span class="sxs-lookup"><span data-stu-id="7b716-109">Select simple properties</span></span>

<span data-ttu-id="7b716-110">W domyślnym formacie tabeli polecenia cmdlet programu Azure PowerShell nie wyświetlają wszystkich dostępnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="7b716-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="7b716-111">Pełne właściwości można uzyskać za pomocą polecenia cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list) lub potokowego przekazania wartości wyjściowych do polecenia `Select-Object *`:</span><span class="sxs-lookup"><span data-stu-id="7b716-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="7b716-112">Jeśli znasz nazwy odpowiednich właściwości, możesz ich użyć z poleceniem `Select-Object`, aby pobrać je bezpośrednio:</span><span class="sxs-lookup"><span data-stu-id="7b716-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="7b716-113">Dane wyjściowe polecenia `Select-Object` zawsze są formatowane w celu wyświetlenia żądanych informacji.</span><span class="sxs-lookup"><span data-stu-id="7b716-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="7b716-114">Aby uzyskać informacje o używaniu formatowania w zapytaniach dotyczących wyników poleceń cmdlet, zobacz [Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="7b716-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="7b716-115">Wybieranie właściwości zagnieżdżonych</span><span class="sxs-lookup"><span data-stu-id="7b716-115">Select nested properties</span></span>

<span data-ttu-id="7b716-116">Niektóre właściwości w danych wyjściowych poleceń cmdlet programu Azure PowerShell używają obiektów zagnieżdżonych, takich jak właściwość `StorageProfile` danych wyjściowych polecenia `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="7b716-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="7b716-117">Aby uzyskać wartość z właściwości zagnieżdżonej, podaj nazwę wyświetlaną i pełną ścieżkę do badanej wartości jako część argumentu słownika dla polecenia `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="7b716-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="7b716-118">Każdy argument słownika wybiera jedną właściwość z obiektu.</span><span class="sxs-lookup"><span data-stu-id="7b716-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="7b716-119">Właściwość do wyodrębnienia musi być częścią wyrażenia.</span><span class="sxs-lookup"><span data-stu-id="7b716-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="7b716-120">Filtrowanie wyników</span><span class="sxs-lookup"><span data-stu-id="7b716-120">Filter results</span></span> 

<span data-ttu-id="7b716-121">Polecenie cmdlet `Where-Object` pozwala filtrować wyniki na podstawie dowolnej wartości właściwości, w tym właściwości zagnieżdżonych.</span><span class="sxs-lookup"><span data-stu-id="7b716-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="7b716-122">W następnym przykładzie pokazano używanie polecenia `Where-Object` do znajdowania maszyn wirtualnych z systemem Linux w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b716-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="7b716-123">Można potokowo przekazywać wyniki poleceń `Select-Object` i `Where-Object` między tymi poleceniami.</span><span class="sxs-lookup"><span data-stu-id="7b716-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="7b716-124">Ze względu na wydajność zawsze zaleca się umieszczanie operacji `Where-Object` przed operacją `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="7b716-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```