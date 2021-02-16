---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187659"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
Pobiera stan zasad konfiguracji gościa (szczegółowy) dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.
Inicjatywy to zasady typu definicji "Inicjatywy".

## SKŁADNIA

### Żytoskop (domyślny)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie Get-AzVMGuestPolicyStatus pobiera stan zasad konfiguracji gościa dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.
Inicjatywy to zasady typu definicji "Inicjatywy".
To polecenie cmdlet otrzymuje stan zgodności maszyny wirtualnej i przyczyny, dla których jest ono niezgodne z poszczególnymi zasadami w ramach inicjatywy.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Uzyskaj wszystkie najnowsze statusy zasad konfiguracji gościa dla maszyny wirtualnej.
Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady we wszystkich inicjatywach typu "Konfiguracja gościa", powody zgodności, czas kontroli zgodności, informacje o zasobach sprawdzone pod kątem zgodności.
Wyniki zawierają najnowsze stany, ale nie zawierają poprzednich stanów historycznych.

### Przykład 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Uzyskaj najnowsze statusy zasad konfiguracji gościa, korzystając z identyfikatora inicjatywy. Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady w ramach inicjatywy, powody zgodności, czas sprawdzania zgodności, informacje o zasobach sprawdzone pod kątem zgodności.
Wyniki nie zawierają wygenerowanych poprzednich stanów, a jedynie najnowszy stan dla każdej zasady w ramach inicjatywy.

### Przykład 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Uzyskaj najnowsze statusy zasad konfiguracji gościa według nazwy inicjatywy.
Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady w ramach inicjatywy, powody zgodności, czas sprawdzania zgodności, informacje o zasobach sprawdzone pod kątem zgodności.
Wyniki nie zawierają wygenerowanych poprzednich stanów, a jedynie najnowszy stan dla każdej zasady w ramach inicjatywy.

### Przykład 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Uzyskaj stan zasad konfiguracji gościa według raportu ReportId.
ReportId to właściwość ReportId, która może zostać znaleziona w wynikach Get-AzVMGuestPolicyStatus initiativeId lub Initiative Name (zobacz inne przykłady)

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

Required: True
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

### - ReportId
Identyfikator stanu zasad konfiguracji gościa.
Zasady, w których typem definicji jest inicjatywa, a kategorią jest konfiguracja gościa, należy przypisać do zakresu, aby uzyskać statusy.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Nazwa maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
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

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## NOTATKI

## LINKI POKREWNE
