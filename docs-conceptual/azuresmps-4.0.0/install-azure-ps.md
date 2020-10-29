---
title: Instalowanie i konfigurowanie modułu zarządzania usługami programu Azure PowerShell | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2860d5c7642b137c1cb14a38fa13d59ec2a4123c
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523210"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Instalowanie modułu zarządzania usługami programu Azure PowerShell

Instalowanie programu Azure PowerShell z [Galerii programu PowerShell](https://www.powershellgallery.com/) jest preferowaną metodą instalacji.

## <a name="step-1-install-powershellget"></a>Krok 1. Zainstaluj moduł PowerShellGet

Instalowanie elementów z Galerii programu PowerShell wymaga modułu PowerShellGet. Upewnij się, że masz odpowiednią wersję modułu PowerShellGet oraz spełnione inne wymagania systemowe. Uruchom następujące polecenie, aby sprawdzić, czy w Twoim systemie został zainstalowany moduł PowerShellGet.

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Jeśli nie masz zainstalowanego modułu PowerShellGet, zobacz sekcję [Jak uzyskać moduł PowerShellGet](#how-to-get-powershellget).

## <a name="step-2-install-azure-powershell"></a>Krok 2. Zainstaluj program Azure PowerShell

Uruchom następujące polecenie z poziomu konsoli programu Windows PowerShell jako administrator:

```powershell
Install-Module Azure
```

Moduł Azure to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager. Po zainstalowaniu modułu AzureRM każdy moduł platformy Azure, który nie został wcześniej zainstalowany, zostanie pobrany i zainstalowany z Galerii programu PowerShell.

Moduł zarządzania usługami platformy Azure udostępnia zależności z modułami usługi Azure PowerShell Resource Manager. Jeśli masz zainstalowane moduły usługi Azure PowerShell Resource Manager, musisz dodać parametr `-AllowClobber` do polecenia instalacji. Umożliwi to aktualizowanie istniejących udostępnionych zależności. Bez tego parametru nie można zainstalować modułu.

```powershell
Install-Module Azure -AllowClobber
```

Po zainstalowaniu tego modułu należy zaimportować moduł za pomocą następującego polecenia:

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>Aby korzystać z poleceń cmdlet

Aby rozpocząć pracę z poleceniami cmdlet zarządzania usługami platformy Azure, najpierw zaloguj się do konta platformy Azure. Aby zalogować się do konta, uruchom następujące polecenie:

```powershell
Add-AzureAccount
```

Gdy zalogujesz się do platformy Azure, program Azure PowerShell utworzy kontekst dla danej sesji. Ten kontekst zawiera środowisko, konto, dzierżawę i subskrypcję programu Azure PowerShell, które będą używane dla wszystkich poleceń cmdlet w tej sesji. Teraz możesz używać poniższych modułów.

## <a name="azure-service-management-cmdlets"></a>Polecenia cmdlet zarządzania usługami platformy Azure

Moduły programu Azure PowerShell są często aktualizowane. Jeśli zauważysz, że pomoc online do polecenia cmdlet zawiera polecenia cmdlet lub parametry, których nie ma w module, pobierz i zainstaluj najnowszą wersję modułu. Aby znaleźć wersji modułu, wpisz: `(Get-InstalledModule Azure).Version`.

Przykładowe skrypty, które mogą pomóc zautomatyzować niektóre typowe zadania na platformie Azure, można znaleźć w temacie [Centrum skryptów Microsoft Azure](http://www.windowsazure.com/documentation/scripts/).

Ogólne informacje na temat instalowania, używania i dostosowywania środowiska programu Windows PowerShell oraz powiązanych szkoleń można znaleźć w temacie [Scripting with Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction) (Obsługa skryptów w programie Windows PowerShell).

### <a name="how-to-get-powershellget"></a>Jak uzyskać moduł PowerShellGet

|Wersja systemu operacyjnego|Instrukcje dotyczące instalacji|
|---|---|
|Mam system Windows 10 lub Windows Server 2016|Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym|
|Chcę przeprowadzić uaktualnienie do programu PowerShell 5|[Zainstaluj najnowszą wersję platformy WMF](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a>Sprawdzanie wersji programu Azure PowerShell

Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane. Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-InstalledModule Azure` z wiersza polecenia.

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
