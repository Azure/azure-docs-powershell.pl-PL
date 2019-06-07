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
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855792"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="63f67-103">Moduł usługi Azure Stack w wersji 1.7.2</span><span class="sxs-lookup"><span data-stu-id="63f67-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="63f67-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="63f67-104">Requirements:</span></span>

<span data-ttu-id="63f67-105">Minimalna obsługiwana wersja usługi Azure Stack to 1904.</span><span class="sxs-lookup"><span data-stu-id="63f67-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="63f67-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="63f67-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="63f67-107">Instalowanie programu PowerShell dla usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="63f67-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="63f67-108">Instalacja składa się z trzech kroków:</span><span class="sxs-lookup"><span data-stu-id="63f67-108">Installation has three steps:</span></span>

1. <span data-ttu-id="63f67-109">Instalowanie programu Azure Stack PowerShell w zależności od wersji usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="63f67-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="63f67-110">Włączanie dodatkowych funkcji magazynu</span><span class="sxs-lookup"><span data-stu-id="63f67-110">Enable additional storage features</span></span>
3. <span data-ttu-id="63f67-111">Potwierdzanie instalacji programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="63f67-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="63f67-112">Instalowanie programu Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="63f67-112">Install Azure Stack PowerShell</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a><span data-ttu-id="63f67-113">Włączanie dodatkowych funkcji magazynu</span><span class="sxs-lookup"><span data-stu-id="63f67-113">Enable additional storage features</span></span>

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a><span data-ttu-id="63f67-114">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="63f67-114">Release Notes</span></span>

* <span data-ttu-id="63f67-115">Obsługiwane z aktualizacją 1904</span><span class="sxs-lookup"><span data-stu-id="63f67-115">Supported with 1904 update</span></span>
* <span data-ttu-id="63f67-116">To jest wersja zawierająca zmiany powodujące niezgodność.</span><span class="sxs-lookup"><span data-stu-id="63f67-116">This a breaking change release.</span></span> <span data-ttu-id="63f67-117">Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="63f67-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="63f67-118">Moduł Azs.Backup.Admin \* Zmiana powodująca niezgodność: Kopia zapasowa zmienia się na tryb szyfrowania opartego na certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="63f67-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="63f67-119">Obsługa kluczy symetrycznych jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="63f67-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="63f67-120">Moduł Azs.Fabric.Admin       \* Wycofanie           \* Polecenie Get-AzsInfrastructureVolume jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsVolume \* Polecenie Get AzsStorageSystem jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsStorageSubSystem           \* Polecenie Get AzsStoragePool jest przestarzałe, obiekt StorageSubSystem ma właściwość pojemności</span><span class="sxs-lookup"><span data-stu-id="63f67-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="63f67-121">Moduł Azs.Compute.Admin           \* Poprawka usterki: Add-AzsPlatformImage, Get-AzsPlatformImage: Wywoływanie polecenia ConvertTo-PlatformImageObject tylko w ścieżce powodzenia           \* Poprawka usterki: Add-AzsVmExtension, Get-AzsVmExtension: Wywoływanie polecenia ConvertTo-VmExtensionObject tylko w ścieżce powodzenia</span><span class="sxs-lookup"><span data-stu-id="63f67-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="63f67-122">Moduł Azs.Storage.Admin           \* Poprawka usterki — nowy limit przydziału magazynu używa wartości domyślnych, jeśli żadne wartości nie zostaną podane.'</span><span class="sxs-lookup"><span data-stu-id="63f67-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
