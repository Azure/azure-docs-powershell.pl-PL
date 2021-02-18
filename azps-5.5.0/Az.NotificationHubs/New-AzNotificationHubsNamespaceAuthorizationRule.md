---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240483"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Tworzy regułę autoryzacji i przypisuje regułę do przestrzeni nazw centrum powiadomień.

## SKŁADNIA

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** tworzy regułę autoryzacji sas (Shared Access Signature) i przypisuje ją do przestrzeni nazw centrum powiadomień.
Reguły autoryzacji zarządzają prawami użytkowników do przestrzeni nazw i do centrum powiadomień zawartych w tej przestrzeni nazw.
To polecenie cmdlet udostępnia dwa sposoby tworzenia nowej reguły autoryzacji i przypisywania jej do przestrzeni nazw.
Możesz utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes,** a następnie skonfigurować ten obiekt przy użyciu wartości właściwości, które ma posiadać nowa reguła.
Można to zrobić za pomocą programu .NET Framework.
Następnie możesz skopiować te wartości właściwości do nowej reguły, używając *parametru SASRule.*
Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości, używając *parametru InputFile.*
Plik JSON to plik tekstowy o składni podobnej do następującej: {  
    "Name": "ContosoAuthorizationRule",  
    "Klucz Podstawowy": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Prawa": \[  
        "Słuchaj",  
        "Wyślij"  
    \]  
} W połączeniu z poleceniem cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** poprzedni przykład JSON tworzy regułę autoryzacji o nazwie ContosoAuthorizationRule, która zapewnia użytkownikom prawa do odsłuchiwanie i wysyłanie do przestrzeni nazw.
Klucz *Podstawowy używany* do uwierzytelniania można losowo wygenerować za pomocą następującego polecenia programu Windows PowerShell: Convert \[ \] ::ToBase64String((1,32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))

## PRZYKŁADY

### Przykład 1. Tworzenie reguły autoryzacji i przypisywanie jej do przestrzeni nazw
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

To polecenie tworzy regułę autoryzacji i przypisuje tę regułę do przestrzeni nazw ContosoNamespace.
Tworząc tę regułę, należy określić odpowiednią przestrzeń nazw i grupę zasobów, do których jest przypisana przestrzeń nazw.
Nie trzeba jednak określać żadnych informacji na temat samej reguły: informacje o regułach będą pochodzić z pliku C:\Configuration\NamespaceAuthorizationRules.jswejściowych.

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

### -InputFile
Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji dla nowej reguły autoryzacji.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### —Przestrzeń nazw
Określa przestrzeń nazw, do której zostaną przypisane reguły autoryzacji.
Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.
Nowe reguły muszą zostać przypisane do istniejącej przestrzeni nazw.
Polecenie **cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** nie może utworzyć nowej przestrzeni nazw.

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
Określa grupę zasobów, do której jest przypisana przestrzeń nazw.
Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.
Należy użyć istniejącej grupy zasobów.
To polecenie cmdlet nie może utworzyć nowej grupy zasobów.

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

### -SASRule
Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji dla nowych reguł.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


