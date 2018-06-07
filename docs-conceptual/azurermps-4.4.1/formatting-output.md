---
title: Formatowanie wyników zapytania | Microsoft Docs
description: Jak wykonać zapytanie dotyczące zasobów platformy Azure i sformatować wyniki.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 481beac237d1a6e4b9cf50e541f6abcad8e3ae1a
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820259"
---
# <a name="formatting-query-results"></a><span data-ttu-id="93d37-103">Formatowanie wyników zapytania</span><span class="sxs-lookup"><span data-stu-id="93d37-103">Formatting query results</span></span>

<span data-ttu-id="93d37-104">Domyślnie dane wyjściowe każdego polecenia cmdlet programu PowerShell są wstępnie sformatowane, co ułatwia ich odczytywanie.</span><span class="sxs-lookup"><span data-stu-id="93d37-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="93d37-105">Ponadto program PowerShell udostępnia następujące polecenia cmdlet, które pozwalają elastycznie dopasować dane wyjściowe lub przekształcić je do innego formatu:</span><span class="sxs-lookup"><span data-stu-id="93d37-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="93d37-106">Formatowanie</span><span class="sxs-lookup"><span data-stu-id="93d37-106">Formatting</span></span>      | <span data-ttu-id="93d37-107">Konwersja</span><span class="sxs-lookup"><span data-stu-id="93d37-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="93d37-108">Przykłady formatowania</span><span class="sxs-lookup"><span data-stu-id="93d37-108">Formatting examples</span></span>

<span data-ttu-id="93d37-109">W tym przykładzie zostanie pobrana lista maszyn wirtualnych platformy Azure w domyślnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="93d37-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="93d37-110">Domyślnie dane wyjściowe polecenia Get-AzureRmVM mają format tabeli.</span><span class="sxs-lookup"><span data-stu-id="93d37-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="93d37-111">Jeśli chcesz ograniczyć zwracane kolumny, możesz użyć polecenia cmdlet `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="93d37-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="93d37-112">W kolejnym przykładzie zostanie pobrana ta sama lista maszyn wirtualnych, ale dane wyjściowe zostaną ograniczone tylko do nazwy i lokalizacji maszyny wirtualnej oraz grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93d37-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="93d37-113">Parametr `-Autosize` umożliwia zmienianie rozmiaru kolumn na podstawie rozmiaru danych.</span><span class="sxs-lookup"><span data-stu-id="93d37-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="93d37-114">Jeśli chcesz, możesz jednak wyświetlić informacje w formacie listy.</span><span class="sxs-lookup"><span data-stu-id="93d37-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="93d37-115">Pokazano to w poniższym przykładzie, korzystającym z polecenia cmdlet `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="93d37-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a><span data-ttu-id="93d37-116">Konwersja na inne typy danych</span><span class="sxs-lookup"><span data-stu-id="93d37-116">Converting to other data types</span></span>

<span data-ttu-id="93d37-117">Program PowerShell udostępnia też wiele formatów danych wyjściowych, które spełniają różne potrzeby.</span><span class="sxs-lookup"><span data-stu-id="93d37-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="93d37-118">W poniższym przykładzie polecenie cmdlet `Select-Object` zostanie użyte do pobrania atrybutów maszyn wirtualnych w subskrypcji i przekształcenia danych wyjściowych na format CSV w celu ich łatwego zaimportowania do bazy danych lub arkusza kalkulacyjnego.</span><span class="sxs-lookup"><span data-stu-id="93d37-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="93d37-119">Dane wyjściowe można także przekształcić na format JSON.</span><span class="sxs-lookup"><span data-stu-id="93d37-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="93d37-120">W poniższym przykładzie zostanie utworzona ta sama lista maszyn wirtualnych, ale format danych wyjściowych zostanie zmieniony na JSON.</span><span class="sxs-lookup"><span data-stu-id="93d37-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
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
