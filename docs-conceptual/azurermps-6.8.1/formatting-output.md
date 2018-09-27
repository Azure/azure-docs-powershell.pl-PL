---
title: Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell
description: Jak formatować dane wyjściowe polecenia cmdlet programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 99c635e7d94731d360b81c10b7f08086652ca81f
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560341"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="02163-103">Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="02163-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="02163-104">Domyślnie dane wyjściowe każdego polecenia cmdlet programu Azure PowerShell są wstępnie sformatowane, co ułatwia ich odczytywanie.</span><span class="sxs-lookup"><span data-stu-id="02163-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="02163-105">Ponadto program PowerShell udostępnia następujące polecenia cmdlet, które pozwalają elastycznie dopasować dane wyjściowe lub przekształcić je do innego formatu:</span><span class="sxs-lookup"><span data-stu-id="02163-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="02163-106">Formatowanie</span><span class="sxs-lookup"><span data-stu-id="02163-106">Formatting</span></span>      | <span data-ttu-id="02163-107">Konwersja</span><span class="sxs-lookup"><span data-stu-id="02163-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="02163-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="02163-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="02163-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="02163-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="02163-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="02163-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="02163-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="02163-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="02163-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="02163-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="02163-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="02163-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="02163-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="02163-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="02163-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="02163-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="02163-116">Przykłady formatowania</span><span class="sxs-lookup"><span data-stu-id="02163-116">Format examples</span></span>

<span data-ttu-id="02163-117">W tym przykładzie zostanie pobrana lista maszyn wirtualnych platformy Azure w domyślnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02163-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="02163-118">Domyślnie dane wyjściowe polecenia `Get-AzureRmVM` mają format tabeli.</span><span class="sxs-lookup"><span data-stu-id="02163-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="02163-119">Jeśli chcesz ograniczyć zwracane kolumny, możesz użyć polecenia cmdlet `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="02163-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="02163-120">W kolejnym przykładzie zostanie pobrana ta sama lista maszyn wirtualnych, ale dane wyjściowe zostaną ograniczone tylko do nazwy i lokalizacji maszyny wirtualnej oraz grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02163-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="02163-121">Parametr `-Autosize` umożliwia zmienianie rozmiaru kolumn na podstawie rozmiaru danych.</span><span class="sxs-lookup"><span data-stu-id="02163-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="02163-122">Dane wyjściowe mogą również zostać sformatowane jako lista.</span><span class="sxs-lookup"><span data-stu-id="02163-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="02163-123">Pokazano to w poniższym przykładzie, korzystającym z polecenia cmdlet `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="02163-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="02163-124">Konwersja na inne typy danych</span><span class="sxs-lookup"><span data-stu-id="02163-124">Convert to other data types</span></span>

<span data-ttu-id="02163-125">Program PowerShell umożliwia również konwertowanie danych wyjściowych poleceń na wiele formatów danych.</span><span class="sxs-lookup"><span data-stu-id="02163-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="02163-126">W poniższym przykładzie polecenie cmdlet `Select-Object` zostało użyte do pobrania atrybutów maszyn wirtualnych w subskrypcji i przekonwertowania danych wyjściowych na format CSV w celu ich łatwego zaimportowania do bazy danych lub arkusza kalkulacyjnego.</span><span class="sxs-lookup"><span data-stu-id="02163-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="02163-127">Dane wyjściowe można również przekonwertować na format JSON.</span><span class="sxs-lookup"><span data-stu-id="02163-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="02163-128">W poniższym przykładzie zostanie utworzona ta sama lista maszyn wirtualnych, ale format danych wyjściowych zostanie zmieniony na JSON.</span><span class="sxs-lookup"><span data-stu-id="02163-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
