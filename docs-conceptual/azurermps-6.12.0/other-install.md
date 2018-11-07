---
title: Inne metody instalacji programu Azure PowerShell
description: Jak zainstalować program Azure PowerShell bez modułu PowerShellGet za pomocą instalatora MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 9fa5790e0a2aca4f933b40256634f772c258b189
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212869"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Instalowanie programu Azure PowerShell w systemie Windows za pomocą instalatora MSI

W tym artykule opisano sposób instalowania programu Azure PowerShell w systemie Windows przy użyciu instalatora MSI.  
Tych metod instalacji należy używać tylko wtedy, gdy są one niezbędne w danym systemie. Zalecaną metodą instalacji programu Azure PowerShell w systemie Windows jest moduł PowerShellGet. Aby uzyskać instrukcje dotyczące instalowania programu Azure PowerShell przy użyciu modułu PowerShellGet, zobacz [Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet](install-azurerm-ps.md).

> [!NOTE]
> Instalacja za pomocą Instalatora platformy internetowej nie jest już dostępna dla programu Azure PowerShell w wersji 6.x lub nowszej. Jeśli jest wymagane użycie Instalatora platformy internetowej, rozważ użycie zamiast niego instalatora MSI lub zainstaluj starszą wersję programu Azure PowerShell.

Aby zainstalować w środowiskach Linux lub macOS, zobacz [Instalowanie programu Azure PowerShell w systemie macOS lub Linux](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Instalowanie lub aktualizowanie w systemie Windows za pomocą pakietu MSI

Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Jeśli zainstalowano wcześniejsze wersje modułów platformy Azure za pomocą pakietu MSI, instalator automatycznie je usuwa. Pakiet MSI instaluje moduły w lokalizacji `${env:ProgramFiles}\WindowsPowerShell\Modules`. Zostaną zainstalowane moduły `AzureRM` i `Azure`.

> [!NOTE]
> Używaj modułu `Azure` tylko wtedy, gdy pracujesz z klasycznym modelem wdrażania platformy Azure.

Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `AzureRM` w bieżącej sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Automatyczne zaimportowanie modułu `AzureRM` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).
Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).
