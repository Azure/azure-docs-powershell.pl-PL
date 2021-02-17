---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191531"
---
# Get-AzNotificationHubAuthorizationRule

## SYNOPSIS
Pobiera informacje o zasadach autoryzacji skojarzonych z centrum powiadomień.

## SKŁADNIA

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzNotificationHubAuthorizationRule** pobiera informacje o zasadach autoryzacji sygnatury dostępu udostępnionego (SAS) skojarzonych z centrum powiadomień.
Polecenie cmdlet zwraca informacje o wszystkich regułach skojarzonych z centrum lub, włączając parametr *AuthorizationRule,* pobiera informacje o określonej regułie.
Reguły autoryzacji zarządzają dostępem do Centrum powiadomień.
Reguła autoryzacji utworzy linki jako URI na podstawie różnych poziomów uprawnień.
Klienci są kierowani do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.
Na przykład klient z uprawnieniem Posłuchaj zostanie przekierowyowany do URI tego uprawnienia.
Polecenie **cmdlet Get-AzNotificationHubAuthorizationRule** pobiera tylko informacje o zasadach autoryzacji skojarzonych z centrum powiadomień.
Aby uzyskać informacje o samym centrum, użyj aplikacji Get-AzNotificationHub.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji dotyczących wszystkich reguł autoryzacji przypisanych do centrum powiadomień
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

To polecenie pobiera informacje dotyczące wszystkich reguł autoryzacji przypisanych do centrum powiadomień o nazwie ContosoInternalHub w przestrzeni nazw ContosoNamespace.
Należy określić przestrzeń nazw, w której znajduje się centrum, oraz grupę zasobów, do której przypisano centrum.

### Przykład 2. Uzyskiwanie informacji dotyczących reguł autoryzacji przypisanych do centrum powiadomień
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

To polecenie pobiera informacje dotyczące wszystkich reguł autoryzacji przypisanych do centrum powiadomień o nazwie ContosoInternalHub w przestrzeni nazw ContosoNamespace.
To polecenie używa *parametru AuthorizationRule* w celu ograniczenia zwracanych danych do jednej reguły autoryzacji o nazwie ListenRule.

## PARAMETERS

### -AuthorizationRule
Określa nazwę reguły uwierzytelniania SAS.
Te reguły określają typ dostępu użytkowników do Centrum powiadomień.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
Określa centrum powiadomień, do których to polecenie cmdlet przypisuje reguły autoryzacji.
Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Określa grupę zasobów, do której jest przypisane centrum powiadomień.
Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający zarządzanie zapasami i administrowanie azure.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


