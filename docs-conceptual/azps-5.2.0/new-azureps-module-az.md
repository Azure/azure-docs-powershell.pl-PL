---
title: Wprowadzenie do modułu Az programu Azure PowerShell
description: Przedstawiamy moduł Az programu PowerShell zalecany do współpracy z platformą Azure i zastąpienia modułu AzureRM programu PowerShell.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 9021a1d8fdc73aedb87b17631f8e67cb8ef79166
ms.sourcegitcommit: a6d92493a8d1b81b85f4db2a38f271134be5e6c5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/12/2020
ms.locfileid: "97353856"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Wprowadzenie do modułu Az programu Azure PowerShell

## <a name="overview"></a>Omówienie

Moduł Az programu PowerShell to zbiór poleceń cmdlet umożliwiających zarządzanie zasobami platformy Azure bezpośrednio z poziomu programu PowerShell. Program PowerShell zapewnia zaawansowane funkcje automatyzacji, które można wykorzystać do zarządzania zasobami platformy Azure na potrzeby przykładów w kontekście potoku ciągłej integracji/ciągłego wdrażania.

Moduł Az programu PowerShell zastępuje moduł AzureRM i jest zalecaną wersją do współpracy z platformą Azure.

Możesz użyć modułu Az programu PowerShell przy użyciu jednej z następujących metod:

* [Instalowanie modułu Az programu PowerShell za pośrednictwem modułu PowerShellGet](install-az-ps.md) (zalecana opcja).
* [Odinstalowywanie modułu Az programu PowerShell za pomocą pliku MSI](install-az-ps-msi.md).
* [Używanie programu Azure Cloud Shell](/azure/cloud-shell/overview).
* [Używanie modułu Az programu PowerShell w kontenerze platformy Docker](azureps-in-docker.md).

## <a name="features"></a>Funkcje

Moduł Az programu PowerShell oferuje następujące korzyści:

* Bezpieczeństwo i stabilność
  * Szyfrowanie pamięci podręcznej tokenów
  * Zapobieganie atakom typu man-in-the-middle
  * Obsługa uwierzytelniania za pomocą usługi ADFS 2019
  * Uwierzytelnianie za pomocą nazwy użytkownika i hasła w programie PowerShell 7
  * Obsługa funkcji, takich jak ciągła weryfikacja dostępu (dostępna w 2021 r.)
* Obsługa wszystkich usług platformy Azure
  * Wszystkie ogólnie dostępne usługi platformy Azure mają odpowiadający im obsługiwany moduł programu PowerShell
  * Wiele poprawek usterek i uaktualnień wersji interfejsu API od czasu modułu AzureRM
* Nowe możliwości
  * Obsługa w usłudze Cloud Shell i na wielu platformach
  * Możliwość uzyskania token dostępu i używania go w celu uzyskiwania dostępu do zasobów platformy Azure
  * Dostępne polecenie cmdlet do zaawansowanych operacji REST dla zasobów platformy Azure

> [!NOTE]
> Program PowerShell w wersji 7 lub nowszej jest zalecaną wersją programu PowerShell do używania z modułem Az programu PowerShell na wszystkich platformach.

Moduł Az programu PowerShell jest oparty na bibliotece .NET Standard i współpracuje z programem PowerShell 7 lub nowszym na wszystkich platformach, w tym w systemach Windows, macOS i Linux. Jest on również zgodny z programem Windows PowerShell 5.1.

Dążymy do tego, aby pomoc techniczna platformy Azure była możliwa na wszystkich platformach, a wszystkie moduły Az programu PowerShell obsługiwane na wielu platformach.

## <a name="upgrade-your-environment-to-az"></a>Uaktualnienie środowiska do modułu Az

Aby być na bieżąco z najnowszymi funkcjami platformy Azure w programie PowerShell, przeprowadź migrację do modułu Az. Jeśli Twoje środowisko nie jest gotowe do zainstalowania modułu Az w celu zastąpienia modułu AzureRM, dostępnych jest kilka opcji umożliwiających eksperymentowanie z modułem Az:

