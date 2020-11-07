---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705355"
---
# Get-AzVMGuestPolicyStatusHistory

## STRESZCZENIe
Pobiera historię stanu zgodności zasad konfiguracji gościa dla inicjatywy typu "Gość konfiguracja" przypisaną do maszyny wirtualnej.
Inicjatywa to zasada typu definicji "Inicjatywa".

## POLECENIA

### InitiativeNameScope (domyślny)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzVMGuestPolicyStatusHistory pobiera historię stanu zgodności zasad konfiguracji Gości z inicjatywy typu "Gość konfiguracja" przypisaną do maszyny wirtualnej.
Inicjatywa to zasada typu definicji "Inicjatywa".
Użyj polecenia cmdlet Get-AzVMGuestPolicyStatus, aby uzyskać szczegółowe informacje o pojedynczym stanie zgodności przy użyciu ReportId, który można znaleźć w wynikach Get-AzVMGuestPolicyStatusHistory polecenia cmdlet.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Pobiera historię stanu zgodności według identyfikatora inicjatywy. ShowOnlyChange Switch wyświetla tylko zmiany stanu historycznego.
Pomija Stany, które nie zmieniły się między dwoma sprawdzeniami zgodności.

### Przykład 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Pobiera historię stanu zgodności według nazwy inicjatywy.
W przełączniku ShowOnlyChange są wyświetlane tylko zmiany stanu historycznego.
Pomija Stany, które nie zmieniły się między dwoma sprawdzeniami zgodności.

### Przykład 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Pobiera historię stanu zgodności dla wszystkich zasad konfiguracji gościa przypisanych do maszyny wirtualnej.
W przełączniku ShowOnlyChange są wyświetlane tylko zmiany stanu historycznego.
Pomija Stany, które nie zmieniły się między dwoma sprawdzeniami zgodności.

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

Stan zasad konfiguracji gościa jest wyświetlany według ReportId.
ReportId jest właściwością ReportId, którą można znaleźć w wynikach funkcji Get-AzVMGuestPolicyStatusHistory. (Zobacz inne przykłady)

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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
Identyfikator definicji zasady, w której typ definicji to inicjatywa, a kategoria to konfiguracja gościa

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

### -Initiativename
Nazwa zasady, w której typ definicji to inicjatywa, a kategoria to konfiguracja gościa

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
Umożliwia wyświetlanie zmian stanu historycznego tylko dla zasad konfiguracji gościa.
Pomija Stany, które nie zmieniły się między dwoma uruchomieniami inspekcji stanu zgodności.

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

### -VMName
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
## WYSYŁA

### Microsoft. Azure. Commands. GuestConfiguration. models. PolicyStatus
## INFORMACYJN

## LINKI POKREWNE
