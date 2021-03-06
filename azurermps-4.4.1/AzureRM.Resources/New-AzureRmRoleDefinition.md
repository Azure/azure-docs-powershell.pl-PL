---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549891"
---
# New-AzureRmRoleDefinition

## STRESZCZENIe
Tworzy rolę niestandardową w usłudze Azure RBAC.
Podaj plik definicji roli JSON lub obiekt PSRoleDefinition jako dane wejściowe.
Najpierw użyj polecenia Get-AzureRmRoleDefinition, aby wygenerować obiekt definicji roli punktu odniesienia.
Następnie zmodyfikuj jej właściwości stosownie do potrzeb.
Na koniec Użyj tego polecenia, aby utworzyć rolę niestandardową przy użyciu definicji roli.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### InputFileParameterSet
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzureRmRoleDefinition tworzy rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.
Podaj definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.

Definicja roli wejściowej musi zawierać następujące właściwości:

1) DisplayName: Nazwa roli niestandardowej

2) Opis: Krótki opis roli, która podsumowuje dostęp przyznany przez rolę.

3) Akcje: zestaw operacji, do których rola niestandardowa udziela dostępu.
Użyj Get-AzureRmProviderOperations, aby uzyskać dostęp do operacji dla dostawców zasobów platformy Azure, które można zabezpieczyć przy użyciu usługi Azure RBAC.
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

Uwaga: Jeśli użytkownikowi przypisano rolę określającą operację w argumentach zagranicowanie, a także przypisana innej roli udziela dostępu do tej samej operacji, użytkownik będzie mógł wykonać tę operację.
Nonaruszone nie jest regułą Odmów — jest to wygodna metoda tworzenia zestawu dozwolonych operacji, gdy trzeba wykluczyć konkretne operacje.

Poniżej przedstawiono przykładową definicję roli JSON, którą można podać jako dane wejściowe {"name": "firma Contoso jest w trakcie rozmowy", "opis": "może monitorować funkcje obliczeniowe, sieciowe i magazynowe, a także ponownie uruchamiać maszyny wirtualne", "akcje": \[ "Microsoft. COMPUTE/ */Read", "Microsoft. COMPUTE/virtualMachines/Start/* Action", "Microsoft. COMPUTE/virtualMachines//Action", "Microsoft. COMPUTE/virtualMachines/DownloadRemoteDesktopConnectionFile/Action Network//Read", "Microsoft. Storage/ */Read", "Microsoft. Authorization* //Read", "Microsoft. resources/subscriptiones/resourceGroups/odczytywać", "Microsoft. resources/subscriptions/resourceGroups/Resources/ *", "Microsoft.Support/* Read", "Microsoft. Insights/alertRules \] \[ \]

## Przykłady

### --------------------------Utwórz przy użyciu--------------------------PSRoleDefinitionObject
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### --------------------------Utworzyć przy użyciu pliku JSON--------------------------
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETRÓW

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Set-AzureRmRoleDefinition](./Set-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

