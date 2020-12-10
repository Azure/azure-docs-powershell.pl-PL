---
title: Instalowanie programu Azure PowerShell za pomocą pakietu MSI
description: Jak zainstalować program Azure PowerShell bez modułu PowerShellGet za pomocą instalatora MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: de9ac41b86e97c948943d22b2019c8022bdf52e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856718"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Instalowanie programu Azure PowerShell w systemie Windows za pomocą instalatora MSI

W tym artykule opisano sposób instalowania programu Azure PowerShell w systemie Windows przy użyciu instalatora MSI. Instalator MSI jest udostępniany na potrzeby środowisk, w których galeria programu PowerShell może być zablokowana przez zaporę, lub w których wymagany jest instalator w trybie offline. Zalecaną metodą instalacji programu Azure PowerShell jest moduł PowerShellGet. Aby uzyskać instrukcje dotyczące instalowania programu Azure PowerShell przy użyciu modułu PowerShellGet, zobacz [Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet](install-az-ps.md).

## <a name="requirements"></a>Wymagania

Instalator MSI w systemie Windows jest zaprojektowany wyłącznie do instalowania programu Azure PowerShell dla programu PowerShell 5.1. W przypadku instalacji na platformach innych niż Windows lub starszych wersji programu PowerShell, zobacz [Instalowanie za pomocą modułu PowerShellGet](install-az-ps.md). Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:

```powershell-interactive
$PSVersionTable.PSVersion
```

Aby użyć programu Azure PowerShell w programie PowerShell 5.1:

1. Jeśli to konieczne, przeprowadź aktualizację do programu [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell). Jeśli używasz systemu Windows 10, masz już zainstalowany program PowerShell 5.1.
2. Zainstaluj program [.NET Framework 4.7.2 lub nowszy](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Instalowanie lub aktualizowanie w systemie Windows za pomocą pakietu MSI

Pakiet MSI dla programu Azure PowerShell jest dostępny w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases):

1. Przejdź do adresu https://github.com/Azure/azure-powershell/releases.
2. Wyszukaj najnowszy moduł galerii dla programu Azure PowerShell (są one wyświetlane chronologicznie i zwykle są to tylko wersje wydania bez nazwy, np. „4.7.0”).
3. Przewiń na sam dół informacji o poprawce i kliknij strzałkę obok pozycji „Zasoby”, aby wyświetlić opcje pakietu MSI.
4. Kliknij wybrane polecenie Az pakietu MSI, aby rozpocząć pobieranie.

Jeśli wcześniejsze wersje programu Azure PowerShell zainstalowano za pomocą pakietu MSI, instalator automatycznie je usunie. Pakiet MSI instaluje moduły w lokalizacji `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module Az`. Ze względu na strukturę modułu może to potrwać maksymalnie minutę.

Musisz powtórzyć ten krok dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="provide-feedback"></a>Przekazywanie opinii

Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues). Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Następne kroki

Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md). Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).
