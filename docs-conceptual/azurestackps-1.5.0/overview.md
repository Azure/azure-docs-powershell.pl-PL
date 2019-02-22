---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153903"
---
# <a name="azure-stack-module-150"></a>Moduł usługi Azure Stack w wersji 1.5.0

## <a name="requirements"></a>Wymagania:
Minimalna obsługiwana wersja usługi Azure Stack to 1808.

Uwaga: Jeśli używasz starszej wersji, zainstaluj wersję 1.4.0

## <a name="known-issues"></a>Znane problemy:

- Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym. Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.
- Nie można usunąć puli adresów IP bez ponownego wdrożenia.

## <a name="install"></a>Instalowanie
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a>Informacje o wersji
* Wszystkie moduły administratora usługi Azure Stack zostały zaktualizowane pod kątem uzyskania takiej samej lub większej zależności od modułu AzureRm.Profile
* Obsługa zarządzania nazwami zasobów zagnieżdżonych we wszystkich modułach
* We wszystkich modułach naprawiono usterkę polegającą na tym, że element ErrorActionPreference jest zastępowany w celu zatrzymania
* Moduł Azs.Compute.Admin
    * Dodano nowe właściwości limitu przydziału na potrzeby obsługi dysku zarządzanego
    * Dodano polecenia cmdlet powiązane z migracją dysku
    * Dodatkowe właściwości w obiektach rozszerzeń maszyny wirtualnej i obrazu platformy
* Azs.Fabric.Admin 
    * Nowe polecenie cmdlet umożliwiające dodawanie węzła jednostki skalowania
* Azs.Backup.Admin
    * Polecenie Set-AzsBackupShare jest teraz aliasem polecenia cmdlet Set-AzsBackupConfiguration
    * Polecenie Get-AzsBackupLocation jest teraz aliasem polecenia cmdlet Get-AzsBackupConfiguration
    * Set-AzsBackupConfiguration, parametr BackupShare jest teraz aliasem ścieżki parametru
* Azs.Subscriptions
    * Get-AzsDelegatedProviderOffer, parametr OfferName jest teraz aliasem parametru Offer
* Azs.Subscriptions.Admin
    * Get-AzsDelegatedProviderOffer, parametr OfferName jest teraz aliasem parametru Offer

## <a name="content"></a>Zawartość:
### <a name="azure-bridge"></a>Azure Bridge
Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.

### <a name="backup"></a>Backup
Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:
- Konfigurowanie miejsca przechowywania kopii zapasowych
- Wykonywanie kopii zapasowych
- Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich

### <a name="commerce"></a>Commerce
Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.

### <a name="compute"></a>Wystąpienia obliczeniowe
Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy, dyskami zarządzanymi oraz rozszerzeniami maszyn wirtualnych.

### <a name="fabric"></a>Fabric
Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:
- Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania
- Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną
- Naprawianie węzłów jednostki skalowania
- Ponowne uruchamianie roli infrastruktury
- Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury
- Tworzenie nowych pul adresów IP


### <a name="gallery"></a>Galeria
Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.

### <a name="infrastructure-insights"></a>Infrastructure Insights
Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:
- Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack
- Wyświetlanie alertów i zarządzanie nimi

### <a name="keyvault"></a>KeyVault
Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.

### <a name="network"></a>Sieć
Wersja zapoznawcza modułu administratora Network, który pozwala na:
- Zarządzanie limitami przydziału sieci
- Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia
- Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora

### <a name="storage"></a>Magazyn
Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.  W tej wersji udostępniamy następujące funkcje:
- Zarządzanie limitami przydziału magazynu
- Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu
- Przywracanie usuniętych kont magazynu
- Migrowanie kontenerów między udziałami
- Wyświetlanie informacji o pojedynczych składnikach magazynu
- Wyświetlanie informacji dotyczących użycia i wydajności

### <a name="subscription-admin"></a>Subscription (administrator)
Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.  Ten moduł udostępnia administratorom następujące funkcje:
- Zarządzanie planami i ofertami
- Wyświetlanie informacji dotyczących użycia i wydajności
- Zarządzanie kontrolą dostępu opartą na rolach

### <a name="subscription"></a>Subskrypcja
Wersja zapoznawcza modułu Subscription usługi Azure Stack.  Ten moduł udostępnia użytkownikom następujące funkcje:
- Tworzenie, usuwanie i aktualizowanie subskrypcji

### <a name="update"></a>Aktualizacja
Wersja zapoznawcza modułu administratora Update usługi Azure Stack.  W tym module administratorzy mogą wykonywać następujące czynności:
- Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich
- Wznawianie przerwanych aktualizacji
- Wyświetlanie zainstalowanych aktualizacji
