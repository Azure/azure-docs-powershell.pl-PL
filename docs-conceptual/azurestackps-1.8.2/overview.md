---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: e314374eff433d1869378bdaa9a0370c3fd3d8d1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022954"
---
# <a name="azure-stack-module-182"></a><span data-ttu-id="d5bc4-103">Moduł usługi Azure Stack w wersji 1.8.2</span><span class="sxs-lookup"><span data-stu-id="d5bc4-103">Azure Stack Module 1.8.2</span></span>

## <a name="requirements"></a><span data-ttu-id="d5bc4-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="d5bc4-104">Requirements:</span></span>

<span data-ttu-id="d5bc4-105">Minimalna obsługiwana wersja usługi Azure Stack to 1910.</span><span class="sxs-lookup"><span data-stu-id="d5bc4-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="d5bc4-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="d5bc4-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="d5bc4-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="d5bc4-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.2
```

## <a name="release-notes"></a><span data-ttu-id="d5bc4-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="d5bc4-108">Release Notes</span></span>

* <span data-ttu-id="d5bc4-109">Obsługiwane z aktualizacją 1910</span><span class="sxs-lookup"><span data-stu-id="d5bc4-109">Supported with 1910 update</span></span>
