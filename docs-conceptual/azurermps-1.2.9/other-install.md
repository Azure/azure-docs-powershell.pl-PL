---
title: Inne metody instalacji programu Azure PowerShell | Microsoft Docs
description: Informacje dotyczące instalacji programu Azure PowerShell za pomocą pakietu MSI lub Instalatora platformy sieci Web.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 0d6129fae45d16c414668be68ed377c9241f5330
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/25/2018
ms.locfileid: "50000967"
---
# <a name="other-installation-methods"></a>Inne metody instalacji

Program Azure PowerShell można zainstalować na wiele sposobów. Preferowaną metodą jest użycie modułu PowerShellGet z galerią programu PowerShell. Program Azure PowerShell można zainstalować w systemie Windows za pomocą Instalatora platformy internetowej (WebPI) lub pliku MSI dostępnego w witrynie GitHub.
 
## <a name="install-on-windows-using-the-web-platform-installer"></a>Instalowanie w systemie Windows za pomocą Instalatora platformy internetowej

Instalowanie najnowszej wersji programu Azure PowerShell przy użyciu pakietu WebPI odbywa się tak samo jak w przypadku wcześniejszych wersji.
Pobierz [pakiet WebPI programu Azure PowerShell](http://aka.ms/webpi-azps) i uruchom instalację.

> [!NOTE]
> Jeśli wcześniej zainstalowano moduły platformy Azure z Galerii programu PowerShell, instalator automatycznie je usuwa. Pozwala to uprościć środowisko, w którym jest zainstalowana tylko jedna wersja programu Azure PowerShell. Występują jednak scenariusze, które wymagają zainstalowania wielu wersji.
>
> Moduły z Galerii programu PowerShell są instalowane w folderze `$env:ProgramFiles\WindowsPowerShell\Modules`. Z kolei instalator pakietu WebPI instaluje moduły platformy Azure w folderze `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Jeśli podczas instalacji wystąpi błąd, można ręcznie usunąć foldery Azure`$env:ProgramFiles\WindowsPowerShell\Modules` z folderu \*, a następnie ponowić próbę instalacji.

Po zakończeniu instalacji ustawienie `$env:PSModulePath` powinno obejmować katalogi zawierające polecenia cmdlet programu Azure PowerShell. Poprawność instalacji programu Azure PowerShell można sprawdzić za pomocą następującego polecenia.

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> W przypadku instalacji przy użyciu pakietu WebPI może wystąpić znany problem. Jeśli komputer wymaga ponownego uruchomienia ze względu na aktualizacje systemu lub inne instalacje, aktualizacje środowiska `$env:PSModulePath` mogą nie uwzględnić ścieżki, w której jest zainstalowany program Azure PowerShell.

Podczas próby załadowania lub wykonania poleceń cmdlet po instalacji może pojawić się następujący komunikat o błędzie:

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Problem ten można rozwiązać przez ponowne uruchomienie komputera lub zaimportowanie modułu przy użyciu w pełni kwalifikowanej ścieżki. Na przykład:

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Instalowanie w systemie Windows za pomocą pakietu MSI

Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Jeśli są zainstalowane wcześniejsze wersje modułów platformy Azure, instalator automatycznie je usuwa. Pakiet MSI instaluje moduły w katalogu `$env:ProgramFiles\WindowsPowerShell\Modules`, ale nie tworzy folderów odpowiadających poszczególnym wersjom.

