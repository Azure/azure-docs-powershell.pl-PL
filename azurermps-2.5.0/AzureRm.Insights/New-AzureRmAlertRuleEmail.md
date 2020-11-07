---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
ms.openlocfilehash: 20134cc0f2eef927361439fb431bc4ab9308a9a1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899330"
---
# New-AzureRmAlertRuleEmail

## STRESZCZENIe
Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
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
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

To polecenie tworzy akcję e-mail dotyczącą reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.

### Przykład 3: Tworzenie reguły alertu e-mail dla właścicieli usługi i właścicieli niebędących usługami
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

To polecenie umożliwia utworzenie akcji e-mail dotyczącej reguły alertu dla określonego adresu i jego właścicieli.

## PARAMETRÓW

### -CustomEmail
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

### -SendToServiceOwner
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String []

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Management. Monitor. Management. models. RuleEmailAction

## INFORMACYJN

## LINKI POKREWNE



[Dodaj-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Dodaj-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Nowe — AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


