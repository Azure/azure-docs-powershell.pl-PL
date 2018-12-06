---
title: Formatowanie wyników zapytania | Microsoft Docs
description: Jak wykonać zapytanie dotyczące zasobów platformy Azure i sformatować wyniki.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9ae0d661630bf4e080b3bbaa7f357c384ef68cc4
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826565"
---
# <a name="formatting-query-results"></a>Formatowanie wyników zapytania

Domyślnie dane wyjściowe każdego polecenia cmdlet programu PowerShell są wstępnie sformatowane, co ułatwia ich odczytywanie.  Ponadto program PowerShell udostępnia następujące polecenia cmdlet, które pozwalają elastycznie dopasować dane wyjściowe lub przekształcić je do innego formatu:

| Formatowanie      | Konwersja       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a>Przykłady formatowania

W tym przykładzie zostanie pobrana lista maszyn wirtualnych platformy Azure w domyślnej subskrypcji.  Domyślnie dane wyjściowe polecenia Get-AzureRmVM mają format tabeli.

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Jeśli chcesz ograniczyć zwracane kolumny, możesz użyć polecenia cmdlet `Format-Table`. W kolejnym przykładzie zostanie pobrana ta sama lista maszyn wirtualnych, ale dane wyjściowe zostaną ograniczone tylko do nazwy i lokalizacji maszyny wirtualnej oraz grupy zasobów.  Parametr `-Autosize` umożliwia zmienianie rozmiaru kolumn na podstawie rozmiaru danych.

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

Jeśli chcesz, możesz jednak wyświetlić informacje w formacie listy. Pokazano to w poniższym przykładzie, korzystającym z polecenia cmdlet `Format-List`.

```powershell-interactive
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

## <a name="converting-to-other-data-types"></a>Konwersja na inne typy danych

Program PowerShell udostępnia też wiele formatów danych wyjściowych, które spełniają różne potrzeby.  W poniższym przykładzie polecenie cmdlet `Select-Object` zostanie użyte do pobrania atrybutów maszyn wirtualnych w subskrypcji i przekształcenia danych wyjściowych na format CSV w celu ich łatwego zaimportowania do bazy danych lub arkusza kalkulacyjnego.

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

Dane wyjściowe można także przekształcić na format JSON.  W poniższym przykładzie zostanie utworzona ta sama lista maszyn wirtualnych, ale format danych wyjściowych zostanie zmieniony na JSON.

```powershell-interactive
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
