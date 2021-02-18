---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240490"
---
# Set-AzNotificationHubAuthorizationRule

## SYNOPSIS
Ustawia reguły autoryzacji dla centrum powiadomień.

## SKŁADNIA

### InputFileParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzNotificationHubAuthorizationRule** modyfikuje regułę autoryzacji sas (Shared Access Signature) przypisaną do centrum powiadomień.
Reguły autoryzacji zarządzają dostępem do centrum powiadomień przez utworzenie linków ( URI) na podstawie różnych poziomów uprawnień.
Poziomy uprawnień mogą być następujące: 
- Słuchaj
- Wyślij
- Zarządzanie klientami jest kierowane do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.
Na przykład klient, który otrzymał uprawnienie Posłuchaj, zostanie przekierowyowany do URI tego uprawnienia.
To polecenie cmdlet udostępnia dwa sposoby modyfikowania reguły autoryzacji przypisanej do centrum powiadomień.
Na przykład możesz utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes,** a następnie skonfigurować ten obiekt przy użyciu wartości właściwości, które mają być posiadania reguły.
Obiekt można skonfigurować za pomocą programu .NET Framework.
Następnie możesz skopiować te wartości właściwości do reguły, używając *parametru SASRule.*
Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości za pomocą *parametru InputFile.*
Plik JSON to plik tekstowy o składni podobnej do tej: { "Name": "ContosoAuthorizationRule",  
  "Klucz Podstawowy": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
  "Prawa": \[  
        "Słuchaj",  
        "Wyślij"  
    \]  
  } W połączeniu z poleceniem cmdlet New-AzNotificationHubAuthorizationRule poprzedni przykładowy kod JSON modyfikuje regułę autoryzacji o nazwie ContosoAuthorizationRule, aby umożliwić użytkownikom odsłuchiwanie i wysyłanie praw do centrum.

## PRZYKŁADY

### Przykład 1. Modyfikowanie reguły autoryzacji przypisanej do centrum powiadomień
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

To polecenie modyfikuje regułę autoryzacji przypisaną do centrum powiadomień o nazwie ContosoExternalHub.
Należy określić przestrzeń nazw, w której znajduje się centrum, oraz grupę zasobów przypisaną do centrum.
Zmodyfikowana reguła nie jest uwzględniana w samym poleceniu.
Zamiast tego informacje znajdują się w pliku wejściowym, w C:\Configuration\AuthorizationRules.jspliku.

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

### — Wymuszanie
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

### -InputFile
Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji nowej reguły.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
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
Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od tego, z których z nich korzystać.

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
Określa grupę zasobów, do której jest przypisane centrum powiadomień. Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.

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
Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji zmodyfikowanych reguł autoryzacji.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
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

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)


