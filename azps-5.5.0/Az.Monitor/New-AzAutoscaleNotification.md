---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192186"
---
# New-AzAutoscaleNotification

## SYNOPSIS
Tworzy powiadomienie e-mail z automatycznym skalowaniem.

## SKŁADNIA

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzAutoscaleNotification** tworzy powiadomienie e-mail dla skalowania automatycznego.

## PRZYKŁADY

### Przykład 1. Tworzenie powiadomienia e-mail z automatycznym skalowaniem
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

To polecenie tworzy powiadomienie e-mail Autosacale dla dwóch określonych adresów.

### Przykład 2. Tworzenie powiadomienia e-mail o automatycznym skalowania dla administratora subskrypcji
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

To polecenie powoduje utworzenie powiadomienia e-mail Autosacale dla administratora subskrypcji.

## PARAMETERS

### - CustomEmail
Określa rozdzieloną przecinkami listę adresów e-mail.

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

### -SendEmailToSubscriptionAdministrator
Oznacza, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.

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
Oznacza, że ta operacja wysyła powiadomienie e-mail do współwłasnych administratorów subskrypcji.

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

### - Webhook
Określa rozdzielaną przecinkami listę autoskalowania sieci Web.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]

### System.String[]

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification

## NOTATKI

## LINKI POKREWNE

[New-AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


