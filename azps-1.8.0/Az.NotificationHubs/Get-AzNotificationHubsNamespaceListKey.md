---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399859"
---
# Get-AzNotificationHubsNamespaceListKey

## SYNOPSIS
Pobiera podstawowe i pomocnicze parametry połączenia skojarzone z regułą autoryzacji przestrzeni nazw centrum powiadomień.

## SKŁADNIA

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzNotificationHubsNamespaceListKey** zwraca podstawowe i pomocnicze parametry połączenia dla reguły autoryzacji sas (Shared Access Signature) przypisanej do przestrzeni nazw centrum powiadomień.
Reguły autoryzacji zarządzają prawami użytkowników do przestrzeni nazw centrum powiadomień.
Każda reguła zawiera podstawowy i pomocniczy ciąg połączenia.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie podstawowych i pomocniczych ciągów połączenia dla reguły autoryzacji
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

To polecenie zwraca podstawowe i pomocnicze ciągi połączeń reguły autoryzacji o nazwie ListenRule przypisanej do przestrzeni nazw ContosoNamespace.
Po uruchomieniu tego polecenia musisz podać nazwę grupy zasobów, do których jest przypisana przestrzeń nazw.

## PARAMETERS

### -AuthorizationRule
Określa nazwę reguły uwierzytelniania SAS.
Te reguły określają typ dostępu użytkowników do Centrum powiadomień.

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
Określa przestrzeń nazw zawierającą ciągi połączeń, które otrzymuje to polecenie cmdlet.

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

### - ResourceGroup
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)



