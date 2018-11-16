---
title: Wykonywanie zapytań dotyczących zasobów platformy Azure i formatowanie wyników | Microsoft Docs
description: Jak wykonać zapytanie dotyczące zasobów platformy Azure i sformatować wyniki.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9a7627a25f9bbd196b1d615229e45a6e1ce7a7d9
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574876"
---
# <a name="querying-for-azure-resources"></a>Wykonywanie zapytań dotyczących zasobów platformy Azure

W programie PowerShell można wykonywać zapytania przy użyciu wbudowanych poleceń cmdlet. W programie PowerShell nazwy poleceń cmdlet mają postać **_czasownik-rzeczownik_**. Polecenia cmdlet z czasownikiem **_Get_** służą do tworzenia zapytań. Rzeczowniki w poleceniach cmdlet to typy zasobów platformy Azure, na których działają czasowniki.

## <a name="selecting-simple-properties"></a>Wybieranie prostych właściwości

Każde polecenie cmdlet programu Azure PowerShell ma zdefiniowane formatowanie domyślne. Najbardziej typowe właściwości każdego typu zasobu są automatycznie wyświetlane w formacie tabeli lub listy. Aby uzyskać więcej informacji na temat formatowania danych wyjściowych, zobacz [Formatowanie wyników zapytania](formatting-output.md).

Przy użyciu polecenia cmdlet `Get-AzureRmVM` wykonaj zapytanie dotyczące listy maszyn wirtualnych na Twoim koncie.

```powershell-interactive
Get-AzureRmVM
```

Domyślny format danych wyjściowych to tabela.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Za pomocą polecenia cmdlet `Select-Object` można wybrać poszczególne, interesujące właściwości.

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Wybieranie złożonych zagnieżdżonych właściwości

Jeśli właściwość, którą chcesz wybrać, jest zagnieżdżona głęboko w danych wyjściowych JSON, musisz podać pełną ścieżkę do niej. W poniższym przykładzie pokazano, jak wybrać nazwę maszyny wirtualnej i typ systemu operacyjnego z polecenia cmdlet `Get-AzureRmVM`.

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Filtrowanie wyników za pomocą polecenia cmdlet Where-Object

Polecenie cmdlet `Where-Object` pozwala filtrować wyniki na podstawie dowolnej wartości właściwości. Poniższy filtr wybiera tylko te maszyny wirtualne, których nazwy zawierają tekst „RGD”.

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

W następnym przykładzie wyniki będą zawierać maszyny wirtualne, których właściwość vmSize ma wartość „Standard_DS1_V2”.

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
