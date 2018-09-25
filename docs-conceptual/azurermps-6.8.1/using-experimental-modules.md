---
title: Korzystanie z eksperymentalnych modułów programu Azure PowerShell
description: Wyjaśnienie filozofii i zasad użycia eksperymentalnych modułów programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: cb1c49682ea1bfd5fa43baafe4cb0f7fc0c46020
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300803"
---
# <a name="use-experimental-azure-powershell-modules"></a>Korzystanie z eksperymentalnych modułów programu Azure PowerShell

Zespół programu Azure PowerShell eksperymentuje z wieloma udoskonaleniami w zakresie korzystania z tego programu, ze szczególnym uwzględnieniem narzędzi dla deweloperów (w szczególności interfejsów wiersza polecenia).

## <a name="experimentation-methodology"></a>Metodologia eksperymentów

Aby ułatwić eksperymenty, tworzymy nowe moduły programu Azure PowerShell, które wdrażają istniejące funkcje zestawu SDK platformy Azure przy użyciu nowych, łatwiejszych w obsłudze sposobów. W większości przypadków polecenia cmdlet dokładnie duplikują istniejące polecenia cmdlet. Jednak eksperymentalne polecenia cmdlet są dostępne ze skróconą notacją i bardziej inteligentnymi wartościami domyślnymi, co ułatwia tworzenie zasobów platformy Azure i zarządzanie nimi.

Te moduły mogą być instalowane obok istniejących modułów programu Azure PowerShell. Nazwy poleceń cmdlet zostały skrócone, aby zmniejszyć ich długość i wyeliminować konflikty z istniejącymi poleceniami cmdlet, które nie są eksperymentalne.

W przypadku modułów eksperymentalnych obowiązuje następująca konwencja nazewnictwa: `AzureRM.*.Experiments`. Ta konwencja nazewnictwa przypomina nazewnictwo modułów z wersji zapoznawczej: `AzureRM.*.Preview`. Moduły z wersji zapoznawczej różnią się od modułów eksperymentalnych. Moduły z wersji zapoznawczej wdrażają nowe funkcje usług platformy Azure, które są dostępne tylko w wersji zapoznawczej. Moduły z wersji zapoznawczej zastępują istniejące moduły programu Azure PowerShell i używają tych samych nazw poleceń cmdlet i nazw parametrów.

## <a name="how-to-install-an-experimental-module"></a>Jak zainstalować moduł eksperymentalny

Moduły eksperymentalne są publikowane w galerii programu PowerShell tak samo, jak istniejące moduły programu Azure PowerShell. Aby wyświetlić listę modułów eksperymentalnych, uruchom następujące polecenie:

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

Aby zainstalować moduł eksperymentalny, użyj następujących poleceń w sesji programu PowerShell z podwyższonym poziomem uprawnień:

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>Dokumentacja i pomoc techniczna

Dokumentacja jest zawarta w pakiecie instalacyjnym, a dostęp do niej można uzyskiwać za pomocą polecenia cmdlet `Get-Help`. Dla modułów eksperymentalnych nie jest publikowana oficjalna dokumentacja.

