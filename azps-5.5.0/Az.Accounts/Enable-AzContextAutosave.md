---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195443"
---
# Enable-AzContextAutosave

## SYNOPSIS
Konteksty platformy Azure to obiekty programu PowerShell reprezentujące aktywną subskrypcję, dla których mają być uruchamiane polecenia, oraz informacje o uwierzytelnianiu potrzebne do nawiązania połączenia z chmurą platformy Azure. W kontekście platformy Azure program Azure PowerShell nie musi ponownie uwierzytelniania konta przy każdym przełączaniu subskrypcji. Aby uzyskać więcej informacji, zobacz [obiekty kontekstowe programu Azure PowerShell.](https://docs.microsoft.com/powershell/azure/context-persistence)

To polecenie cmdlet umożliwia zapisanie i automatyczne załadowanie informacji kontekstowych platformy Azure po uruchomieniu procesu programu PowerShell. Na przykład podczas otwierania nowego okna.

## SKŁADNIA

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS

Umożliwia zapisanie i automatyczne załadowanie informacji kontekstowych platformy Azure podczas uruchamiania procesu programu PowerShell. Kontekst jest zapisywany na końcu wykonywania każdego polecenia cmdlet mającego wpływ na kontekst. Na przykład dowolne polecenie cmdlet profilu. Jeśli korzystasz z uwierzytelniania użytkownika, tokeny mogą być aktualizowane w trakcie uruchamiania dowolnego polecenia cmdlet.

## PRZYKŁADY

### Przykład 1. Włączanie poświadczeń automatycznegoavingu dla bieżącego użytkownika

Włącz funkcję autozazysowania poświadczeń dla bieżącego użytkownika. Przy każdym otwarciu okna programu PowerShell zostanie zapamiętany bieżący kontekst bez logowania się.

```powershell
Enable-AzContextAutosave
```

### Przykład 2

Zezwalaj na zapisanie i automatyczne załadowanie poświadczeń, konta i subskrypcji platformy Azure po otwarciu okna programu PowerShell w tej sesji programu PowerShell. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETERS

### -DefaultProfile

Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure

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

Określa zakres zmian kontekstu. Może to być na przykład zmiana mająca zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika. Zmiany wprowadzone w zakresie mają `CurrentUser` wpływ na wszystkie sesje programu PowerShell rozpoczęte przez użytkownika. Jeśli dla określonej sesji są potrzebne różne ustawienia, należy użyć `Process` zakresu.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
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

Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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

### Typowe parametry

To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## NOTATKI

## LINKI POKREWNE
