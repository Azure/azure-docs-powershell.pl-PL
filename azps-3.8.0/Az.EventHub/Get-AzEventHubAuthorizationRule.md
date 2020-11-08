---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7fa3b4780e4c25dd716b851fd80c698b8d98d0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050790"
---
# Get-AzEventHubAuthorizationRule

## STRESZCZENIe
Pobiera szczegóły reguły autoryzacji lub pobiera listę reguł autoryzacji.

## POLECENIA

### NamespaceAuthorizationRuleSet (domyślny)
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventhubAuthorizationRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasAuthoRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzEventHubAuthorizationRule pobiera szczegóły reguły autoryzacji lub listę wszystkich reguł autoryzacji określonego centrum zdarzeń.
Jeśli jest podana nazwa reguły autoryzacji, zostaną zwrócone szczegóły dotyczące jednej reguły autoryzacji.
Jeśli nie podano nazwy reguły autoryzacji, zostanie zwrócona lista wszystkich reguł autoryzacji określonego centrum zdarzeń.
Jeśli zostanie podana nazwa aliasu (odzyskiwanie po awarii), zostanie zwrócona wartość szczegółów reguły autoryzacji obszaru nazw skonfigurowanego dla aliasu.

## Przykłady

### Przykład 1,0-AuthorizationRule dla obszaru nazw
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

Pobiera regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .

### Przykład 1,1-AuthorizationRules dla obszaru nazw
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Pobiera listę wszystkich reguł autoryzacji w obszarze nazw obszar_nazw \` \` .

### Przykład 2,0-AuthorizationRule dla EventHub
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

Pobiera regułę autoryzacji \` MyAuthRuleName \` w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw \` \` obszar_nazwname.

### Przykład 2,1-AuthorizationRules dla EventHub
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Pobiera reguły autoryzacji listy w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw obszar_nazwname \` \` .

### Przykład 3,0-AuthorizationRule dla aliasu (Konfiguracja geoawaryjna)
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

Pobiera regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .

### Przykład 3,1-AuthorizationRules dla aliasu (Konfiguracja geoawaryjna)
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

Pobiera listę wszystkich reguł autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .

## PARAMETRÓW

### -Aliasname
Nazwa aliasu

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### — Eventhub
Nazwa Eventhub

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa AuthorizationRule

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Nazwa obszaru nazw

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes

## INFORMACYJN

## LINKI POKREWNE