Zachęcamy do testowania tych modułów. Wasze opinie pozwalają nam poprawiać użyteczność i reagować na Wasze potrzeby. Jednak wsparcie dla tych modułów jest ograniczone z uwagi na to, że są to moduły eksperymentalne. Pytania i raporty dotyczące problemów można przekazywać, tworząc [problem](https://github.com/Azure/azure-powershell/issues) w repozytorium GitHub.

## <a name="experiments-and-areas-of-improvement"></a>Eksperymenty i obszary ulepszeń

Te ulepszenia zostały wybrane na podstawie kluczowych różnic w konkurencyjnych produktach. Na przykład w interfejsie wiersza polecenia platformy Azure w wersji 2.0 oparto polecenia na _scenariuszach_, a nie na _obszarze powierzchni interfejsu API_.
W interfejsie wiersza polecenia platformy Azure w wersji 2.0 używana jest pewna liczba domyślnych ustawień inteligentnych, dzięki którym korzystanie ze scenariuszy wprowadzających jest łatwiejsze dla użytkowników.

### <a name="core-improvements"></a>Ulepszenia funkcji podstawowych

Ulepszenia funkcji podstawowych są traktowane jako zdroworozsądkowe, a w celu wdrożenia tych aktualizacji potrzebne jest eksperymentowanie tylko w ograniczonym zakresie.

- Polecenia cmdlet oparte na scenariuszach — **wszystkie* polecenia cmdlet powinny być projektowane wokół scenariuszy, a nie w oparciu o usługę Azure REST.

- Krótsze nazwy — obejmują nazwy poleceń cmdlet (na przykład `New-AzureRmVM` => `New-AzVm`) oraz nazwy parametrów (na przykład `-ResourceGroupName` => `-Rg`). W celu zapewniania zgodności ze „starymi” poleceniami cmdlet należy stosować aliasy. Wymagane jest udostępnianie zestawów parametrów _zgodnych z poprzednimi wersjami_.

- Inteligentne wartości domyślne — inteligentne wartości domyślne należy tworzyć, aby wypełniać „wymagane” informacje. Na przykład:
  - Grupa zasobów
  - Lokalizacja
  - Zasoby zależne

### <a name="experimental-improvements"></a>Ulepszenia eksperymentalne

Ulepszenia eksperymentalne stanowią istotną zmianę, którą zespół chce zweryfikować za pośrednictwem eksperymentów.

- Typy proste — scenariusze tworzenia powinny odbiegać od typów złożonych i obiektów konfiguracji. Konfiguracja powinna być uproszczona i ograniczona do jednego lub dwóch parametrów.

- „Tworzenie inteligentne” — żadne scenariusze tworzenia, które wdrażają „Tworzenie inteligentne”, _nie powinny_ zawierać parametrów wymaganych: wszystkie wymagane informacje powinny być wybierane w programie Azure PowerShell jako opcje.

- Parametry szare — w wielu przypadkach niektóre parametry mogą być „szare” lub półopcjonalne. Jeśli parametr nie jest określony, użytkownik jest pytany, czy chce, aby parametr został dla niego wygenerowany. Dodatkowo warto, aby za zgodą użytkownika parametry szare otrzymywały wartości na podstawie kontekstu.
  Na przykład rozsądne może okazać się, aby parametr szary sugerował wartość, która została użyta jako ostatnia.

- Przełącznik `-Auto` — przełącznik `-Auto` stanowi sposób, dzięki któremu użytkownicy mogą „wybrać opcję” _ustawienia domyślnego dla wszystkich elementów_ z zachowaniem integralności wymaganych parametrów w ścieżce głównej.

### <a name="feature-specific-switches"></a>Przełączniki właściwe dla funkcji

Na przykład scenariusz „Tworzenie aplikacji internetowej” może zawierać przełącznik `-Git` lub `-AddRemote`, który automatycznie dodaje zdalne środowisko platformy „azure” do istniejącego repozytorium Git.

- Wartości domyślne dostępne do konfigurowania — użytkownicy powinni mieć możliwość ustawiania wartości domyślnych dla typowych parametrów, takich jak `-ResourceGroupName` i `-Location`.

- Rozmiary domyślne — „rozmiary” zasobów mogą być mylące dla użytkowników, ponieważ wielu dostawców zasobów używa różnych nazw (na przykład „Standardowa\_DS1\_v2” lub „S1”). Jednak większość użytkowników najbardziej martwi się o koszty. Dlatego warto zdefiniować „uniwersalne” rozmiary oparte na harmonogramie cen. Użytkownicy mogą wybrać konkretny rozmiar albo pozwolić programowi Azure PowerShell wybrać _najlepszą opcję_ w oparciu o budżet na zasoby.

- Format wyjściowy — program Azure PowerShell aktualnie zwraca obiekty `PSObject`, a ilość danych wyjściowych konsoli jest niewielka. Program Azure PowerShell może wymagać wyświetlenia pewnych informacji dla użytkownika w odniesieniu do używanych „domyślnych ustawień inteligentnych”.
