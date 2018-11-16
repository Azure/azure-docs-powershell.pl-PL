---
title: Omówienie programu Azure Stack PowerShell | Microsoft Docs
description: Omówienie programu Azure Stack PowerShell z instrukcjami dotyczącymi instalacji i konfiguracji.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575420"
---
# <a name="azurerm-module-230"></a>Moduł AzureRM 2.3.0

## <a name="requirements"></a>Wymagania:
Minimalna obsługiwana wersja usługi Azure Stack to 1808.

Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11


## <a name="install"></a>Instalowanie
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a>Informacje o wersji
* Wersja 2.3.0 zawiera listę zmian powodujących niezgodność. Aby uaktualnić z wersji 1.2.11, skorzystaj z przygotowanego przez nas przewodnika po migracji dostępnego pod adresem https://aka.ms/azspowershellmigration
* Ta wersja odpowiada specyficznemu dla usługi Azure Stack profilowi interfejsu API o nazwie 2018-03-01-hybrid
* Wszystkie moduły mają taką samą lub większą zależność od modułu AzureRm.Profile.
* Wersje interfejsu API obsługiwane przez poszczególne moduły zostały zaktualizowane. 
    * Obliczenia — 30.03.2017
    * Sieć — 01.10.2017
    * Magazyn — 01.01.2016
    * Zasoby — 01.02.2018
    * Magazyn kluczy — 01.10.2016
    * DNS — 01.04.2016
* Pełną mapę wersji interfejsu API dla poszczególnych typów zasobów można znaleźć pod adresem https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json

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
