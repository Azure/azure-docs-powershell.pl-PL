---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 2f5ff44e6d96900afe36b9ade8360fb0a69ec726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951098"
---
# Set-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Ustawia reguły autoryzacji dla przestrzeni nazw centrum powiadomień.

## SKŁADNIA

### InputFileParameterSet
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** modyfikuje regułę autoryzacji sas (Shared Access Signature) przypisaną do przestrzeni nazw centrum powiadomień.
Reguły autoryzacji zarządzają prawami użytkowników do przestrzeni nazw i do centrum powiadomień zawartych w tej przestrzeni nazw.
To polecenie cmdlet udostępnia dwa sposoby modyfikowania reguły autoryzacji przypisanej do przestrzeni nazw.
Na przykład możesz utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes,** a następnie skonfigurować ten obiekt przy użyciu wartości właściwości, które mają być posiadania reguły.
Aby to .NET Framework, możesz użyć tej funkcji.
Następnie można skopiować te wartości właściwości do reguły za pomocą *parametru SASRule.*
Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości za pomocą *parametru InputFile.*
Plik JSON to plik tekstowy o składni podobnej do tej: {  
    "Name": "ContosoAuthorizationRule",  
    "Klucz Podstawowy": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Prawa": \[  
        "Słuchaj",  
        "Wyślij"  
    \]  
} W połączeniu z poleceniem cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** poprzedni przykład JSON modyfikuje regułę autoryzacji o nazwie ContosoAuthorizationRule, aby nadać użytkownikom prawa do odsłuchiania i wysyłania do przestrzeni nazw.

## PRZYKŁADY

### Przykład 1. Modyfikowanie reguły autoryzacji przypisanej do przestrzeni nazw
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

To polecenie modyfikuje regułę autoryzacji przypisaną do przestrzeni nazw o nazwie ContosoNamespace.
Należy określić grupę zasobów, do których jest przypisana przestrzeń nazw.
Informacje na temat reguły autoryzacji nie są zawarte w samym poleceniu.
Zamiast tego informacje są uzyskiwane z pliku wejściowego, C:\Configuration\AuthorizationRules.jsdalej.

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
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### —Przestrzeń nazw
Określa przestrzeń nazw zawierającą reguły autoryzacji, które modyfikuje to polecenie cmdlet.
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
Określa grupę zasobów, do której jest przypisana przestrzeń nazw.
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

### -SASRule
Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji reguł autoryzacji, które to polecenie cmdlet modyfikuje.

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

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespaceAuthorizationRule](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[Remove-AzNotificationHubsNamespaceAuthorizationRule](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


