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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882507"
---
# <a name="azure-stack-module-130"></a>Moduł usługi Azure Stack w wersji 1.3.0

## <a name="requirements"></a>Wymagania:
Minimalna obsługiwana wersja usługi Azure Stack to 1804.

Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11

## <a name="known-issues"></a>Znane problemy:

- Alert dotyczący zamknięcia wymaga usługi Azure Stack w wersji 1803.
- Niektóre polecenia cmdlet modułu Storage wymagają usługi Azure Stack w wersji 1804.
- Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym. Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.
- Nie można usunąć puli adresów IP bez ponownego wdrożenia.

## <a name="breaking-changes"></a>Zmiany powodujące niezgodność
Wszystkie zmiany powodujące niezgodność spowodowane migracją z wersji 1.2.11 są udokumentowane tutaj: https://aka.ms/azspowershellmigration

## <a name="install"></a>Instalowanie
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
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
Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy oraz rozszerzeniami maszyn wirtualnych.

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
