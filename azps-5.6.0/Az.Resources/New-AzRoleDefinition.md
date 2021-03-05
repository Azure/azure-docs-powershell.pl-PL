---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 0930b66cf12d9c96d4fe00fa823cfd67c87081f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974458"
---
# New-AzRoleDefinition

## SYNOPSIS
Tworzy rolę niestandardową w usłudze Azure RBAC.
Jako dane wejściowe podaj plik definicji roli JSON lub obiekt PSRoleDefinition.
Najpierw użyj polecenia Get-AzRoleDefinition, aby wygenerować obiekt definicji roli planu bazowego.
Następnie zmodyfikuj jego właściwości zgodnie z wymaganiami.
Na koniec użyj tego polecenia, aby utworzyć rolę niestandardową przy użyciu definicji ról.

## SKŁADNIA

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie New-AzRoleDefinition cmdlet tworzy niestandardową rolę w usłudze Azure Role-Based Access Control.
Podaj definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.
Definicja roli wprowadzania MUSI zawierać następujące właściwości:
1) DisplayName: nazwa roli niestandardowej
2) Opis: krótki opis roli podsumowujący dostęp udzielany przez tę rolę.
3) Akcje: zestaw operacji, do których udziela dostęp rola niestandardowa.
Użyj Get-AzProviderOperation, aby uzyskać operację dla dostawców zasobów platformy Azure, które mogą być zabezpieczone przy użyciu usługi Azure RBAC.
Poniżej przedstawiono kilka prawidłowych ciągów operacji:
 - "*/read" udziela dostępu do operacji odczytu wszystkich dostawców zasobów platformy Azure.
 - "Microsoft.Network/*/read" udziela dostępu do operacji odczytu dla wszystkich typów zasobów dostawcy zasobów Microsoft.Network platformy Azure.
 - "Microsoft.Compute/virtualMachines/*" udziela dostępu do wszystkich operacji maszyn wirtualnych i ich typów zasobów podrzędnego.
4) AssignableScopes: zestaw zakresów (subskrypcji platformy Azure lub grup zasobów), w których rola niestandardowa będzie dostępna dla przydziału.
Za pomocą funkcji AssignableScopes możesz udostępnić niestandardową rolę dla przydziałów tylko w potrzebnych subskrypcjach lub grupach zasobów, a nie zaśmiecać środowisko użytkownika dla pozostałych subskrypcji lub grup zasobów.
Poniżej przedstawiono kilka prawidłowych zakresów, które można przypisać:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": umożliwia przypisanie roli w dwóch subskrypcjach.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": umożliwia przypisanie roli w ramach jednej subskrypcji.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": udostępnia rolę tylko w grupie zasobów sieciowych.
Definicja roli wprowadzania MOŻE zawierać następujące właściwości:
1) NotActions: zbiór operacji, które należy wykluczyć z akcji w celu określenia skutecznych akcji dla roli niestandardowej.
Jeśli nie chcesz udzielać dostępu do roli niestandardowej przez określoną operację, wygodnie jest wykluczyć ją za pomocą notactions, zamiast określać wszystkie operacje inne niż ta operacja w akcjach.
2) DataActions: zestaw operacji danych, do których rola niestandardowa udziela dostępu.
3) NotDataActions: zestaw operacji, które należy wykluczyć z akcji Danych w celu określenia skutecznych akcji danych dla roli niestandardowej.
Jeśli nie chcesz udzielać dostępu do danych w roli niestandardowej za pomocą funkcji NotDataActions, możesz ją wykluczyć za pomocą notDataActions, zamiast określać wszystkie operacje inne niż ta operacja w akcjach.
UWAGA: Jeśli użytkownikowi przypisano rolę określającą operację w notactions, a także inną rolę, udziela dostępu do tej samej operacji — użytkownik będzie mógł wykonać tę operację.
NotActions nie jest regułą odrzucaną — jest to po prostu wygodny sposób na utworzenie zestawu dozwolonych operacji, gdy trzeba wykluczyć określone operacje.
Poniżej przedstawiono przykładową definicję ról json, która może być dostarczana jako dane wejściowe { "Nazwa": "Zaktualizowana rola", "Opis": "Może monitorować wszystkie zasoby oraz uruchamiać i ponownie uruchamiać maszyny wirtualne", "Akcje": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices//blobServices/. containers/blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## PRZYKŁADY

### Przykład 1. Tworzenie przy użyciu funkcji PSRoleDefinitionObject
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### Przykład 2. Tworzenie przy użyciu pliku JSON
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
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
Nazwa pliku zawierająca jedną definicję roli json.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Rola
Obiekt definicji roli.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## NOTATKI
Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie

## LINKI POKREWNE

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

