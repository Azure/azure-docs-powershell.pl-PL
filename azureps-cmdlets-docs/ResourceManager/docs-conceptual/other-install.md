---
title: Inne metody instalacji programu Azure PowerShell | Microsoft Docs
description: "Informacje dotyczące instalacji programu Azure PowerShell za pomocą pakietu MSI lub Instalatora platformy sieci Web."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 368404bcb5218814b4965bb1bcda1e2876441d2a
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/29/2017
---
# <a name="other-installation-methods"></a>Inne metody instalacji

Program Azure PowerShell można zainstalować na wiele sposobów. Preferowaną metodą jest użycie modułu PowerShellGet z galerią programu PowerShell. Program Azure PowerShell można zainstalować za pomocą Instalatora platformy sieci Web (WebPI) lub pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/latest).

## <a name="install-using-the-web-platform-installer"></a>Instalowanie za pomocą Instalatora platformy sieci Web

Instalowanie najnowszej wersji programu Azure PowerShell przy użyciu pakietu WebPI odbywa się tak samo jak w przypadku wcześniejszych wersji.
Pobierz [pakiet WebPI programu Azure PowerShell](http://aka.ms/webpi-azps) i uruchom instalację.

> [!NOTE]
> Jeśli wcześniej zainstalowano moduły platformy Azure z Galerii programu PowerShell, instalator automatycznie je usuwa. Pozwala to uprościć środowisko, w którym jest zainstalowana tylko jedna wersja programu Azure PowerShell. Występują jednak scenariusze, które wymagają zainstalowania wielu wersji.
>
> Moduły z Galerii programu PowerShell są instalowane w folderze `$env:ProgramFiles\WindowsPowerShell\Modules`. Z kolei instalator pakietu WebPI instaluje moduły platformy Azure w folderze `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Jeśli podczas instalacji wystąpi błąd, można ręcznie usunąć foldery Azure* z folderu `$env:ProgramFiles\WindowsPowerShell\Modules`, a następnie ponowić próbę instalacji.

Po zakończeniu instalacji ustawienie `$env:PSModulePath` powinno obejmować katalogi zawierające polecenia cmdlet programu Azure PowerShell. Poprawność instalacji programu Azure PowerShell można sprawdzić za pomocą następującego polecenia.

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> W przypadku instalacji przy użyciu pakietu WebPI może wystąpić znany problem. Jeśli komputer wymaga ponownego uruchomienia ze względu na aktualizacje systemu lub inne instalacje, aktualizacje środowiska `$env:PSModulePath` mogą nie uwzględnić ścieżki, w której jest zainstalowany program Azure PowerShell.

Podczas próby załadowania lub wykonania poleceń cmdlet po instalacji może pojawić się następujący komunikat o błędzie:

```
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

## <a name="install-using-the-msi-package"></a>Instalowanie za pomocą pakietu MSI

Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Jeśli są zainstalowane wcześniejsze wersje modułów platformy Azure, instalator automatycznie je usuwa. Pakiet MSI instaluje moduły w katalogu `$env:ProgramFiles\WindowsPowerShell\Modules`, ale nie tworzy folderów odpowiadających poszczególnym wersjom.
