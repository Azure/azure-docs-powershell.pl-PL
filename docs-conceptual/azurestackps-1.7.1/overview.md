---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: d3069aba7d1ac248aff755e4b21533af1f73251d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/02/2019
ms.locfileid: "58808064"
---
# <a name="azure-stack-module-171"></a><span data-ttu-id="f8d49-103">Moduł usługi Azure Stack w wersji 1.7.1</span><span class="sxs-lookup"><span data-stu-id="f8d49-103">Azure Stack Module 1.7.1</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d49-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="f8d49-104">Requirements:</span></span>

<span data-ttu-id="f8d49-105">Minimalna obsługiwana wersja usługi Azure Stack to 1901.</span><span class="sxs-lookup"><span data-stu-id="f8d49-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="f8d49-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="f8d49-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="f8d49-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="f8d49-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a><span data-ttu-id="f8d49-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="f8d49-108">Release Notes</span></span>

* <span data-ttu-id="f8d49-109">Obsługiwane z aktualizacją 1901</span><span class="sxs-lookup"><span data-stu-id="f8d49-109">Supported with 1901 update</span></span>
* <span data-ttu-id="f8d49-110">To jest wersja zawierająca zmiany powodujące niezgodność.</span><span class="sxs-lookup"><span data-stu-id="f8d49-110">This a breaking change release.</span></span> <span data-ttu-id="f8d49-111">Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="f8d49-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="f8d49-112">Moduł Azs.Backup.Admin \* Zmiana powodująca niezgodność: Kopia zapasowa zmienia się na tryb szyfrowania opartego na certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="f8d49-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="f8d49-113">Obsługa kluczy symetrycznych jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="f8d49-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="f8d49-114">Moduł Azs.Fabric.Admin       \* Wycofanie           \* Polecenie Get-AzsInfrastructureVolume jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsVolume \* Polecenie Get AzsStorageSystem jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsStorageSubSystem           \* Polecenie Get AzsStoragePool jest przestarzałe, obiekt StorageSubSystem ma właściwość pojemności</span><span class="sxs-lookup"><span data-stu-id="f8d49-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="f8d49-115">Moduł Azs.Compute.Admin           \* Poprawka usterki: Add-AzsPlatformImage, Get-AzsPlatformImage: Wywoływanie polecenia ConvertTo-PlatformImageObject tylko w ścieżce powodzenia           \* Poprawka usterki: Add-AzsVmExtension, Get-AzsVmExtension: Wywoływanie polecenia ConvertTo-VmExtensionObject tylko w ścieżce powodzenia</span><span class="sxs-lookup"><span data-stu-id="f8d49-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="f8d49-116">Moduł Azs.Storage.Admin           \* Poprawka usterki — nowy limit przydziału magazynu używa wartości domyślnych, jeśli żadne wartości nie zostaną podane.'</span><span class="sxs-lookup"><span data-stu-id="f8d49-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
