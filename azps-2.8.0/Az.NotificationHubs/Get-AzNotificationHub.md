---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: f58a34c5fb5a7ca108f2f4f55c9322f1f439fbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872032"
---
# Get-AzNotificationHub

## STRESZCZENIe
Pobiera informacje o koncentratorach powiadomień.

## POLECENIA

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzNotificationHub** pobiera informacje o koncentratorach powiadomień w określonym obszarze nazw i przypisano do określonej grupy zasobów.
Na przykład możesz uzyskać informacje o wszystkich koncentratorach powiadomień w obszarze nazw ContosoNamespace i przypisać je do grupy zasobów ContosoNotificationsGroup.
Możesz też użyć parametru *NotificationHub* , aby ograniczyć zwracane dane do informacji dotyczących określonego centrum powiadomień.
Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy, takiej jak iOS, Android, Windows Phone 8 i Windows Store, używanych przez tych klientów.
Te koncentratory są w przybliżeniu równoważne poszczególnym aplikacjom, a każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.
To polecenie cmdlet pobiera tylko informacje o koncentratorze.
Potrzebne są inne polecenia cmdlet, takie jak Get-AzNotificationHubAuthorizationRules, get-AzNotificationHubListKeys i Get-AzNotificationHubPNSCredentials, aby uzyskać informacje na temat reguł autoryzacji koncentratora, ciągów połączeń i poświadczeń usługi powiadamiania o platformie.

## Przykłady

### Przykład 1: uzyskiwanie informacji o wszystkich koncentratorach powiadomień w określonym obszarze nazw
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

To polecenie pobiera informacje dotyczące wszystkich koncentratorów powiadomień w przestrzeni nazw o nazwie ContosoNamespace, które zostały przypisane do grupy zasobów ContosoNotificationsGroup.

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

### -Namespace
Określa obszar nazw, do którego jest przypisany centrum powiadomień.
Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.

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

### -NotificationHub
Określa nazwę centrum powiadomień, które ma być pobierane przez to polecenie cmdlet.
Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.

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

### -ResourceName
Określa grupę zasobów, do której jest przypisany centrum powiadomień.
Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.

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

## WYSYŁA

### Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes

## INFORMACYJN

## LINKI POKREWNE

[Get-AzNotificationHubAuthorizationRules](./Get-AzNotificationHubAuthorizationRules.md)

[Get-AzNotificationHubListKeys](./Get-AzNotificationHubListKeys.md)

[Get-AzNotificationHubPNSCredentials](./Get-AzNotificationHubPNSCredentials.md)

[Nowe — AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


