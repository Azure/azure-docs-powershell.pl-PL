---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: f0c22f199d19e97f957bc86fbee8d649d30b622d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718765"
---
# Set-AzureRmRoleDefinition

## STRESZCZENIe
Modyfikuje rolę niestandardową w usłudze Azure RBAC.
Podaj zmodyfikowaną definicję roli jako plik JSON lub jako PSRoleDefinition.
Najpierw użyj polecenia Get-AzureRmRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.
Następnie zmodyfikuj właściwości, które chcesz zmienić.
Na koniec Zapisz definicję roli za pomocą tego polecenia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet Set-AzureRmRoleDefinition aktualizuje istniejącą rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.
Wprowadź zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.
Definicja roli zaktualizowanej roli niestandardowej musi zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie zostały zaktualizowane: DisplayName, Description, Actions, AssignableScopes.
Nienaruszone, akcje dataNotDataActions są opcjonalne.
Poniżej przedstawiono przykładowy kod JSON zaktualizowanej definicji ról dla Set-AzureRmRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e"; "nazwa": "zaktualizowana rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] ; "zanaruszone": \[ "* /Write" \] ; "akcje danych": \[ "Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/Read", "NotDataActions": "Microsoft. Storage/storageAccounts/blobServices/Containers \] \[ /BLOB/Write", "AssignableScopes" \] : \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## Przykłady

### Aktualizowanie przy użyciu PSRoleDefinitionObject
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### Tworzenie przy użyciu pliku JSON
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plik_wejściowy
Nazwa pliku zawierającego pojedynczą definicję roli JSON do zaktualizowania.
Uwzględnij tylko właściwości, które mają zostać zaktualizowane w notacji JSON.
Właściwość ID jest wymagana.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rola
Obiekt definicji roli do zaktualizowania

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition
Parametry: role (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Nowe — AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

