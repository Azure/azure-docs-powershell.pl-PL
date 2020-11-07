---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e5fbecea64a15569fbd6319f3f3be5ff4102153e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719067"
---
# Disconnect-AzureRmAccount

## STRESZCZENIe
Odłączenie połączonego konta platformy Azure i usunięcie wszystkich poświadczeń i kontekstów skojarzonych z tym kontem.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Opis. tekst (domyślnie)
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UserId
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Serviceprincipal
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountName
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Tekst
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Disconnect-AzureRmAccount rozłącza połączone konto platformy Azure i usuwa wszystkie poświadczenia i konteksty (informacje o subskrypcji i dzierżawie) skojarzone z tym kontem.
Po wykonaniu tego polecenia musisz zalogować się ponownie przy użyciu polecenia Connect-AzureRmAccount.

## Przykłady

### Wylogowywanie się z bieżącego konta
```
PS C:\> Disconnect-AzureRmAccount
```

Wylogowuje się z konta platformy Azure skojarzonego z bieżącym kontekstem.

### Wylogowanie konta skojarzonego z określonym kontekstem
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

Wylogowuje konto skojarzone z danym kontekstem (nazwane "praca"). Ponieważ w tym polu jest używany zakres "CurrentUser", wszystkie poświadczenia i konteksty zostaną trwale usunięte.

### Wylogowywanie określonego użytkownika
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

Wylogowuje user1@contoso.org użytkownika "użytkownik — wszystkie poświadczenia i wszystkie konteksty skojarzone z tym użytkownikiem zostaną usunięte.

## PARAMETRÓW

### -Identyfikator aplikacji
Identyfikator podmiotu zabezpieczeń (unikatowy identyfikator globalny)

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureContext
Świetle

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ontextname
Nazwa kontekstu do wylogowania

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Obiekt konta do usunięcia

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Zakres
Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dzierżawy
Identyfikator dzierżawy (unikatowy identyfikator globalny)

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Nazwa użytkownika formularza ' user@contoso.org '

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest wykonywane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. profile. PSAzureRmAccount
Parametry: Inputobject (ByValue)

### Microsoft. Azure. Commands. profile. PSAzureContext
Parametry: AzureContext (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. profile. PSAzureRmAccount

## INFORMACYJN

## LINKI POKREWNE
