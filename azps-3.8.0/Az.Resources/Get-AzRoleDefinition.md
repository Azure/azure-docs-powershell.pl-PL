---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050987"
---
# Get-AzRoleDefinition

## STRESZCZENIe
Lista wszystkich ról usługi Azure RBAC dostępnych do przypisania.

## POLECENIA

### RoleDefinitionNameParameterSet (domyślny)
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionIdParameterSet
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionCustomParameterSet
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Użyj polecenia Get-AzRoleDefinition z określoną nazwą roli, aby wyświetlić jego szczegóły.
Aby sprawdzić poszczególne operacje, do których rola udziela dostępu, przejrzyj właściwości akcji i nienaruszonych ról.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

Pobierz definicję roli czytelnika

### Przykład 2
```
PS C:\> Get-AzRoleDefinition
```

Lista wszystkich definicji ról RBAC

## PARAMETRÓW

### -Custom
Jeśli ta informacja jest określona, wyświetlane są tylko niestandardowe role utworzone w katalogu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -ID
Identyfikator definicji roli.

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa definicji roli.
Dla przykładu czytelnik, współautor, współautor maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zakres
Zakres definicji roli.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. GUID

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE

[Nowe — AzRoleAssignment](./New-AzRoleAssignment.md)

[Get-AzRoleAssignment](./Get-AzRoleAssignment.md)

[Nowe — AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

