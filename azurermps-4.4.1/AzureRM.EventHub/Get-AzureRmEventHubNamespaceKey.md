---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553904"
---
# Get-AzureRmEventHubNamespaceKey

## STRESZCZENIe
Pobiera szczegóły podstawowego, pomocniczego connectionStrings oraz kluczy reguły autoryzacji określonej reguły autoryzacji obszaru nazw koncentratorów zdarzeń.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## Opis
Polecenie cmdlet Get-AzureRmEventHubNamespaceKey zwraca podstawowe i pomocnicze connectionStrings oraz klucze dotyczące określonej reguły autoryzacji w danym obszarze nazw koncentratorów zdarzeń.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Pobiera szczegóły podstawowego, pomocniczego connectionStrings oraz kluczy dla reguły autoryzacji \` MyAuthRuleName w \` obszarze nazw Hub zdarzeń w obszarze nazw \` \` \` MyResourceGroupName \` .

## PARAMETRÓW

### -AuthorizationRuleName
Nazwa reguły autoryzacji w obszarze nazw koncentratorów zdarzeń.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### Microsoft. Azure. Commands. EventHub. modele. ListKeysAttributes

## INFORMACYJN

## LINKI POKREWNE

