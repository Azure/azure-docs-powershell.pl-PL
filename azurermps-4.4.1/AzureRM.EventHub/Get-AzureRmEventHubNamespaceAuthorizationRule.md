---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719326"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## STRESZCZENIe
Pobiera szczegóły reguły autoryzacji obszaru nazw Eventubs lub pobiera listę reguł autoryzacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## Opis
Polecenie cmdlet Get-AzureRmEventHubNamespaceAuthorizationRule pobiera szczegóły dotyczące określonej reguły autoryzacji obszaru nazw koncentratora zdarzeń lub listę reguł autoryzacji obszaru nazw.
Jeśli jest podana nazwa reguły autoryzacji, zostanie zwrócona wartość szczegółów jednej reguły autoryzacji.
Jeśli nie podano nazwy reguły autoryzacji, zostanie zwrócona lista wszystkich reguł autoryzacji w obszarze nazw.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Zwraca regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw Hub zdarzeń obszar_nazwname \` \` o MyResourceGroupName grupy zasobów \` \` .

### Przykład 2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

Zwraca domyślną regułę autoryzacji \` RootManageSharedAccessKey \` w obszarze nazw Hubs nazwy obszar_nazwname \` \` z grupą zasobów \` MyResourceGroupName \` .

### Przykład 3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Zwraca wszystkie reguły autoryzacji w przestrzeni nazw Hub zdarzeń \` \` o adresie NamespaceName z grupą \` MyResourceGroupName \` .

## PARAMETRÓW

### -AuthorizationRuleName
Nazwa reguły autoryzacji obszaru nazw koncentratorów zdarzeń.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
Nazwa obszaru nazw koncentratorów zdarzeń.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## INFORMACYJN

## LINKI POKREWNE

