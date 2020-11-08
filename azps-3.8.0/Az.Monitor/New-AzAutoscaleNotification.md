---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051949"
---
# New-AzAutoscaleNotification

## STRESZCZENIe
Umożliwia utworzenie powiadomienia e-mail autoskalowania.

## POLECENIA

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzAutoscaleNotification** umożliwia utworzenie powiadomienia e-mail w celu automatycznego skalowania.

## Przykłady

### Przykład 1: Tworzenie powiadomienia e-mail autoskalowania
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

To polecenie tworzy powiadomienie o Autosacale e-mail dla dwóch określonych adresów.

### Przykład 2: Tworzenie powiadomienia e-mail autoskalowania dla administratora subskrypcji
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

To polecenie tworzy powiadomienie o Autosacale pocztą e-mail dla administratora subskrypcji.

## PARAMETRÓW

### -CustomEmail
Określa listę adresów e-mail rozdzielonych przecinkami.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -SendEmailToSubscriptionAdministrator
Wskazuje, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.

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

### -SendEmailToSubscriptionCoAdministrator
Wskazuje, że ta operacja wysyła powiadomienie e-mail do współadministratora subskrypcji.

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

### -Webhook
Określa listę rozdzielanych przecinkami punktów webhook.

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification []

### System. String []

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Management. Monitor. Management. models. AutoscaleNotification

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


