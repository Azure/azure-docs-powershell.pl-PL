---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100396034"
---
# New-AzAlertRuleEmail

## SYNOPSIS
Tworzy akcję wiadomości e-mail dla reguły alertu.

## SKŁADNIA

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzAlertRuleEmail** tworzy akcję poczty e-mail dla reguły alertu.

## PRZYKŁADY

### Przykład 1. Tworzenie akcji wiadomości e-mail reguły alertu dla właścicieli usług
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

To polecenie tworzy akcję poczty e-mail reguły alertu w celu wysłania jej właścicielom usługi po jej zwolniniu z alertu.

### Przykład 2. Tworzenie akcji poczty e-mail reguły alertu dla właścicieli niebędące usługami
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

To polecenie tworzy akcję poczty e-mail reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.

### Przykład 3. Tworzenie akcji wiadomości e-mail reguły alertu dla właścicieli usług i osób niebędących usługami
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

To polecenie tworzy akcję poczty e-mail reguły alertu dla określonego adresu i dla jego właścicieli usługi.

## PARAMETERS

### - CustomEmail
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

### -SendToServiceOwner
Wskazuje, że ta operacja wysyła wiadomość e-mail do właścicieli usług w momencie jej odpalowania.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String[]

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.Monitor.Management.Models.RuleemailAction

## NOTATKI

## LINKI POKREWNE


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


