---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: c4f2bbd4bc9e2989549304493481f56cbbf5280a
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882197"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Instalowanie programu Azure PowerShell w systemie macOS lub Linux

W przypadku platform innych niż Windows program Azure PowerShell można uruchomić w programie PowerShell Core w wersji 6. Ta wersja programu PowerShell jest przeznaczona do użycia na każdej platformie, która obsługuje platformę .NET Core. W przypadku pracy z tymi platformami jest dostępna wersja programu Azure PowerShell obsługująca wersję platformy .NET Standard.

> [!NOTE]
> Obecnie program Azure PowerShell dla platformy .NET Standard nadal jest w wersji beta.
> Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.
>
> * [Problemy z programem Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Instalowanie programu PowerShell Core

Instrukcje dotyczące instalacji programu PowerShell Core różnią się w przypadku systemu macOS i większości dystrybucji systemu Linux.
Szczegółowe instrukcje można znaleźć w następujących artykułach:

* [Instalowanie programu PowerShell Core w systemie macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Instalowanie programu PowerShell Core w systemie Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>Instalowanie programu Azure PowerShell dla platformy .NET Standard

> [!IMPORTANT]
> Moduł `AzureRM` szczegółowo opisany w innych artykułach nie współpracuje z programem PowerShell Core.
> Należy zainstalować moduł `Az`, aby uzyskać dostęp do funkcji Azure PowerShell w programie PowerShell Core.

Program PowerShell Core jest dostarczany z już zainstalowanym modułem PowerShellGet. Uruchom program PowerShell przy użyciu następującego polecenia:

```bash
pwsh
```

Aby zainstalować program Azure PowerShell, uruchom następujące polecenie:

```powershell
Install-Module Az
```

> [!NOTE]
> Jeśli podczas próby zainstalowania modułu wystąpi błąd uprawnień, być może trzeba będzie uruchomić program PowerShell w trybie administratora, aby zainstalować moduły.
>
> ```bash
> sudo pwsh
> ```

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.

## <a name="enable-aliases"></a>Włączanie aliasów

W celu zachowania zgodności z istniejącym modułem `AzureRM` nowy moduł `Az` może tworzyć aliasy zgodne z poprzednimi wersjami dla poleceń cmdlet `AzureRM`. Przed rozpoczęciem korzystania z modułu po raz pierwszy należy ustawić te aliasy za pomocą następującego polecenia:

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

Spowoduje to skonfigurowanie aliasów tylko dla bieżącego użytkownika. Sprawdź w pomocy dotyczącej poleceń cmdlet informacje na temat innych wartości, które można przekazać do opcji `-Scope` w celu skonfigurowania aliasów.

> [!NOTE]
> Jeśli wystąpi błąd związany z lokalizacją ścieżki, upewnij się, czy istnieje ona w systemie lokalnym. W przypadku zakresu `CurrentUser` ten błąd można naprawić, uruchamiając następujące polecenie w narzędziu `bash`:
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>Logowanie

Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `Az` w sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure. Zaimportowanie modułu __nie__ wymaga podwyższonego poziomu uprawnień.

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Automatyczne zaimportowanie modułu `Az` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).
W systemach macOS i Linux należy pracować z profilem, używając zmiennej środowiskowej `$Profile`. Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="next-steps"></a>Następne kroki

Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).
