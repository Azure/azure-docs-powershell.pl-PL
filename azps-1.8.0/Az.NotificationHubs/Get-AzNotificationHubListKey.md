---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 7ce6c3c08c1794e2bed794186203a5c6c0d1fdea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399893"
---
# Get-AzNotificationHubListKey

## SYNOPSIS
Pobiera podstawowe i pomocnicze parametry połączenia skojarzone z regułą autoryzacji centrum powiadomień.

## SKŁADNIA

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzNotificationHubListKey** zwraca podstawowe i pomocnicze parametry połączenia reguły autoryzacji podpisu dostępu udostępnionego (SAS) centrum powiadomień.
Reguły autoryzacji zarządzają prawami użytkowników do centrum.
Każda reguła zawiera podstawowy i pomocniczy ciąg połączenia.
Te parametry połączenia ( URI) wykonują następujące czynności:
- Wskaż użytkownikom zasób.
- Uwzględnianie tokenu zawierającego parametry zapytania.
Jeden z tych parametrów ( podpis) służy do uwierzytelniania użytkownika i zapewnienia określonego poziomu dostępu.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie podstawowych i pomocniczych ciągów połączenia dla reguły autoryzacji
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

To polecenie pobiera podstawowe i pomocnicze parametry połączenia reguły autoryzacji ListenRule — reguły przypisanej do centrum powiadomień aplikacji ContosoInternalHub.
To polecenie musi zawierać przestrzeń nazw centrum i grupę zasobów.

## PARAMETERS

### -AuthorizationRule
Określa nazwę reguły uwierzytelniania SAS (Shared Access Signature).
Te reguły określają typ dostępu użytkowników do Centrum powiadomień.

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
Określa centrum powiadomień, do których to polecenie cmdlet przypisuje regułę autoryzacji.
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

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## NOTATKI

## LINKI POKREWNE