* Korzystaj ze środowiska `PowerShell` w usłudze [Azure Cloud Shell](/azure/cloud-shell/overview). Usługa Azure Cloud Shell to środowisko powłoki oparte na przeglądarce, w którym zainstalowano moduł Az oraz włączono aliasy zapewniające zgodność przy użyciu polecenia cmdlet `Enable-AzureRM`.
* Pozostaw moduł AzureRM zainstalowany w programie Windows PowerShell 5.1 i zainstaluj moduł Az dla programu PowerShell w wersji 7 lub nowszej. Programy Windows PowerShell 5.1 i PowerShell 7 lub nowsze korzystają z oddzielnych kolekcji modułów. Postępuj zgodnie z instrukcjami, aby zainstalować [najnowszą wersję programu PowerShell](/powershell/scripting/install/installing-powershell), a następnie [zainstaluj moduł Az](install-az-ps.md) z programu PowerShell 7 lub nowszego.

Aby uaktualnić istniejącą instalację modułu AzureRM:

1. [Odinstaluj moduł AzureRM programu Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [Zainstaluj moduł Az programu Azure PowerShell](install-az-ps.md)
1. **OPCJONALNIE**: Za pomocą polecenia [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) włącz tryb zgodności, aby dodać aliasy dla poleceń cmdlet modułu AzureRM na czas zapoznawania się z nowym zestawem poleceń. Aby uzyskać więcej informacji, zobacz następną sekcję lub zapoznaj się z tematem [Rozpoczynanie migracji z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Migrowanie istniejących skryptów z modułu AzureRM do modułu Az

Jeśli skrypty nadal są oparte na module AzureRM, udostępniamy kilka zasobów ułatwiających migrację:

* [Wprowadzenie do migracji z modułu AzureRM do Az](migrate-from-azurerm-to-az.md)
* [Pełna lista zmian powodujących niezgodność w module Az 1.0.0 względem modułu AzureRM](migrate-az-1.0.0.md)
* Polecenie cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

## <a name="supportability"></a>Możliwości obsługi

Moduł Az to najnowszy moduł programu PowerShell dla platformy Azure. Problemy lub żądania funkcji można rejestrować bezpośrednio w [repozytorium GitHub](https://github.com/Azure/azure-powershell) lub za pośrednictwem pomocy technicznej firmy Microsoft, jeśli masz umowę pomocy technicznej. Żądania funkcji zostaną zaimplementowane w najnowszej wersji modułu Az. Krytyczne problemy zostaną zaimplementowane w dwóch najnowszych wersjach modułu Az.

W module AzureRM nie będą już wprowadzane nowe polecenia cmdlet ani funkcje. Jednak moduł AzureRM jest nadal oficjalnie obsługiwany i będzie otrzymywać krytyczne poprawki do lutego 2021 r.

## <a name="data-collection"></a>Zbieranie danych

Domyślnie program Azure PowerShell zbiera dane telemetryczne. Firma Microsoft agreguje zebrane dane, aby wykrywać wzorce użycia i typowe problemy oraz usprawnić środowisko Azure PowerShell.
Program Microsoft Azure PowerShell nie zbiera żadnych danych osobowych ani prywatnych. Na przykład dane użycia pomagają identyfikować problemy, takie jak polecenia cmdlet, które nie powiodły się, i ułatwiają określanie priorytetów naszej pracy.

Doceniamy szczegółowe informacje, jakie są udostępniane przez te dane, ale rozumiemy również, że nie każdy chce wysyłać dane dotyczące użycia. Zbieranie danych można wyłączyć za pomocą polecenia cmdlet [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection). Aby dowiedzieć się więcej, przeczytaj nasze [zasady zachowania poufności informacji](https://privacy.microsoft.com/privacystatement).
