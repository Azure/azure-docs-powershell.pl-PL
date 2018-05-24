---
title: Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia w systemach macOS i Linux.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 7228ca9791f174cb3554dd359b3723e98589ee17
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux

Teraz jest możliwa instalacja programów PowerShell Core w wersji 6 i Azure PowerShell na platformach innych niż Windows.
Proces instalowania programu Azure PowerShell w systemach macOS i Linux nie różni się zbytnio od instalowania w systemie Windows, należy jednak najpierw zainstalować program PowerShell Core w wersji 6.

> [!NOTE]

> W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.
> Wsparcie dla tych produktów jest ograniczone. Jeśli napotkasz problemy lub odkryjesz usterkę, zarejestruj problemy w witrynie GitHub.
>
> * [Problemy z programem PowerShell Core w wersji 6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemy z programem Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>Krok 1. Instalowanie programu PowerShell Core w wersji 6

Proces instalowania programu PowerShell Core w wersji 6 różni się zależnie od docelowego systemu operacyjnego.
Chociaż istnieje możliwość zainstalowania programu PowerShell Core w wersji 6 w systemie Windows, ten artykuł koncentruje się na systemach macOS i Linux. Jeśli chcesz korzystać z programu Azure PowerShell w systemie Windows, zobacz artykuł poświęcony [instalacji](./install-azurerm-ps.md) w systemie Windows.

Proces instalowania programu **PowerShell Core w wersji 6** w systemie Linux lub macOS różni się zależnie od dystrybucji systemu Linux i wersji systemu operacyjnego.
Szczegółowe instrukcje można znaleźć w następującym artykule:

- [Instalowanie programu PowerShell Core w systemach macOS i Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>Krok 2. Instalowanie programu Azure PowerShell dla platformy .NET Core

Program PowerShell Core w wersji 6 jest dostarczany z już zainstalowanym modułem PowerShellGet. Ułatwia to instalację modułów opublikowanych w galerii programu PowerShell. Aby zainstalować program Azure PowerShell, otwórz nową sesję programu PowerShell i uruchom następujące polecenie:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>Krok 3. Ładowanie modułu AzureRM.Netcore

Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell. Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Po zakończeniu importowania można przetestować nowo zainstalowany moduł, próbując zalogować się do platformy Azure przy użyciu następującego polecenia:

```powershell
Connect-AzureRmAccount
```

Powyższe polecenie powinno poprosić o przejście na stronę `https://aka.ms/devicelogin` i wprowadzenie udostępnionego kodu.

## <a name="available-cmdlets"></a>Dostępne polecenia cmdlet

Moduły programu Azure PowerShell dla platformy .NET Standard są ciągle w fazie opracowywania. Nie oferują one pełnego zestawu poleceń cmdlet dostępnych w modułach w wersji dla systemu Windows. Następujące funkcje są implementowane w modułach AzureRM.Netcore:

* Zarządzanie kontami
  - Logowanie się przy użyciu konta Microsoft, konta organizacji lub jednostki usługi za pośrednictwem usługi Microsoft Azure Active Directory
  - Zapisywanie poświadczeń na dysku poleceniem Save-AzureRmContext i ładowanie zapisanych poświadczeń poleceniem Import-AzureRmContext
* Środowisko
  - Pobieranie różnych gotowych środowisk platformy Microsoft Azure
  - Dodawanie/ustawianie/usuwanie dostosowanych środowisk (takich jak środowiska Azure Stack lub Windows Azure Pack)
* Polecenia cmdlet płaszczyzny zarządzania dla usług platformy Azure korzystających z interfejsów menedżera zasobów i zarządzania usługami.
  - Maszyna wirtualna
  - App Service (Websites)
  - SQL Database
  - Magazyn
  - Sieć

## <a name="next-steps"></a>Następne kroki

Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).
