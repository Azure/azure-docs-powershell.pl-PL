---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574502"
---
# <a name="install-azure-powershell-with-powershellget"></a>Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet

W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu PowerShellGet. W przypadku wersji zapoznawczej modułu Az inne metody instalacji nie są obsługiwane. 

## <a name="requirements"></a>Wymagania

Program Azure PowerShell działa z programem PowerShell 5.x w systemie Windows lub z programem PowerShell 6.x na dowolnej platformie. Aby sprawdzić wersję programu PowerShell na maszynie, uruchom następujące polecenie:

```powershell-interactive
$PSVersionTable.PSVersion
```

Jeśli masz nieaktualną wersją lub musisz zainstalować program PowerShell, zobacz [Instalowanie różnych wersji programu PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6). Ta strona zawiera linki do informacji o instalacji dla określonych platform.

## <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

> [!IMPORTANT]
>
> Moduły `AzureRM` i `Az` nie powinny być zainstalowane w systemie jednocześnie. Aby można było zainstalować moduł `Az`, należy odinstalować moduł `AzureRM`. Aby uzyskać instrukcje, jak to zrobić, zobacz [Odinstalowywanie modułu programu Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).

Aby zainstalować moduły w zakresie globalnym, wymagany jest podwyższony poziom uprawnień w celu zainstalowania modułów z galerii programu PowerShell. Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień (opcja „Uruchom jako Administrator” w systemie Windows lub z uprawnieniami superużytkownika w systemie macOS lub Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Jeśli nie masz dostępu do uprawnień administratora, możesz przeprowadzić instalację dla bieżącego użytkownika, dodając argument `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.

Moduł `Az` to zbiorczy moduł poleceń cmdlet programu Azure PowerShell. Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.

## <a name="sign-in"></a>Logowanie

Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `Az` w bieżącej sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Automatyczne zaimportowanie modułu `Az` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).
Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualizowanie modułu programu Azure PowerShell

Możesz zaktualizować instalację programu Azure PowerShell przez uruchomienie polecenia [Update-Module](/powershell/module/powershellget/update-module). To polecenie __nie__ powoduje odinstalowania wcześniejszych wersji.

```powershell-interactive
Update-Module -Name Az
```

Jeśli chcesz usunąć starsze wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Korzystanie z wielu wersji programu Azure PowerShell

Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell. Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).

Możesz załadować określoną wersję modułu `Az`, używając argumentu `-RequiredVersion` w poleceniu `Install-Module` lub `Import-Module`:

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Jeśli masz zainstalowaną więcej niż jedną wersję modułu, podczas importowania domyślnie jest ładowana najnowsza wersja.

## <a name="provide-feedback"></a>Przekazywanie opinii

Jeśli znajdziesz błąd podczas korzystania z programu Azure Powershell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).
Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).

## <a name="next-steps"></a>Następne kroki

Aby zacząć korzystać z programu Azure PowerShell i dowiedzieć się więcej o module i jego funkcjach, zobacz [Rozpoczęcie korzystania z programu Azure PowerShell](get-started-azureps.md).