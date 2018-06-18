---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323105"
---
# <a name="install-azure-powershell-with-powershellget"></a>Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet

W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w środowisku systemu Windows przy użyciu modułu PowerShellGet.  Jest to preferowany sposób instalacji programu Azure PowerShell, ale jeśli wolisz go zainstalować za pomocą Instalatora platformy internetowej lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md).

Jeśli chcesz korzystać z programu Azure PowerShell w systemie macOS lub Linux, zobacz następujący artykuł: [Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Wymagania systemowe

Usługa Azure PowerShell w wersji 6.1.0 wymaga programu PowerShell w wersji 5.0 lub nowszej. Aby uzyskać informacje dotyczące uaktualnienia programu PowerShell do wersji 5.0, zobacz [Upgrading existing Windows PowerShell (Uaktualnianie istniejącego programu Windows PowerShell)](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

Moduł PowerShellGet jest automatycznie uwzględniony jako część programu PowerShell 5.0.

## <a name="install-or-update-the-azure-powershell-module"></a>Instalowanie lub aktualizowanie modułu Azure PowerShell

Instalacja programu Azure PowerShell z Galerii programu PowerShell wymaga podniesionych uprawnień. Uruchom następujące polecenie z sesji programu PowerShell z podwyższonym poziomem uprawnień:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> To polecenie zaktualizuje dowolną istniejącą instalację programu Azure PowerShell w Twoim systemie. Jeśli potrzebujesz mieć zainstalowaną więcej niż jedną wersję, zobacz odpowiedź na pytanie [Czy mogę zainstalować wiele wersji programu Azure PowerShell?](#multiple-versions) w sekcji Często zadawane pytania

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Wybierz odpowiedź „Tak” lub „Tak na wszystkie”, aby kontynuować instalację.

> [!NOTE]
> Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.

Moduł AzureRM to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager. Po zainstalowaniu modułu AzureRM każdy moduł programu Azure PowerShell, który nie został wcześniej zainstalowany, zostanie pobrany z Galerii programu PowerShell.

## <a name="load-the-azure-powershell-module"></a>Ładowanie modułu programu Azure PowerShell

Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell. Należy to zrobić w ramach normalnej sesji programu PowerShell (bez podwyższonego poziomu uprawnień). Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Zgłaszanie problemów i przesyłanie opinii

Jeśli napotkasz jakiekolwiek usterki w narzędziu, [prześlij zgłoszenie w witrynie GitHub](https://github.com/Azure/azure-powershell/issues). Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet `Send-Feedback`.

## <a name="next-steps"></a>Następne kroki

Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz następujące artykuły:

* [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Często zadawane pytania

### <a id="helpmechoose"></a>Jak mogę sprawdzić wersję programu Azure PowerShell?

Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane. Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-Module AzureRM` z wiersza polecenia.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>Czy mogę użyć programu Azure PowerShell na potrzeby klasycznych wdrożeń platformy Azure?

Jeśli masz wdrożenia korzystające z klasycznego modelu wdrażania, możesz zainstalować wersję zarządzania usługą programu Azure PowerShell. Aby uzyskać więcej informacji, zobacz [Instalowanie modułu Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps). Moduły Azure i AzureRM mają wspólne zależności. Jeśli korzystasz z modułów Azure i AzureRM, należy zainstalować tę samą wersję każdego pakietu.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>Czy mogę zainstalować wiele wersji programu Azure PowerShell?

Moduł PowerShellGet to jedyna metoda instalacji, która obsługuje wiele wersji. Aby zainstalować wiele wersji, możesz dodać parametr `-RequiredVersion` do polecenia cmdlet `Install-Module`. Na przykład w celu zainstalowania wersji 6.1.0 oraz 1.2.9:

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Tylko jedna wersja modułu może zostać załadowana w sesji programu PowerShell. Musisz otworzyć nowe okno programu PowerShell i użyć polecenia `Import-Module`, aby zaimportować określoną wersję modułu programu Azure PowerShell.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Wersja 2.1.0 i wersja 1.2.6 to pierwsze wersje modułu przeznaczone do instalacji i używania obok siebie. Załadowanie starszej wersji programu Azure PowerShell powoduje załadowanie niezgodnych wersji modułu **AzureRM.Profile**. W wyniku tego każde wykonanie polecenia cmdlet powoduje wyświetlenie polecenia cmdlet z monitem o zalogowanie się.
