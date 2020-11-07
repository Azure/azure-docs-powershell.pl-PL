---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 40747a82cab67a61e6a65e9eba4f3ba6ebc66f96
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892473"
---
# New-AzRoleDefinition

## STRESZCZENIe
Tworzy rolę niestandardową w usłudze Azure RBAC.
Podaj plik definicji roli JSON lub obiekt PSRoleDefinition jako dane wejściowe.
Najpierw użyj polecenia Get-AzRoleDefinition, aby wygenerować obiekt definicji roli punktu odniesienia.
Następnie zmodyfikuj jej właściwości stosownie do potrzeb.
Na koniec Użyj tego polecenia, aby utworzyć rolę niestandardową przy użyciu definicji roli.

## POLECENIA

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzRoleDefinition tworzy rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.
Podaj definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.
Definicja roli wejściowej musi zawierać następujące właściwości:
1) DisplayName: Nazwa roli niestandardowej
2) Opis: Krótki opis roli, która podsumowuje dostęp przyznany przez rolę.
3) Akcje: zestaw operacji, do których rola niestandardowa udziela dostępu.
Użyj Get-AzProviderOperation, aby uzyskać dostęp do operacji dla dostawców zasobów platformy Azure, które można zabezpieczyć przy użyciu usługi Azure RBAC.
Poniżej przedstawiono niektóre prawidłowe ciągi operacji:
 - "*/read" udziela dostępu do operacji odczytu wszystkich dostawców zasobów platformy Azure.
 - "Microsoft. Network/*/Read" udziela dostępu do operacji odczytu dla wszystkich typów zasobów w dostawcy zasobów Microsoft. Network na platformie Azure.
 - "Microsoft. COMPUTE/virtualMachines//*" udziela dostępu wszystkim operacjom maszyn wirtualnych i jego podrzędnych typów zasobów.
4) AssignableScopes: zestaw zakresów (subskrypcje platformy Azure lub grupy zasobów), w których rola niestandardowa będzie dostępna do przypisania.
Korzystając z AssignableScopes, możesz ustawić rolę niestandardową dla przydziałów tylko w przypadku abonamentów lub grup zasobów, które ich potrzebują, a nie nie ma potrzeby nieuwzględniania środowiska użytkownika dla pozostałych subskrypcji lub grup zasobów.
Poniżej przedstawiono niektóre z następujących zakresów, które można przydzielać:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"; "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": udostępnia rolę do przypisania w dwóch abonamentach.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": udostępnia rolę do przypisania w ramach jednej subskrypcji.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": udostępnia rolę do przypisania tylko w grupie zasób sieciowy.
Definicja roli wejściowej może zawierać następujące właściwości:
1) Noactions: zestaw operacji, które muszą być wykluczone z akcji, aby określić skuteczne działania roli niestandardowej.
Jeśli istnieje określona operacja, której nie chcesz udzielać dostępu w roli niestandardowej, wygodnie jest użyć funkcji noactions, aby ją wykluczyć, a nie określając wszystkich operacji innych niż określona operacja w działaniach.
2) Akcje danych: zestaw operacji na dane, do których rola niestandardowa udziela dostępu.
3) NotDataActions: zestaw operacji, które muszą być wykluczone z akcji dataactions w celu określenia efektywnych akcji dataactions dla roli niestandardowej.
Jeśli istnieje określona operacja na danych, której nie chcesz udzielać dostępu w roli niestandardowej, wygodnie jest używać NotDataActions do jej wykluczania, a nie do określania wszystkich operacji innych niż określona operacja w działaniach.
Uwaga: Jeśli użytkownikowi przypisano rolę określającą operację w argumentach zagranicowanie, a także przypisana innej roli udziela dostępu do tej samej operacji, użytkownik będzie mógł wykonać tę operację.
Nonaruszone nie jest regułą Odmów — jest to wygodna metoda tworzenia zestawu dozwolonych operacji, gdy trzeba wykluczyć konkretne operacje.
Poniżej przedstawiono przykładową definicję roli JSON, którą można podać jako dane wejściowe {"name": "zaktualizowana rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": " \[ */Read", "Microsoft. ClassicCompute/virtualmachines/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] ; "zanaruszone": \[ "* /Write" \] ; "akcje danych": \[ "Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/Read", "NotDataActions": "Microsoft. Storage/storageAccounts/blobServices/Containers \] \[ /BLOB/Write", "AssignableScopes" \] : \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## Przykłady

### Tworzenie przy użyciu PSRoleDefinitionObject
```
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

### Tworzenie przy użyciu pliku JSON
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plik_wejściowy
Nazwa pliku zawierającego jedną definicję roli JSON.

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

### -Rola
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition

## INFORMACYJN
Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

