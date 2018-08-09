---
title: Wykonywanie zapytań względem danych wyjściowych poleceń cmdlet programu Azure PowerShell
description: Jak wykonać zapytanie dotyczące zasobów platformy Azure i sformatować wyniki.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: daa39ada5b4e969264b6e8596dc7b090bb196fd5
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653631"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="a59b5-103">Wykonywanie zapytań względem danych wyjściowych poleceń cmdlet programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a59b5-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="a59b5-104">W programie PowerShell można wykonywać zapytania przy użyciu wbudowanych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a59b5-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="a59b5-105">W programie PowerShell nazwy poleceń cmdlet mają postać **_czasownik-rzeczownik_**.</span><span class="sxs-lookup"><span data-stu-id="a59b5-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="a59b5-106">Polecenia cmdlet z czasownikiem **_Get_** służą do tworzenia zapytań.</span><span class="sxs-lookup"><span data-stu-id="a59b5-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="a59b5-107">Rzeczowniki w poleceniach cmdlet to typy zasobów platformy Azure, na których działają czasowniki.</span><span class="sxs-lookup"><span data-stu-id="a59b5-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="a59b5-108">Wybieranie prostych właściwości</span><span class="sxs-lookup"><span data-stu-id="a59b5-108">Select simple properties</span></span>

<span data-ttu-id="a59b5-109">Każde polecenie cmdlet programu Azure PowerShell ma zdefiniowane formatowanie domyślne.</span><span class="sxs-lookup"><span data-stu-id="a59b5-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="a59b5-110">Najbardziej typowe właściwości każdego typu zasobu są automatycznie wyświetlane w formacie tabeli lub listy.</span><span class="sxs-lookup"><span data-stu-id="a59b5-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="a59b5-111">Aby uzyskać więcej informacji na temat formatowania danych wyjściowych, zobacz [Formatowanie wyników zapytania](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="a59b5-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="a59b5-112">Przy użyciu polecenia cmdlet `Get-AzureRmVM` wykonaj zapytanie dotyczące listy maszyn wirtualnych na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="a59b5-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="a59b5-113">Domyślny format danych wyjściowych to tabela.</span><span class="sxs-lookup"><span data-stu-id="a59b5-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="a59b5-114">Za pomocą polecenia cmdlet `Select-Object` można wybrać poszczególne, interesujące właściwości.</span><span class="sxs-lookup"><span data-stu-id="a59b5-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="a59b5-115">Wybieranie złożonych zagnieżdżonych właściwości</span><span class="sxs-lookup"><span data-stu-id="a59b5-115">Select complex nested properties</span></span>

<span data-ttu-id="a59b5-116">Jeśli właściwość, którą chcesz wybrać, jest zagnieżdżona głęboko w danych wyjściowych JSON, musisz podać pełną ścieżkę do niej.</span><span class="sxs-lookup"><span data-stu-id="a59b5-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="a59b5-117">W poniższym przykładzie pokazano, jak wybrać nazwę maszyny wirtualnej i typ systemu operacyjnego z polecenia cmdlet `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="a59b5-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="a59b5-118">Filtrowanie wyników za pomocą polecenia cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="a59b5-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="a59b5-119">Polecenie cmdlet `Where-Object` pozwala filtrować wyniki na podstawie dowolnej wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="a59b5-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="a59b5-120">Poniższy filtr wybiera tylko te maszyny wirtualne, których nazwy zawierają tekst „RGD”.</span><span class="sxs-lookup"><span data-stu-id="a59b5-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="a59b5-121">W następnym przykładzie wyniki będą zawierać maszyny wirtualne, których właściwość vmSize ma wartość „Standard_DS1_V2”.</span><span class="sxs-lookup"><span data-stu-id="a59b5-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```