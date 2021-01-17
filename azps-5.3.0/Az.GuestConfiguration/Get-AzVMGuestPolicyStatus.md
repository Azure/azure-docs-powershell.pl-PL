---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489649"
---
# Get-AzVMGuestPolicyStatus

## STRESZCZENIe
Pobiera stan zasad konfiguracji gościa (szczegółowy) z inicjatywy typu "Gość konfiguracja" przypisanej do maszyny wirtualnej.
Inicjatywa to zasada typu definicji "Inicjatywa".

## POLECENIA

### VmScope (domyślny)
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

## Opis
Polecenie cmdlet Get-AzVMGuestPolicyStatus umożliwia pobieranie stanu zasad konfiguracji Gościa z inicjatywy typu "Gość konfiguracja" przypisanej do maszyny wirtualnej.
Inicjatywa to zasada typu definicji "Inicjatywa".
To polecenie cmdlet pobiera stan zgodności maszyny wirtualnej oraz powody, dla których nie jest on zgodny z indywidualnymi zasadami z inicjatywy.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Uzyskaj wszystkie najnowsze Stany zasad konfiguracji Gości dla maszyny wirtualnej.
Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady we wszystkich inicjatywach typu "Konfiguracja gościa", przyczyny zgodności, czas sprawdzania zgodności, informacje o zasobach, które sprawdziły się pod kątem zgodności.
Wyniki zawierają najnowsze Stany, nie obejmuje wcześniejszych stanów historycznych.

### Przykład 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Uzyskaj najnowsze Stany zasad konfiguracji gościa według identyfikatora inicjatywy. Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady z inicjatywy, przyczyn zgodności, czasu sprawdzania zgodności, informacji o zasobie, które sprawdziły się pod kątem zgodności.
Wyniki nie uwzględniają wcześniejszych wygenerowanych Stanów, ale zawiera najnowszy status dla każdej zasady z inicjatywy.

### Przykład 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Uzyskaj najnowsze Stany zasad konfiguracji gościa według nazwy inicjatywy.
Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady z inicjatywy, przyczyn zgodności, czasu sprawdzania zgodności, informacji o zasobie, które sprawdziły się pod kątem zgodności.
Wyniki nie uwzględniają wcześniejszych wygenerowanych Stanów, ale zawiera najnowszy status dla każdej zasady z inicjatywy.

### Przykład 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Stan zasad konfiguracji gościa jest wyświetlany według ReportId.
ReportId jest właściwością ReportId, którą można znaleźć w wynikach Get-AzVMGuestPolicyStatus przy użyciu initiativeId lub nazwy inicjatywy (Proszę znaleźć inne przykłady).

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

Required: True
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

### -ReportId
Identyfikator stanu zasad konfiguracji gościa.
Zasady, w których typ definicji to inicjatywa, a kategoria to konfiguracja gościa, musi być przypisana do zakresu w celu uzyskania statusu.

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

### -VMName
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
## WYSYŁA

### Microsoft. Azure. Commands. GuestConfiguration. models. PolicyStatusDetailed
## INFORMACYJN

## LINKI POKREWNE
