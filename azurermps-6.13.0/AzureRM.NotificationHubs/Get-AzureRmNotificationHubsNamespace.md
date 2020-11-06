---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b4603566b793cbded7e593c9e4a23c3788c140de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553468"
---
# Get-AzureRmNotificationHubsNamespace

## STRESZCZENIe
Pobiera informacje o obszarze nazw centrum powiadomień.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmNotificationHubsNamespace** pobiera informacje o obszarach nazw centrum powiadomień.
To polecenie cmdlet umożliwia uzyskiwanie informacji dotyczących wszystkich obszarów nazw, informacji o obszarach nazw przypisanych do określonej grupy zasobów; lub zwracania informacji o określonym obszarze nazw.
Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.
Musisz mieć co najmniej jeden obszar nazw centrum powiadomień: wszystkie Centra powiadomień muszą być przypisane do obszaru nazw.
Jeden obszar nazw może zawierać wiele koncentratorów, co oznacza, że w organizacji może być potrzebny tylko jeden obszar nazw.
Możesz jednak korzystać z wielu obszarów nazw w celu lepszego organizowania koncentratorów lub nadawać konkretne osobom uprawnienia do zarządzania wybranym podzbiorem koncentratorów.
Polecenie cmdlet **Get-AzureRmNotificationHubsNamespace** zwraca podstawowe informacje o obszarze nazw.
Aby uzyskać informacje na temat reguł autoryzacji skojarzonych z obszarem nazw, użyj elementu Get-AzureRmNotificationHubsNamespaceAuthorizationRules.

## Przykłady

### Przykład 1: uzyskiwanie informacji dla wszystkich obszarów nazw centrum powiadomień
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

To polecenie zwraca informacje dotyczące wszystkich obszarów nazw centrum powiadomień.

### Przykład 2: uzyskiwanie informacji o jednej przestrzeni nazw centrum powiadomień
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

To polecenie pobiera informacje dotyczące jednej przestrzeni nazw centrum powiadomień: ContosoNamespace.

### Przykład 3: uzyskiwanie informacji dla wszystkich koncentratorów powiadomień przypisanych do określonego obszaru nazw
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

To polecenie pobiera informacje dla wszystkich obszarów nazw centrum powiadomień przypisanych do grupy zasobów ContosoNotificationsGroup.

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

### -Namespace
Określa unikatową nazwę obszaru nazw.
Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Określa grupę zasobów, do której przypisano obszar nazw.
Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft. Azure. Commands. NotificationHubs. models. NamespaceAttributes

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Nowe — AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


