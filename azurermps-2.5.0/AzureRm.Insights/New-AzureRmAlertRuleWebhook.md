---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
ms.openlocfilehash: d45624da172ecafba48354968d5a3ac5531be693
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899328"
---
# New-AzureRmAlertRuleWebhook

## STRESZCZENIe
Tworzy element webhook reguły alertu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmAlertRuleWebhook** tworzy element webhook reguły alertu.

## Przykłady

### Przykład 1: Tworzenie elementu webhook reguły alertu
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

To polecenie tworzy element webhook reguły alertu, określając tylko identyfikator URI usługi.

### Przykład 2: Tworzenie elementu webhook o jednej właściwości
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

To polecenie tworzy element webhook reguły alertu dla Contoso.com o jednej właściwości, a następnie zapisuje go w zmiennej $Actual.

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

### -Property
Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceUri
Określa identyfikator URI usługi.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Management. Monitor. Management. models. RuleWebhookAction

## INFORMACYJN

## LINKI POKREWNE



[Dodaj-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Dodaj-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Nowe — AzureRmAlertRuleEmail](./New-AzureRmAlertRuleEmail.md)

[Nowe — AzureRmAutoscaleWebhook](./New-AzureRmAutoscaleWebhook.md)


