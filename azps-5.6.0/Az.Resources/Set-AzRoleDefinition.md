---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 18488b44ff99c44d6362de68de45e81853418e0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971761"
---
# Set-AzRoleDefinition

## SYNOPSIS
Modyfikuje rolę niestandardową w usłudze Azure RBAC.
Podaj zmodyfikowaną definicję roli jako plik JSON lub jako definicję PSRoleDefinition.
Najpierw użyj polecenia Get-AzRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.
Następnie zmodyfikuj właściwości, które chcesz zmienić.
Na koniec zapisz definicję ról przy użyciu tego polecenia.

## SKŁADNIA

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie Set-AzRoleDefinition aktualizuje istniejącą rolę niestandardową w usłudze Azure Role-Based Access Control.
Podaj zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.
Definicja roli zaktualizowanej roli niestandardowej MUSI zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie są aktualizowane: DisplayName, Description, Actions, AssignableScopes.
NotActions, DataActions, NotDataActions są opcjonalne.
Poniżej przedstawiono przykładową zaktualizowaną definicję roli dla programu Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Zaktualizowano rolę", "Opis": "Może monitorować wszystkie zasoby oraz uruchamiać i ponownie uruchamiać maszyny wirtualne". "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" , "NotDataActions": "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" , "NotDataActions": "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" , "NotDataActions": "NotDataActions": "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## PRZYKŁADY

### Przykład 1. Aktualizacja przy użyciu funkcji PSRoleDefinitionObject
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### Przykład 2. Tworzenie przy użyciu pliku JSON
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### -InputFile
Nazwa pliku zawierająca jedną definicję roli json do zaktualizowania.
Uwzględnij tylko właściwości, które mają zostać zaktualizowane w JSON.
Właściwość Id jest wymagana.

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

### - Rola
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## NOTATKI
Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie

## LINKI POKREWNE

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

