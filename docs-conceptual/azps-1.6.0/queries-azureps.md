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
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475464"
---
# <a name="query-output-of-azure-powershell"></a>Wykonywanie zapytań dotyczących danych wyjściowych programu Azure PowerShell 

Wyniki każdego polecenia cmdlet programu Azure PowerShell są obiektem programu Azure PowerShell. Nawet polecenia cmdlet, które nie są jawnie operacjami `Get-`, mogą zwracać wartość, którą można zbadać, aby uzyskać informacje o utworzonym lub zmodyfikowanym zasobie. Większość poleceń cmdlet zwraca jeden obiekt, ale niektóre zwracają tablicę, na której należy wykonać iterację.

Prawie we wszystkich przypadkach dane wyjściowe z programu Azure PowerShell bada się za pomocą polecenia cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), które często skraca się do postaci `select`. Dane wyjściowe można filtrować za pomocą polecenia [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) lub jego aliasu `where`.

## <a name="select-simple-properties"></a>Wybieranie prostych właściwości

W domyślnym formacie tabeli polecenia cmdlet programu Azure PowerShell nie wyświetlają wszystkich dostępnych właściwości. Pełne właściwości można uzyskać za pomocą polecenia cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list) lub potokowego przekazania wartości wyjściowych do polecenia `Select-Object *`:

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

Jeśli znasz nazwy odpowiednich właściwości, możesz ich użyć z poleceniem `Select-Object`, aby pobrać je bezpośrednio:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

Dane wyjściowe polecenia `Select-Object` zawsze są formatowane w celu wyświetlenia żądanych informacji. Aby uzyskać informacje o używaniu formatowania w zapytaniach dotyczących wyników poleceń cmdlet, zobacz [Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell](formatting-output.md).

## <a name="select-nested-properties"></a>Wybieranie właściwości zagnieżdżonych

Niektóre właściwości w danych wyjściowych poleceń cmdlet programu Azure PowerShell używają obiektów zagnieżdżonych, takich jak właściwość `StorageProfile` danych wyjściowych polecenia `Get-AzVM`. Aby uzyskać wartość z właściwości zagnieżdżonej, podaj nazwę wyświetlaną i pełną ścieżkę do badanej wartości jako część argumentu słownika dla polecenia `Select-Object`:

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

Każdy argument słownika wybiera jedną właściwość z obiektu. Właściwość do wyodrębnienia musi być częścią wyrażenia.

## <a name="filter-results"></a>Filtrowanie wyników 

Polecenie cmdlet `Where-Object` pozwala filtrować wyniki na podstawie dowolnej wartości właściwości, w tym właściwości zagnieżdżonych. W następnym przykładzie pokazano używanie polecenia `Where-Object` do znajdowania maszyn wirtualnych z systemem Linux w grupie zasobów.

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

Można potokowo przekazywać wyniki poleceń `Select-Object` i `Where-Object` między tymi poleceniami. Ze względu na wydajność zawsze zaleca się umieszczanie operacji `Where-Object` przed operacją `Select-Object`:

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