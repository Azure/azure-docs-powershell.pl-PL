---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549171"
---
# New-AzureRmAlertRuleEmail

## STRESZCZENIe
Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmAlertRuleEmail** umożliwia utworzenie akcji poczty e-mail dla reguły alertu.

## Przykłady

### Przykład 1: Tworzenie akcji e-mail z regułą alertów dla właścicieli usługi
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

To polecenie umożliwia utworzenie akcji wiadomości e-mail z regułą alertu w celu wysłania jej właścicielom usług, gdy zostanie wygenerowane jej reguły alertu.

### Przykład 2: Tworzenie akcji e-mail z regułą alertów dla właścicieli niebędących usługami
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

To polecenie tworzy akcję e-mail dotyczącą reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.

### Przykład 3: Tworzenie reguły alertu e-mail dla właścicieli usługi i właścicieli niebędących usługami
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

To polecenie umożliwia utworzenie akcji e-mail dotyczącej reguły alertu dla określonego adresu i jego właścicieli.

## PARAMETRÓW

### -CustomEmails
Określa listę adresów e-mail rozdzielanych przecinkami.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SendToServiceOwners
Wskazuje, że ta operacja wysyła wiadomość e-mail do właścicieli usługi, gdy reguła jest uruchamiana.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Management. Monitor. Management. models. RuleEmailAction

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Dodaj-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Dodaj-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Nowe — AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


