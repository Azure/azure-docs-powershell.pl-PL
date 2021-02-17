---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5c5517faa5dbd65cc6a76a02209cb2b8c429300a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399876"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Pobiera informacje o przestrzeni nazw centrum powiadomień.

## SKŁADNIA

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
**Polecenie cmdlet Get-AzNotificationHubsNamespace** pobiera informacje o przestrzeni nazw centrum powiadomień.
To polecenie cmdlet umożliwia uzyskanie informacji dla wszystkich przestrzeni nazw, informacji o przestrzeni nazw przypisanych do określonej grupy zasobów; lub na celu zwrócenie informacji o określonej przestrzeni nazw.
Przestrzenie nazw to kontenery logiczne, które ułatwiają organizowanie centrum powiadomień i zarządzanie nimi.
Musisz mieć co najmniej jedną przestrzeń nazw centrum powiadomień: wszystkie centra powiadomień muszą być przypisane do przestrzeni nazw.
Jedna przestrzeń nazw może zawierać wiele koncentratorów, co oznacza, że w organizacji może być potrzebna tylko jedna przestrzeń nazw.
Możesz jednak mieć także wiele przestrzeni nazw, aby lepiej zorganizować swoje centrum lub nadawać określonym osobom uprawnienia do zarządzania wybranym podzestawem centrów.
Polecenie **cmdlet Get-AzNotificationHubsNamespace** zwraca podstawowe informacje o samej przestrzeni nazw.
Aby uzyskać informacje na temat reguł autoryzacji skojarzonych z przestrzenią nazw, użyj funkcji Get-AzNotificationHubsNamespaceAuthorizationRules.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji dla wszystkich przestrzeni nazw centrum powiadomień
```
PS C:\>Get-AzNotificationHubsNamespace
```

To polecenie zwraca informacje dla wszystkich przestrzeni nazw centrum powiadomień.

### Przykład 2. Uzyskiwanie informacji dotyczących przestrzeni nazw pojedynczego centrum powiadomień
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

To polecenie pobiera informacje dla przestrzeni nazw centrum powiadomień: ContosoNamespace.

### Przykład 3. Uzyskiwanie informacji dla wszystkich centrum powiadomień przypisanych do określonej przestrzeni nazw
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

To polecenie pobiera informacje dla wszystkich przestrzeni nazw centrum powiadomień przypisanych do grupy zasobów ContosoNotificationsGroup.

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

### —Przestrzeń nazw
Określa unikatową nazwę przestrzeni nazw.
Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.

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

### - ResourceGroup
Określa grupę zasobów, do której jest przypisana przestrzeń nazw.
Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTATKI

## LINKI POKREWNE


[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


