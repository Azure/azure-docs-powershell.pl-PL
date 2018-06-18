---
title: Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell
description: Jak formatować dane wyjściowe polecenia cmdlet programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/07/2018
ms.openlocfilehash: 833c82903305f99be5ad43f707e22644bb568abe
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323394"
---
# <a name="format-azurepowershell-cmdlet-output"></a>Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell

Domyślnie dane wyjściowe każdego polecenia cmdlet programu Azure PowerShell są wstępnie sformatowane, co ułatwia ich odczytywanie.  Ponadto program PowerShell udostępnia następujące polecenia cmdlet, które pozwalają elastycznie dopasować dane wyjściowe lub przekształcić je do innego formatu:

| Formatowanie      | Konwersja       |
|-----------------|------------------|
| [Format-Custom](/powershell/module/microsoft.powershell.utility/format-custom) | [ConvertTo-Csv](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [Format-List](/powershell/module/microsoft.powershell.utility/format-list)   | [ConvertTo-Html](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [Format-Table](/powershell/module/microsoft.powershell.utility/format-table)  | [ConvertTo-Json](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [Format-Wide](/powershell/module/microsoft.powershell.utility/format-wide)   | [ConvertTo-Xml](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a>Przykłady formatowania

W tym przykładzie zostanie pobrana lista maszyn wirtualnych platformy Azure w domyślnej subskrypcji.  Domyślnie dane wyjściowe polecenia `Get-AzureRmVM` mają format tabeli.

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Jeśli chcesz ograniczyć zwracane kolumny, możesz użyć polecenia cmdlet `Format-Table`. W kolejnym przykładzie zostanie pobrana ta sama lista maszyn wirtualnych, ale dane wyjściowe zostaną ograniczone tylko do nazwy i lokalizacji maszyny wirtualnej oraz grupy zasobów.  Parametr `-Autosize` umożliwia zmienianie rozmiaru kolumn na podstawie rozmiaru danych.

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

Dane wyjściowe mogą również zostać sformatowane jako lista. Pokazano to w poniższym przykładzie, korzystającym z polecenia cmdlet `Format-List`.

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

## <a name="convert-to-other-data-types"></a>Konwersja na inne typy danych

Program PowerShell umożliwia również konwertowanie danych wyjściowych poleceń na wiele formatów danych. W poniższym przykładzie polecenie cmdlet `Select-Object` zostało użyte do pobrania atrybutów maszyn wirtualnych w subskrypcji i przekonwertowania danych wyjściowych na format CSV w celu ich łatwego zaimportowania do bazy danych lub arkusza kalkulacyjnego.

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

Dane wyjściowe można również przekonwertować na format JSON.  W poniższym przykładzie zostanie utworzona ta sama lista maszyn wirtualnych, ale format danych wyjściowych zostanie zmieniony na JSON.

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
