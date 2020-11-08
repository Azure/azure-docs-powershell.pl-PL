---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 7eb19dfc45a954a9e23a3cc6c04190c3a1388547
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052007"
---
# AZ. Accounts module
## Opis
Zarządza poświadczeniami i typową konfiguracją dla wszystkich modułów platformy Azure.

## AZ.
### [Dodaj-AzEnvironment](Add-AzEnvironment.md)
Dodaje punkty końcowe i metadane wystąpienia Menedżera zasobów platformy Azure.

### [Clear-AzContext](Clear-AzContext.md)
Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.

### [Clear-AzDefault](Clear-AzDefault.md)
Czyści ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.

### [Connect — AzAccount](Connect-AzAccount.md)
Połącz się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Wyłącz Autozapisywanie poświadczeń platformy Azure.  Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Nie możesz zbierać danych, aby ulepszyć polecenia cmdlet usługi AzurePowerShell. Dane nie są zbierane, jeśli użytkownik wyraźnie nie zrezygnuje.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Wyłącza aliasy prefiksów AzureRm dla modułów AZ.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Odłączenie połączonego konta platformy Azure i usunięcie wszystkich poświadczeń i kontekstów skojarzonych z tym kontem.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
Zezwalaj na zapisywanie i automatyczne ładowanie informacji o poświadczeniach platformy Azure, kontach i subskrypcjach podczas otwierania okna programu PowerShell. 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet usługi AzurePowerShell.
Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.
Nie są zbierane żadne dane, o ile użytkownik wyraźnie nie zrezygnuje.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Włącza aliasy prefiksów AzureRm dla modułów AZ.

### [Get-AzContext](Get-AzContext.md)
Pobiera metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
Wyświetla metadane dotyczące funkcji automatycznego zapisu kontekstowego, w tym informacje o tym, czy kontekst jest automatycznie zapisywany, oraz gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.

### [Get-AzDefault](Get-AzDefault.md)
Uzyskiwanie wartości domyślnych ustawionych przez użytkownika w bieżącym kontekście.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Uzyskiwanie punktów końcowych i metadanych dla wystąpienia usług platformy Azure.

### [Get-AzProfile](Get-AzProfile.md)
Pobierz profile usług obsługiwane przez zainstalowane moduły.

### [Get-AzSubscription](Get-AzSubscription.md)
Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.

### [Get-AzTenant](Get-AzTenant.md)
Pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.

### [Import — AzContext](Import-AzContext.md)
Ładuje informacje o uwierzytelnianiu platformy Azure z pliku.

### [Rejestr — AzModule](Register-AzModule.md)
Tylko do użytku wewnętrznego — zapewnianie obsługi poleceń cmdlet dla funkcji przygenerowania.

### [Remove-AzContext](Remove-AzContext.md)
Usuwanie kontekstu z zestawu dostępnych kontekstów

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Umożliwia usunięcie punktów końcowych i metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.

### [Zmień nazwę — AzContext](Rename-AzContext.md)
Zmienianie nazwy kontekstu platformy Azure.  Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.

### [Rozpoznaj — AzError](Resolve-AzError.md)
Wyświetlanie szczegółowych informacji o błędach programu PowerShell z rozszerzonymi szczegółami dotyczącymi błędów programu Azure PowerShell.

### [Zapisz — AzContext](Save-AzContext.md)
Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.

### [Wybierz — AzContext](Select-AzContext.md)
Wybierz abonament i konto docelowe dla poleceń cmdlet środowiska Azure PowerShell

### [Wybierz — AzProfile](Select-AzProfile.md)
W przypadku modułów obsługujących wiele profilów usługi — Załaduj polecenia cmdlet odpowiadające danemu profilowi usługi.

### [Wysyłanie opinii](Send-Feedback.md)
Wysyła opinię do zespołu programu Azure PowerShell za pomocą zestawu interakcyjnych wskazówek.

### [Set-AzContext](Set-AzContext.md)
Ustawia dzierżawę, abonament i środowisko dla poleceń cmdlet, które mają być używane w bieżącej sesji.

### [Set-AzDefault](Set-AzDefault.md)
Ustawia wartość domyślną w bieżącym kontekście

### [Set-AzEnvironment](Set-AzEnvironment.md)
Ustawia właściwości dla środowiska platformy Azure.

### [Odinstalowywanie — AzureRm](Uninstall-AzureRm.md)
Usuwa wszystkie moduły AzureRm z komputera.

