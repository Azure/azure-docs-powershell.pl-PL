---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240491"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Pobiera informacje o zasadach autoryzacji skojarzonych z przestrzenią nazw centrum powiadomień.

## SKŁADNIA

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzNotificationHubsNamespaceAuthorizationRule** zwraca informacje o zasadach autoryzacji podpisu dostępu udostępnionego (SAS) skojarzonych z przestrzenią nazw centrum powiadomień.
Możesz zwrócić informacje o wszystkich regułach skojarzonych z przestrzenią nazw.
Ewentualnie, uwzględniając parametr *AuthorizationRule,* możesz zwrócić informacje dotyczące określonej reguły.
Reguły autoryzacji zarządzają dostępem do przestrzeni nazw.
Jest to wykonywane przez utworzenie linków jako URI na podstawie różnych poziomów uprawnień.
Poziomy platformy mogą być następujące: 
- Słuchaj
- Wyślij
- Zarządzanie klientami jest kierowane do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.
Na przykład klient, który otrzymał uprawnienie Posłuchaj, zostanie przekierowyowany do URI dla tego uprawnienia.
To polecenie cmdlet pobiera tylko reguły autoryzacji skojarzone z przestrzenią nazw.
Aby uzyskać informacje o samej przestrzeni nazw, użyj funkcji Get-AzNotificationHubsNamespace.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji na temat wszystkich reguł autoryzacji przypisanych do przestrzeni nazw
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

To polecenie pobiera informacje na temat wszystkich reguł autoryzacji przypisanych zarówno do grupy zasobów ContosoNamespace przestrzeni nazw, jak i grupy zasobów ContosoNotificationsGroup.

### Przykład 2. Uzyskiwanie informacji o regułzie autoryzacji
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

To polecenie pobiera informacje na temat jednej reguły autoryzacji przestrzeni nazw o nazwie ListenRule.
Aby uzyskać informacje dotyczące określonej reguły autoryzacji, musisz dołączyć przestrzeń nazw i grupę zasobów.

## PARAMETERS

### -AuthorizationRule
Określa nazwę reguły uwierzytelniania SAS.
Te reguły określają typ dostępu, jaki użytkownicy mają do przestrzeni nazw.

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
Określa przestrzeń nazw, do której są przypisane reguły autoryzacji.
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

### -ResourceGroup
Określa grupę zasobów, do której są przypisane reguły autoryzacji.
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


