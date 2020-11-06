---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: aa9b4dba29c766923966571c736c7f96a608df29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543172"
---
# Get-AzureRmNotificationHubsNamespaceAuthorizationRules

## STRESZCZENIe
Pobiera informacje o regułach autoryzacji skojarzonych z obszarem nazw centrum powiadomień.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** zwraca informacje o regułach autoryzacji związanych z dostępem do funkcji podpisów udostępnionych (SAS) skojarzonych z obszarem nazw centrum powiadomień.
Możesz zwrócić informacje dotyczące wszystkich reguł skojarzonych z obszarem nazw.
Możesz również zwrócić informacje dotyczące konkretnej reguły, a także podając parametr *AuthorizationRule* .

Reguły autoryzacji zarządzają dostępem do obszarów nazw.
Służą do tego tworzenie linków jako identyfikatorów URI na podstawie różnych poziomów uprawnień.
Może to być jedna z następujących poziomów platformy: 

- Słuch
- Wyślij
- Zarządzanie

Klienci są kierowani do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.
Na przykład klient, któremu nadano uprawnienie do odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.

To polecenie cmdlet pobiera tylko reguły autoryzacji skojarzone z obszarem nazw.
Aby uzyskać informacje na temat samego obszaru nazw, użyj polecenie Get-AzureRmNotificationHubsNamespace.

## Przykłady

### Przykład 1: uzyskiwanie informacji o wszystkich regułach autoryzacji przypisanych do obszarów nazw
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

To polecenie pobiera informacje o wszystkich regułach autoryzacji przypisanych zarówno do obszaru nazw ContosoNamespace, jak i grupy zasobów ContosoNotificationsGroup.

### Przykład 2: uzyskiwanie informacji na temat reguły autoryzacji
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

To polecenie pobiera informacje na temat jednej reguły autoryzacji obszaru nazw o nazwie ListenRule.
Aby uzyskać informacje dotyczące określonej reguły autoryzacji, należy uwzględnić obszar nazw i grupę zasobów.

## PARAMETRÓW

### -AuthorizationRule
Określa nazwę reguły uwierzytelniania SAS.
Te reguły określają typ dostępu do obszaru nazw użytkownikom.

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

### -Namespace
Określa obszar nazw, do którego są przypisywane reguły autoryzacji.
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

### -ResourceName
Określa grupę zasobów, do której są przydzielone reguły autoryzacji.

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

### System. Collections. Generic. list "1 [Microsoft. Azure. Commands. NotificationHubs. modele. SharedAccessAuthorizationRuleAttributes]

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Nowe — AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


