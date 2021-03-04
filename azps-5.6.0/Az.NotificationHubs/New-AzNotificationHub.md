---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951290"
---
# New-AzNotificationHub

## SYNOPSIS
Tworzy centrum powiadomień.

## SKŁADNIA

### InputFileParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzNotificationHub** tworzy centrum powiadomień.
Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.
Centra powiadomień są mniej więcej równoważne poszczególnym aplikacjom: każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.
Polecenie **cmdlet New-AzNotificationHub** zapewnia dwa sposoby tworzenia nowego centrum powiadomień.
Możesz utworzyć wystąpienie obiektu **NotificationHubAttributes,** a następnie skonfigurować ten obiekt.
Następnie możesz skopiować te wartości właściwości do nowego centrum za pomocą *parametru NotificationHubObj.*
Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości, używając *parametru InputFile.*
W połączeniu z poleceniem cmdlet **New-AzNotificationHub** poprzedni przykład JSON tworzy centrum powiadomień o nazwie ContosoNotificationHub znajdujące się w centrum danych Stanów Zjednoczonych Zachód.

## PRZYKŁADY

### Przykład 1. Tworzenie centrum powiadomień
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

To polecenie tworzy centrum powiadomień w przestrzeni nazw ContosoNamespace.
Nowe centrum zostanie przypisane do grupy ContosoNotificationsGroup.
Nie trzeba określać nazwy ani żadnych innych informacji o konfiguracji centrum; te informacje zostaną z pliku wejściowego C:\Configurations\InternalHub.jsdalej.

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
Określa ścieżkę do pliku JSON zawierającego wartości konfiguracyjne dla nowego centrum powiadomień.

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
Określa przestrzeń nazw, do której zostanie przypisane centrum powiadomień.
Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.
Centra powiadomień muszą być przypisane do istniejącej przestrzeni nazw.
Polecenie **cmdlet New-AzNotificationHub** nie może utworzyć nowej przestrzeni nazw.

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

### -NotificationHubObj
Określa obiekt **NotificationHubAttributes** zawierający informacje o konfiguracji dla nowego centrum.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Określa grupę zasobów, do której zostanie przypisane centrum powiadomień.
Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.
Należy użyć istniejącej grupy zasobów.
Polecenie **cmdlet New-AzNotificationHub** nie może utworzyć nowej grupy zasobów.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHub](./Get-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


