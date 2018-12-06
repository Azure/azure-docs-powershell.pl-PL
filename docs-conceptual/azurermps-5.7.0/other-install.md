---
title: Inne metody instalacji programu Azure PowerShell
description: Jak zainstalować program Azure PowerShell bez modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f9293d2715b36161c3e6d0d9469b6f18ab35d6c8
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828216"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="a9e71-103">Instalowanie programu Azure PowerShell w systemie Windows za pomocą instalatora MSI lub Instalatora platformy internetowej</span><span class="sxs-lookup"><span data-stu-id="a9e71-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="a9e71-104">W tym artykule opisano sposób instalowania programu Azure PowerShell w systemie Windows przy użyciu pliku MSI lub Instalatora platformy internetowej (WebPI).</span><span class="sxs-lookup"><span data-stu-id="a9e71-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="a9e71-105">Tych metod instalacji należy używać tylko wtedy, gdy są one niezbędne w danym systemie.</span><span class="sxs-lookup"><span data-stu-id="a9e71-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="a9e71-106">Zalecaną metodą instalacji programu Azure PowerShell w systemie Windows jest moduł PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a9e71-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="a9e71-107">Aby uzyskać instrukcje dotyczące instalowania programu Azure PowerShell przy użyciu modułu PowerShellGet, zobacz [Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="a9e71-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="a9e71-108">Aby zainstalować w środowiskach Linux lub macOS, zobacz [Instalowanie programu Azure PowerShell w systemie macOS lub Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="a9e71-108">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="a9e71-109">Instalowanie lub aktualizowanie w systemie Windows za pomocą pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="a9e71-109">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="a9e71-110">Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="a9e71-110">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="a9e71-111">Jeśli zainstalowano wcześniejsze wersje modułów platformy Azure za pomocą pakietu MSI, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="a9e71-111">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="a9e71-112">Pakiet MSI instaluje moduły w lokalizacji `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="a9e71-112">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="a9e71-113">Zostaną zainstalowane moduły `AzureRM` i `Azure`.</span><span class="sxs-lookup"><span data-stu-id="a9e71-113">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="a9e71-114">Używaj modułu `Azure` tylko wtedy, gdy pracujesz z klasycznym modelem wdrażania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e71-114">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="a9e71-115">Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `AzureRM` w bieżącej sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e71-115">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="a9e71-116">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="a9e71-116">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a9e71-117">Automatyczne zaimportowanie modułu `AzureRM` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="a9e71-117">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="a9e71-118">Aby dowiedzieć się, jak można utrwalić swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a9e71-118">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="a9e71-119">Instalowanie lub aktualizowanie w systemie Windows za pomocą Instalatora platformy internetowej</span><span class="sxs-lookup"><span data-stu-id="a9e71-119">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="a9e71-120">Pobierz [pakiet WebPI programu Azure PowerShell](http://aka.ms/webpi-azps) i uruchom instalację.</span><span class="sxs-lookup"><span data-stu-id="a9e71-120">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="a9e71-121">Jeśli zainstalowano wcześniejsze wersje modułów platformy Azure za pomocą pakietu MSI lub instalatora WebPI, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="a9e71-121">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="a9e71-122">Moduły zostaną zainstalowane w lokalizacji `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="a9e71-122">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="a9e71-123">Zostaną zainstalowane moduły `AzureRM` i `Azure`.</span><span class="sxs-lookup"><span data-stu-id="a9e71-123">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="a9e71-124">Używaj modułu `Azure` tylko wtedy, gdy pracujesz z klasycznym modelem wdrażania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e71-124">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="a9e71-125">Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `AzureRM` w bieżącej sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e71-125">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="a9e71-126">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="a9e71-126">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a9e71-127">Automatyczne zaimportowanie modułu `AzureRM` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="a9e71-127">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="a9e71-128">Aby dowiedzieć się, jak można utrwalić swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a9e71-128">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
