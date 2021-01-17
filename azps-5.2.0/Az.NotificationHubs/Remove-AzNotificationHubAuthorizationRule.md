---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336190"
---
# Remove-AzNotificationHubAuthorizationRule

## STRESZCZENIe
Usuwa regułę autoryzacji z centrum powiadomień.

## POLECENIA

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzNotificationHubAuthorizationRule** usuwa regułę autoryzacji współużytkowanego podpisu dostępu (SAS) z centrum powiadomień.
Reguły autoryzacji zarządzają dostępem do koncentratorów powiadomień za pomocą tworzenia linków, takich jak identyfikatory URI, na podstawie różnych poziomów uprawnień.
Poziom uprawnień może być jednym z następujących: 
- Słuch
- Wyślij
- Zarządzanie klientami jest przekierowywane do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.
Na przykład klient, któremu nadano uprawnienie do odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.
Usunięcie reguły autoryzacji powoduje również usunięcie odpowiednich uprawnień użytkownika.

## Przykłady

### Przykład 1: Usuwanie reguły autoryzacji z centrum powiadomień
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

To polecenie usuwa regułę autoryzacji o nazwie ListenRule z centrum powiadomień o nazwie ContosoExternalHub.
Po uruchomieniu tego polecenia musisz określić zarówno obszar nazw, jak i grupę zasobów, do których jest przypisany koncentrator.

## PARAMETRÓW

### -AuthorizationRule
Określa nazwę reguły uwierzytelniania SAS, która zostanie usunięta przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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

### -Force
Nie pytaj o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

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
Określa centrum powiadomień, do którego przypisani są reguły autoryzacji.
Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów bez względu na platformę.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Nowe — AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


