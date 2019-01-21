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
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240139"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="6cf1f-103">Moduł usługi Azure Stack w wersji 1.6.0</span><span class="sxs-lookup"><span data-stu-id="6cf1f-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf1f-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="6cf1f-104">Requirements:</span></span>
<span data-ttu-id="6cf1f-105">Minimalna obsługiwana wersja usługi Azure Stack to 1811.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="6cf1f-106">Uwaga: Jeśli używasz starszej wersji, zainstaluj wersję 1.6.0</span><span class="sxs-lookup"><span data-stu-id="6cf1f-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="6cf1f-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="6cf1f-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="6cf1f-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="6cf1f-108">Release Notes</span></span>
* <span data-ttu-id="6cf1f-109">Obsługiwane z aktualizacją 1811</span><span class="sxs-lookup"><span data-stu-id="6cf1f-109">Supported with 1811 update</span></span>
* <span data-ttu-id="6cf1f-110">Moduł Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="6cf1f-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="6cf1f-111">Naprawiono brakujący prefiks Azs dla polecenia New-DataDiskObject i dodano alias z ostrzeżeniem o przyszłym wycofaniu.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="6cf1f-112">Moduł Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="6cf1f-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="6cf1f-113">Dodano ostrzeżenie z zaleceniem użycia polecenia Test-AzureStack przed poleceniem Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="6cf1f-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="6cf1f-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="6cf1f-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="6cf1f-115">Nowe polecenia cmdlet (te funkcje są obsługiwane przez usługę Azure Stack w wersji 1811 lub nowszej)</span><span class="sxs-lookup"><span data-stu-id="6cf1f-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="6cf1f-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="6cf1f-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="6cf1f-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="6cf1f-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="6cf1f-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="6cf1f-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="6cf1f-119">Przestarzałe</span><span class="sxs-lookup"><span data-stu-id="6cf1f-119">Deprecation</span></span>
        * <span data-ttu-id="6cf1f-120">Polecenie cmdlet Get-AzsInfrastructureVolume jest teraz aliasem polecenia cmdlet Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="6cf1f-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="6cf1f-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="6cf1f-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="6cf1f-122">Dodano nowe polecenie cmdlet Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="6cf1f-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="6cf1f-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="6cf1f-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="6cf1f-124">Poprawiono usterkę, w przypadku której nie są używane wartości domyślne przydziału</span><span class="sxs-lookup"><span data-stu-id="6cf1f-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="6cf1f-125">Moduł Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="6cf1f-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="6cf1f-126">Naprawiono brakujący prefiks Azs dla polecenia New-AddonPlanDefinitionObject i dodano alias z ostrzeżeniem o przyszłym wycofaniu.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
