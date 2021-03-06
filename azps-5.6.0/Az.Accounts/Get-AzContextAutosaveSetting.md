---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 629e35c5b700477fc46565b2da0e5dcf6f3c5b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981345"
---
# Get-AzContextAutosaveSetting

## SYNOPSIS
Wyświetl metadane dotyczące funkcji autozazysowania kontekstu, w tym informacje o tym, czy kontekst jest zapisywany automatycznie, oraz gdzie można znaleźć zapisane informacje kontekstowe i poświadczenia.

## SKŁADNIA

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Wyświetl metadane dotyczące funkcji autozazysowania kontekstu, w tym informacje o tym, czy kontekst jest zapisywany automatycznie, oraz gdzie można znaleźć zapisane informacje kontekstowe i poświadczenia.

## PRZYKŁADY

### Uzyskiwanie metadanych zapisywania kontekstowego dla bieżącej sesji
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

Uzyskaj szczegółowe informacje na temat tego, czy i gdzie jest zapisywany kontekst.  W powyższym przykładzie funkcja autozazysowania została wyłączona.

### Uzyskiwanie metadanych zapisywania kontekstowego dla bieżącego użytkownika
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

Szczegółowe informacje o tym, czy i gdzie jest domyślnie zapisywany kontekst dla bieżącego użytkownika.  Pamiętaj, że może to być inne niż ustawienia aktywne w bieżącej sesji. W powyższym przykładzie funkcja autozazysowania została włączona i dane są zapisywane w lokalizacji domyślnej.

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

### — Zakres
Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## NOTATKI

## LINKI POKREWNE
