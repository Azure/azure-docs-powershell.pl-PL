---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323258"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Instalowanie programu Azure PowerShell w systemie macOS lub Linux

W przypadku platform innych niż Windows program Azure PowerShell można uruchomić, bazując na programie PowerShell Core w wersji 6. W przeciwieństwie do standardowego programu Azure PowerShell utworzonego na podstawie programu .NET Framework dla systemu Windows ten produkt jest utworzony pod kątem platformy .NET Core i może działać na dowolnej platformie, która obsługuje środowisko uruchomieniowe .Net Core.

> [!NOTE]
> W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.
> Wsparcie dla tych produktów jest ograniczone. Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.
>
> * [Problemy z programem PowerShell Core w wersji 6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemy z programem Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>Instalowanie programu PowerShell Core w wersji 6

Proces instalowania programu PowerShell Core w wersji 6 w systemie Linux lub macOS różni się zależnie od dystrybucji systemu Linux i wersji systemu operacyjnego.
Szczegółowe instrukcje można znaleźć w następujących artykułach:

- [Instalowanie programu PowerShell Core w systemie macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [Instalowanie programu PowerShell Core w systemie Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Instalowanie programu Azure PowerShell dla platformy .NET Core

Program PowerShell Core w wersji 6 jest dostarczany z już zainstalowanym modułem PowerShellGet. Ułatwia to instalację modułów opublikowanych w galerii programu PowerShell. Aby zainstalować program Azure PowerShell, otwórz nową sesję programu PowerShell i uruchom następujące polecenie:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>Ładowanie modułu AzureRM.Netcore

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
