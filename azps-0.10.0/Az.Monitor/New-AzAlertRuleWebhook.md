---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 420bfd3536c9bbf8bcfe075eb7ed56320788d3b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891158"
---
# New-AzAlertRuleWebhook

## STRESZCZENIe
Tworzy element webhook reguły alertu.

## POLECENIA

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzAlertRuleWebhook** tworzy element webhook reguły alertu.

## Przykłady

### Przykład 1: Tworzenie elementu webhook reguły alertu
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

To polecenie tworzy element webhook reguły alertu, określając tylko identyfikator URI usługi.

### Przykład 2: Tworzenie elementu webhook o jednej właściwości
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

To polecenie tworzy element webhook reguły alertu dla Contoso.com o jednej właściwości, a następnie zapisuje go w zmiennej $Actual.

## PARAMETRÓW

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Management. Monitor. Management. models. RuleWebhookAction

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzLogAlertRule](./Add-AzLogAlertRule.md)

[Dodaj-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Dodaj-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[Nowe — AzAlertRuleEmail](./New-AzAlertRuleEmail.md)

[Nowe — AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


