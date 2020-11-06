---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: cfe24ac2900e46a031980886f80bf39b9eee28e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553651"
---
# Get-AzureRmNotificationHub

## STRESZCZENIe
Pobiera informacje o koncentratorach powiadomień.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmNotificationHub** pobiera informacje o koncentratorach powiadomień w określonym obszarze nazw i przypisano do określonej grupy zasobów.
Na przykład możesz uzyskać informacje o wszystkich koncentratorach powiadomień w obszarze nazw ContosoNamespace i przypisać je do grupy zasobów ContosoNotificationsGroup.

Możesz też użyć parametru *NotificationHub* , aby ograniczyć zwracane dane do informacji dotyczących określonego centrum powiadomień.

Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy, takiej jak iOS, Android, Windows Phone 8 i Windows Store, używanych przez tych klientów.
Te koncentratory są w przybliżeniu równoważne poszczególnym aplikacjom, a każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.

To polecenie cmdlet pobiera tylko informacje o koncentratorze.
Potrzebne są inne polecenia cmdlet, takie jak Get-AzureRmNotificationHubAuthorizationRules, get-AzureRmNotificationHubListKeys i Get-AzureRmNotificationHubPNSCredentials, aby uzyskać informacje na temat reguł autoryzacji koncentratora, ciągów połączeń i poświadczeń usługi powiadamiania o platformie.

## Przykłady

### Przykład 1: uzyskiwanie informacji o wszystkich koncentratorach powiadomień w określonym obszarze nazw
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

To polecenie pobiera informacje dotyczące wszystkich koncentratorów powiadomień w przestrzeni nazw o nazwie ContosoNamespace, które zostały przypisane do grupy zasobów ContosoNotificationsGroup.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: String
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
Type: String
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
Type: String
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

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### System. Collections. Generic. list "1 [Microsoft. Azure. Commands. NotificationHubs. modele. NotificationHubAttributes]

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[Get-AzureRmNotificationHubListKeys](./Get-AzureRmNotificationHubListKeys.md)

[Get-AzureRmNotificationHubPNSCredentials](./Get-AzureRmNotificationHubPNSCredentials.md)

[Nowe — AzureRmNotificationHub](./New-AzureRmNotificationHub.md)

[Remove-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)

[Set-AzureRmNotificationHub](./Set-AzureRmNotificationHub.md)


