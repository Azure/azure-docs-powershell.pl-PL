---
title: Wykonywanie zapytań dotyczących zasobów platformy Azure i formatowanie wyników | Microsoft Docs
description: Jak wykonać zapytanie dotyczące zasobów platformy Azure i sformatować wyniki.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1584c8166078b7d7d24ce8748307fde0f565b662
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853478"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="45eaf-103">Wykonywanie zapytań dotyczących zasobów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="45eaf-103">Querying for Azure resources</span></span>

<span data-ttu-id="45eaf-104">W programie PowerShell można wykonywać zapytania przy użyciu wbudowanych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45eaf-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="45eaf-105">W programie PowerShell nazwy poleceń cmdlet mają postać **_czasownik-rzeczownik_**.</span><span class="sxs-lookup"><span data-stu-id="45eaf-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="45eaf-106">Polecenia cmdlet z czasownikiem **_Get_** służą do tworzenia zapytań.</span><span class="sxs-lookup"><span data-stu-id="45eaf-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="45eaf-107">Rzeczowniki w poleceniach cmdlet to typy zasobów platformy Azure, na których działają czasowniki.</span><span class="sxs-lookup"><span data-stu-id="45eaf-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <a name="selecting-simple-properties"></a><span data-ttu-id="45eaf-108">Wybieranie prostych właściwości</span><span class="sxs-lookup"><span data-stu-id="45eaf-108">Selecting simple properties</span></span>

<span data-ttu-id="45eaf-109">Każde polecenie cmdlet programu Azure PowerShell ma zdefiniowane formatowanie domyślne.</span><span class="sxs-lookup"><span data-stu-id="45eaf-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="45eaf-110">Najbardziej typowe właściwości każdego typu zasobu są automatycznie wyświetlane w formacie tabeli lub listy.</span><span class="sxs-lookup"><span data-stu-id="45eaf-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="45eaf-111">Aby uzyskać więcej informacji na temat formatowania danych wyjściowych, zobacz [Formatowanie wyników zapytania](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="45eaf-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="45eaf-112">Przy użyciu polecenia cmdlet `Get-AzureRmVM` wykonaj zapytanie dotyczące listy maszyn wirtualnych na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="45eaf-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="45eaf-113">Domyślny format danych wyjściowych to tabela.</span><span class="sxs-lookup"><span data-stu-id="45eaf-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="45eaf-114">Za pomocą polecenia cmdlet `Select-Object` można wybrać poszczególne, interesujące właściwości.</span><span class="sxs-lookup"><span data-stu-id="45eaf-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="45eaf-115">Wybieranie złożonych zagnieżdżonych właściwości</span><span class="sxs-lookup"><span data-stu-id="45eaf-115">Selecting complex nested properties</span></span>

<span data-ttu-id="45eaf-116">Jeśli właściwość, którą chcesz wybrać, jest zagnieżdżona głęboko w danych wyjściowych JSON, musisz podać pełną ścieżkę do niej.</span><span class="sxs-lookup"><span data-stu-id="45eaf-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="45eaf-117">W poniższym przykładzie pokazano, jak wybrać nazwę maszyny wirtualnej i typ systemu operacyjnego z polecenia cmdlet `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="45eaf-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="45eaf-118">Filtrowanie wyników za pomocą polecenia cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="45eaf-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="45eaf-119">Polecenie cmdlet `Where-Object` pozwala filtrować wyniki na podstawie dowolnej wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="45eaf-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="45eaf-120">Poniższy filtr wybiera tylko te maszyny wirtualne, których nazwy zawierają tekst „RGD”.</span><span class="sxs-lookup"><span data-stu-id="45eaf-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="45eaf-121">W następnym przykładzie wyniki będą zawierać maszyny wirtualne, których właściwość vmSize ma wartość „Standard_DS1_V2”.</span><span class="sxs-lookup"><span data-stu-id="45eaf-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
