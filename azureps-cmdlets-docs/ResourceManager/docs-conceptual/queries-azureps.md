---
title: "<span data-ttu-id=\"a587f-101\">Wykonywanie zapytań dotyczących zasobów platformy Azure i formatowanie wyników | Microsoft Docs</span><span class=\"sxs-lookup\"><span data-stu-id=\"a587f-101\">Querying for Azure resources and formatting results | Microsoft Docs</span></span>"
description: "<span data-ttu-id=\"a587f-102\">Jak wykonać zapytanie dotyczące zasobów platformy Azure i sformatować wyniki.</span><span class=\"sxs-lookup\"><span data-stu-id=\"a587f-102\">How to query for resources in Azure and format the results.</span></span>"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 369ecdca1ab0453847041de88d0765f1ae61ca9d
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="a587f-103">Wykonywanie zapytań dotyczących zasobów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a587f-103">Querying for Azure resources</span></span>
<a id="querying-for-azure-resources" class="xliff"></a>

<span data-ttu-id="a587f-104">W programie PowerShell można wykonywać zapytania przy użyciu wbudowanych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a587f-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="a587f-105">W programie PowerShell nazwy poleceń cmdlet mają postać **_czasownik-rzeczownik_**.</span><span class="sxs-lookup"><span data-stu-id="a587f-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="a587f-106">Polecenia cmdlet z czasownikiem **_Get_** służą do tworzenia zapytań.</span><span class="sxs-lookup"><span data-stu-id="a587f-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="a587f-107">Rzeczowniki w poleceniach cmdlet to typy zasobów platformy Azure, na których działają czasowniki.</span><span class="sxs-lookup"><span data-stu-id="a587f-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <span data-ttu-id="a587f-108">Wybieranie prostych właściwości</span><span class="sxs-lookup"><span data-stu-id="a587f-108">Selecting simple properties</span></span>
<a id="selecting-simple-properties" class="xliff"></a>

<span data-ttu-id="a587f-109">Każde polecenie cmdlet programu Azure PowerShell ma zdefiniowane formatowanie domyślne.</span><span class="sxs-lookup"><span data-stu-id="a587f-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="a587f-110">Najbardziej typowe właściwości każdego typu zasobu są automatycznie wyświetlane w formacie tabeli lub listy.</span><span class="sxs-lookup"><span data-stu-id="a587f-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="a587f-111">Aby uzyskać więcej informacji na temat formatowania danych wyjściowych, zobacz [Formatowanie wyników zapytania](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="a587f-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="a587f-112">Przy użyciu polecenia cmdlet `Get-AzureRmVM` wykonaj zapytanie dotyczące listy maszyn wirtualnych na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="a587f-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="a587f-113">Domyślny format danych wyjściowych to tabela.</span><span class="sxs-lookup"><span data-stu-id="a587f-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="a587f-114">Za pomocą polecenia cmdlet `Select-Object` można wybrać poszczególne, interesujące właściwości.</span><span class="sxs-lookup"><span data-stu-id="a587f-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select-Object Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <span data-ttu-id="a587f-115">Wybieranie złożonych zagnieżdżonych właściwości</span><span class="sxs-lookup"><span data-stu-id="a587f-115">Selecting complex nested properties</span></span>
<a id="selecting-complex-nested-properties" class="xliff"></a>

<span data-ttu-id="a587f-116">Jeśli właściwość, którą chcesz wybrać, jest zagnieżdżona głęboko w danych wyjściowych JSON, musisz podać pełną ścieżkę do niej.</span><span class="sxs-lookup"><span data-stu-id="a587f-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="a587f-117">W poniższym przykładzie pokazano, jak wybrać nazwę maszyny wirtualnej i typ systemu operacyjnego z polecenia cmdlet `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="a587f-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select-Object name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <span data-ttu-id="a587f-118">Filtrowanie wyników za pomocą polecenia cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="a587f-118">Filter result using the Where-Object cmdlet</span></span>
<a id="filter-result-using-the-where-object-cmdlet" class="xliff"></a>

<span data-ttu-id="a587f-119">Polecenie cmdlet `Where-Object` pozwala filtrować wyniki na podstawie dowolnej wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="a587f-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="a587f-120">Poniższy filtr wybiera tylko te maszyny wirtualne, których nazwy zawierają tekst „RGD”.</span><span class="sxs-lookup"><span data-stu-id="a587f-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where-Object ResourceGroupName -like "RGD*" | Select-Object ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="a587f-121">W następnym przykładzie wyniki będą zawierać maszyny wirtualne, których właściwość vmSize ma wartość „Standard_DS1_V2”.</span><span class="sxs-lookup"><span data-stu-id="a587f-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where-Object vmSize -eq 'Standard_DS1_V2'
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```