---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: 0ee905b741c9f79b4f831bb4ea628f97566b2f1d
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427279"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="46102-103">Moduł usługi Azure Stack w wersji 1.8.1</span><span class="sxs-lookup"><span data-stu-id="46102-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="46102-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="46102-104">Requirements:</span></span>

<span data-ttu-id="46102-105">Minimalna obsługiwana wersja usługi Azure Stack to 1910.</span><span class="sxs-lookup"><span data-stu-id="46102-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="46102-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="46102-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="46102-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="46102-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="46102-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="46102-108">Release Notes</span></span>

* <span data-ttu-id="46102-109">Obsługiwane z aktualizacją 1910</span><span class="sxs-lookup"><span data-stu-id="46102-109">Supported with 1910 update</span></span>