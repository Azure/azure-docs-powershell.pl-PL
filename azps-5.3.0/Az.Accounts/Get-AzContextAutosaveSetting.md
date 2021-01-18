---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502594"
---
# Get-AzContextAutosaveSetting

## STRESZCZENIe
Wyświetla metadane dotyczące funkcji automatycznego zapisu kontekstowego, w tym informacje o tym, czy kontekst jest automatycznie zapisywany, oraz gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.

## POLECENIA

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Wyświetla metadane dotyczące funkcji automatycznego zapisu kontekstowego, w tym informacje o tym, czy kontekst jest automatycznie zapisywany, oraz gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.

## Przykłady

### Pobieranie metadanych kontekstu zapisu dla bieżącej sesji
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

Uzyskaj szczegółowe informacje o tym, czy i gdzie kontekst jest zapisany.  W powyższym przykładzie funkcja Autozapis została wyłączona.

### Pobieranie metadanych kontekstu zapisu dla bieżącego użytkownika
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

Uzyskaj szczegółowe informacje o tym, czy i gdzie kontekst jest domyślnie zapisywany dla bieżącego użytkownika.  Zauważ, że może to być inne niż ustawienia aktywne w bieżącej sesji. W powyższym przykładzie funkcja Autozapis została włączona, a dane są zapisywane w lokalizacji domyślnej.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## INFORMACYJN

## LINKI POKREWNE
