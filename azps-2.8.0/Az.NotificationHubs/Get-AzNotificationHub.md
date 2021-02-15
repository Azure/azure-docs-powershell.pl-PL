---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: ea16c01e5c528742702dd08f1f2bd4c14e0cebcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400624"
---
# Get-AzNotificationHub

## SYNOPSIS
Otrzymuje informacje o Twoich centrach powiadomień.

## SKŁADNIA

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzNotificationHub** pobiera informacje o centrach powiadomień w określonej przestrzeni nazw i przypisuje je do określonej grupy zasobów.
Możesz na przykład uzyskać informacje dla wszystkich centrum powiadomień w przestrzeni nazw ContosoNamespace i przypisać je do grupy zasobów ContosoNotificationsGroup.
Możesz również użyć parametru *NotificationHub,* aby ograniczyć zwracane dane do informacji o określonym centrum powiadomień.
Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy, takiej jak systemy iOS, Android, Windows Phone 8 i Sklep Windows, używane przez tych klientów.
Te centra są mniej więcej równoważne poszczególnym aplikacjom, a każda z nich ma zazwyczaj własne centrum powiadomień.
To polecenie cmdlet pobiera tylko informacje o samym centrum.
Inne polecenia cmdlet, takie jak Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys i Get-AzNotificationHubPNSCredentials, są potrzebne do uzyskania informacji o zasadach autoryzacji centrum, ciągach połączeń i poświadczeniach usługi powiadomień platformy.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji dla wszystkich centrum powiadomień w określonej przestrzeni nazw
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

To polecenie pobiera informacje dla wszystkich centrum powiadomień w przestrzeni nazw o nazwie ContosoNamespace, które zostały przypisane do grupy zasobów ContosoNotificationsGroup.

## PARAMETERS

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

### —Przestrzeń nazw
Określa przestrzeń nazw, do której jest przypisane centrum powiadomień.
Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - NotificationHub
Określa nazwę centrum powiadomień, do których otrzymuje to polecenie cmdlet.
Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Określa grupę zasobów, do której jest przypisane centrum powiadomień.
Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## NOTATKI

## LINKI POKREWNE




[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


