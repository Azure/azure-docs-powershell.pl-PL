---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237789"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
Pobiera historię stanu zgodności zasad konfiguracji gościa dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.
Inicjatywy to zasady typu definicji "Inicjatywy".

## SKŁADNIA

### InitiativeNameScope (Domyślna)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie Get-AzVMGuestPolicyStatusHistory cmdlet pobiera historię stanu zgodności zasad konfiguracji gościa dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.
Inicjatywy to zasady typu definicji "Inicjatywy".
Użyj Get-AzVMGuestPolicyStatus cmdlet, aby uzyskać szczegółowe informacje o pojedynczym stanie zgodności przy użyciu funkcji ReportId, które można znaleźć w wynikach Get-AzVMGuestPolicyStatusHistory cmdlet.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Pobiera historię stanu zgodności według identyfikatora inicjatywy. Przełącznik ShowOnlyChange pokazuje tylko historyczne zmiany stanu.
Pomija stany, które nie zmieniły się między dwoma testami zgodności.

### Przykład 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Pobiera historię stanu zgodności według nazwy inicjatywy.
Przełącznik ShowOnlyChange pokazuje tylko zmiany stanu historycznego.
Pomija stany, które nie zmieniły się między dwoma testami zgodności.

### Przykład 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Pobiera historię stanu zgodności dla wszystkich zasad konfiguracji gościa przypisanych do maszyny wirtualnej.
Przełącznik ShowOnlyChange pokazuje tylko zmiany stanu historycznego.
Pomija stany, które nie zmieniły się między dwoma testami zgodności.

### Przykład 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Pobiera historię stanu zgodności według identyfikatora inicjatywy.

### Przykład 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Pobiera historię stanu zgodności według nazwy inicjatywy.

### Przykład 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Pobiera historię stanu zgodności dla wszystkich zasad konfiguracji gościa przypisanych do maszyny wirtualnej.

### Przykład 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Uzyskaj stan zasad konfiguracji gościa według raportu ReportId.
ReportId to właściwość ReportId, która znajduje się w wynikach właściwości Get-AzVMGuestPolicyStatusHistory. (zapoznaj się z innymi przykładami)

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeId
Identyfikator definicji zasad, w których typem definicji jest Initiative, a kategorią jest konfiguracja gościa

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
Nazwa zasad, w których typem definicji jest Initiative, a kategorią jest Konfiguracja gościa

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
Pokazuje historyczne zmiany stanu tylko w przypadku zasad konfiguracji gościa.
Pomija stany, które nie zmieniły się między dwoma inspekcjami stanu zgodności.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Nazwa maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak
## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus
## NOTATKI

## LINKI POKREWNE
