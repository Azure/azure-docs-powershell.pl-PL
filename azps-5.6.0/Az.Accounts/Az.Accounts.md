---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 0c8773066f39d11e6985bbe4bd1f1e69cd9142f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990634"
---
# Moduł Az.Accounts
## Opis
Zarządza poświadczeniami i wspólną konfiguracją dla wszystkich modułów platformy Azure.

## Polecenia cmdlet az.accounts
### [Add-AzEnvironment](Add-AzEnvironment.md)
Dodaje punkty końcowe i metadane dla wystąpienia usługi Azure Resource Manager.

### [Clear-AzContext](Clear-AzContext.md)
Usuń wszystkie poświadczenia platformy Azure, konto i informacje o subskrypcji.

### [Clear-AzDefault](Clear-AzDefault.md)
Wyczyszczenie ustawień domyślnych ustawionych przez użytkownika w bieżącym kontekście.

### [Connect-AzAccount](Connect-AzAccount.md)
Połącz się z platformą Azure przy użyciu uwierzytelnionego konta w celu używania z poleceniami cmdlet z modułów programu Az PowerShell.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Wyłącz automatyczne zapisywanie poświadczeń platformy Azure.  Informacje logowania zostaną zapomniane przy następnym otwarciu okna programu PowerShell

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Zrezygnowano z gromadzenia danych w celu ulepszania poleceń cmdlet programu Azure PowerShell. Domyślnie dane są zbierane, chyba że użytkownik jawnie zrezygnuje.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Wyłącza aliasy prefiksów usługi AzureRm dla modułów az.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Odłącza połączone konto platformy Azure i usuwa wszystkie poświadczenia i konteksty skojarzone z tym kontem.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
Konteksty platformy Azure to obiekty programu PowerShell reprezentujące aktywną subskrypcję, dla których mają być uruchamiane polecenia, oraz informacje o uwierzytelnianiu potrzebne do nawiązania połączenia z chmurą platformy Azure. W kontekście platformy Azure program Azure PowerShell nie musi ponownie uwierzytelniania konta przy każdym przełączaniu subskrypcji. Aby uzyskać więcej informacji, zobacz [obiekty kontekstowe programu Azure PowerShell.](https://docs.microsoft.com/powershell/azure/context-persistence)

To polecenie cmdlet umożliwia zapisanie i automatyczne załadowanie informacji kontekstowych platformy Azure po uruchomieniu procesu programu PowerShell. Na przykład podczas otwierania nowego okna.

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Umożliwia programowi Azure PowerShell zbieranie danych w celu poprawy środowiska użytkownika za pomocą poleceń cmdlet programu Azure PowerShell. Wykonanie tego polecenia cmdlet wybiera opcję zbierania danych dla bieżącego użytkownika na bieżącym komputerze. Domyślnie dane są zbierane, chyba że użytkownik jawnie zrezygnuje.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Włącza aliasy prefiksów usługi AzureRm dla modułów az.

### [Get-AzAccessToken](Get-AzAccessToken.md)
Pobierz nieprzetworzone token dostępu. Podczas korzystania z funkcji -ResourceUrl upewnij się, że wartość jest dopasowana do bieżącego środowiska platformy Azure. Możesz odwołać się do wartości `(Get-AzContext).Environment` .

### [Get-AzContext](Get-AzContext.md)
Pobiera metadane używane do uwierzytelniania żądań usługi Azure Resource Manager.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
Wyświetl metadane dotyczące funkcji autozazysowania kontekstu, w tym informacje o tym, czy kontekst jest zapisywany automatycznie, oraz gdzie można znaleźć zapisane informacje kontekstowe i poświadczenia.

### [Get-AzDefault](Get-AzDefault.md)
Pobierz ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Uzyskaj punkty końcowe i metadane dla wystąpienia usług platformy Azure.

### [Get-AzSubscription](Get-AzSubscription.md)
Uzyskaj subskrypcje dostępne dla bieżącego konta.

### [Get-AzTenant](Get-AzTenant.md)
Pobiera dzierżawy autoryzowane dla bieżącego użytkownika.

### [Import-AzContext](Import-AzContext.md)
Ładowanie informacji uwierzytelniania platformy Azure z pliku.

### [Invoke-AzRestMethod](Invoke-AzRestMethod.md)
Konstruowanie i wykonywanie żądania HTTP tylko do punktu końcowego zarządzania zasobami platformy Azure

### [Register-AzModule](Register-AzModule.md)
TYLKO DO UŻYTKU WEWNĘTRZNEGO — zapewnianie obsługi środowiska uruchomieniowego dla polecenia cmdlet wygenerowanego przez autorest

### [Remove-AzContext](Remove-AzContext.md)
Usuwanie kontekstu z zestawu dostępnych kontekstów

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Usuwa punkty końcowe i metadane na celu połączenie się z danym wystąpieniem platformy Azure.

### [Rename-AzContext](Rename-AzContext.md)
Zmień nazwę kontekstu platformy Azure.  Domyślnie konteksty są nazwane według konta użytkownika i subskrypcji.

### [Resolve-AzError](Resolve-AzError.md)
Wyświetlanie szczegółowych informacji o błędach programu PowerShell z rozszerzonymi szczegółami błędów programu Azure PowerShell.

### [Save-AzContext](Save-AzContext.md)
Zapisuje bieżące informacje o uwierzytelnieniu do użycia w innych sesjach programu PowerShell.

### [Select-AzContext](Select-AzContext.md)
Wybieranie subskrypcji i konta do kierowania w poleceniach cmdlet programu Azure PowerShell

### [Wyślij opinię](Send-Feedback.md)
Wysyła opinie do zespołu programu Azure PowerShell za pomocą zestawu podpowiedzi.

### [Set-AzContext](Set-AzContext.md)
Ustawia dzierżawę, subskrypcję i środowisko, z których będą korzystać polecenia cmdlet w bieżącej sesji.

### [Set-AzDefault](Set-AzDefault.md)
Ustawia wartość domyślną w bieżącym kontekście

### [Set-AzEnvironment](Set-AzEnvironment.md)
Ustawia właściwości środowiska platformy Azure.

### [Uninstall-AzureRm](Uninstall-AzureRm.md)
Usuwa wszystkie moduły usługi AzureRm z komputera.

