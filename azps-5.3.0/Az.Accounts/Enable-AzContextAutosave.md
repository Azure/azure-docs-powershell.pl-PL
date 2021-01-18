---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502605"
---
# Enable-AzContextAutosave

## STRESZCZENIe
Konteksty platformy Azure to obiekty programu PowerShell reprezentujące aktywną subskrypcję, za pomocą których można uruchamiać polecenia, oraz informacje uwierzytelniające potrzebne do nawiązania połączenia z chmurą platformy Azure. W przypadku kontekstów platformy Azure Program Azure PowerShell nie musi ponownie uwierzytelniać konta za każdym razem, gdy użytkownik przełączy abonament. Aby uzyskać więcej informacji, zobacz [obiekty kontekstu środowiska Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).

To polecenie cmdlet umożliwia zapisywanie i automatyczne ładowanie informacji kontekstowych platformy Azure po uruchomieniu procesu programu PowerShell. Na przykład podczas otwierania nowego okna.

## POLECENIA

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis

Umożliwia zapisywanie i automatyczne ładowanie informacji o kontekście platformy Azure po uruchomieniu procesu programu PowerShell. Kontekst zostanie zapisany na końcu wykonania dowolnego polecenia cmdlet, które wpływa na kontekst. Na przykład dowolne polecenie cmdlet profile. Jeśli korzystasz z uwierzytelniania użytkowników, tokeny mogą być aktualizowane w trakcie uruchamiania dowolnego polecenia cmdlet.

## Przykłady

### Przykład 1: Włączanie autozapisywania poświadczeń dla bieżącego użytkownika

Włącz funkcję Autozapisu w poświadczeniach dla bieżącego użytkownika. Za każdym razem, gdy zostanie otwarte okno programu PowerShell, Twój bieżący kontekst zostanie zapamiętany bez logowania.

```powershell
Enable-AzContextAutosave
```

### Przykład 2

Zezwalanie na zapisywanie i automatyczne ładowanie informacji o poświadczeniach, kontach i subskrypcjach platformy Azure podczas otwierania okna programu PowerShell w tej sesji programu PowerShell. (autogenerowana)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETRÓW

### -DefaultProfile

Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

Określa zakres zmian kontekstu. Na przykład, czy zmiany dotyczą tylko bieżącego procesu, czy wszystkich sesji uruchomionych przez tego użytkownika. Zmiany wprowadzone w zakresie wpłyną `CurrentUser` na wszystkie sesje programu PowerShell uruchomione przez użytkownika. Jeśli określona sesja wymaga różnych ustawień, użyj zakresu `Process` .

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
Nie jest uruchamiane polecenie cmdlet.

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

To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## INFORMACYJN

## LINKI POKREWNE
