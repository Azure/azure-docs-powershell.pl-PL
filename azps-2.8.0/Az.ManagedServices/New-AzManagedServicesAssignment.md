---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 3627bace3d8ac0c24ecbfa865d7fa09b2d0de056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704903"
---
# New-AzManagedServicesAssignment

## STRESZCZENIe
Umożliwia utworzenie lub zaktualizowanie zadania rejestracji.

## POLECENIA

### Domyślne (domyślnie)
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinitionName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinition <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Umożliwia utworzenie lub zaktualizowanie zadania rejestracji.

## Przykłady

### Przykład 1
```powershell
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/d4d14a4c-9b54-4dc3-b755-6d0659e0224b

Name                                 RegistrationDefinitionId
----                                 ------------------------
3b3d5411-ec8c-4a52-8972-73f4952724b2 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/d4d14a4c-9b54-4dc3-b755-6d0659e0224b
```

Tworzy nowe zadanie rejestracji z pełnym kwalifikowanym identyfikatorem zasobu definicji rejestracji.

### Przykład 2
```powershell
New-AzManagedServicesAssignment -Scope /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/resourceGroups/mygroup1 -RegistrationDefinitionName 47f471b3-ff5f-463c-8a1f-286501b01ddc

Name                                 RegistrationDefinitionId
----                                 ------------------------
5aa0d921-64b8-40e8-af33-31993f0deaa8 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/47f471b3-ff5f-463c-8a1f-286501b01ddc
```

Tworzy przypisanie rejestracji z określonego zakresu i nazwy definicji rejestracji.

### Przykład 3
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $def

Name                                 RegistrationDefinitionId
----                                 ------------------------
a25f63d9-605c-4878-99bd-0d315480d46b /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/4a50f8eb-96b3-44c4-a397-e1e57035fe65
```
Tworzy zadanie rejestracji z określonym obiektem definicji rejestracji.
## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -RegistrationDefinition
Obiekt wejściowy definicji rejestracji.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RegistrationDefinitionResourceId
W pełni kwalifikowany identyfikator zasobu definicji rejestracji (na przykład/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57).

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationDefinitionName
Nazwa definicji rejestracji (na przykład b0c052e5-c437-4771-a476-8b1201158a57.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zakres
Zakres, w którym ma zostać utworzony przydział rejestracji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationAssignment

## INFORMACYJN

## LINKI POKREWNE
