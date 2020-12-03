---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: e19fea440025e7a00a037e360ac95ff8e0e62129
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/01/2020
ms.locfileid: "96428014"
---
# <a name="azure-stack-module-180"></a><span data-ttu-id="933c9-103">Moduł usługi Azure Stack w wersji 1.8.0</span><span class="sxs-lookup"><span data-stu-id="933c9-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="933c9-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="933c9-104">Requirements:</span></span>

<span data-ttu-id="933c9-105">Minimalna obsługiwana wersja usługi Azure Stack to 1910.</span><span class="sxs-lookup"><span data-stu-id="933c9-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="933c9-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="933c9-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="933c9-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="933c9-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="933c9-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="933c9-108">Release Notes</span></span>

* <span data-ttu-id="933c9-109">Obsługiwane z aktualizacją 1910</span><span class="sxs-lookup"><span data-stu-id="933c9-109">Supported with 1910 update</span></span>
* <span data-ttu-id="933c9-110">Zmiany te obejmują:</span><span class="sxs-lookup"><span data-stu-id="933c9-110">Changes include:</span></span>

    - <span data-ttu-id="933c9-111">**Nowy moduł administracyjny dostawcy DRP**: Dostawca Deployment Resource Provider (DRP) umożliwia zorganizowane wdrożenia dostawców zasobów w usłudze Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="933c9-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="933c9-112">Te polecenia współpracują z warstwą Azure Resource Manager w celu interakcji z dostawcą DRP.</span><span class="sxs-lookup"><span data-stu-id="933c9-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="933c9-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="933c9-113">**BRP**:</span></span>
        - <span data-ttu-id="933c9-114">Obsługa przywracania pojedynczej roli na potrzeby tworzenia kopii zapasowej infrastruktury stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="933c9-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="933c9-115">Dodanie parametru `RoleName` do polecenia cmdlet języka R `estore-AzsBackup`.</span><span class="sxs-lookup"><span data-stu-id="933c9-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="933c9-116">**FRP**: Zmiany powodujące niezgodność dla zasobów **Dysk** i **Wolumin** z interfejsem API w wersji 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="933c9-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="933c9-117">Te funkcje są obsługiwane przez usługę Azure Stack Hub w wersji 1910 lub nowszej:</span><span class="sxs-lookup"><span data-stu-id="933c9-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="933c9-118">Zmieniono wartość identyfikatora oraz parametrów `Name`, `HealthStatus` i `OperationalStatus`.</span><span class="sxs-lookup"><span data-stu-id="933c9-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="933c9-119">Obsługiwane są nowe właściwości `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`i `StoragePool` dla zasobów **Dysk**.</span><span class="sxs-lookup"><span data-stu-id="933c9-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="933c9-120">Właściwości `CanPool` i `CannotPoolReason` zasobów **Dysk** są przestarzałe. Używaj zamiast nich właściwości `OperationalStatus`.</span><span class="sxs-lookup"><span data-stu-id="933c9-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>