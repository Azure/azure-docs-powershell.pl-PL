---
title: Inne metody instalacji programu Azure PowerShell
description: Jak zainstalować program Azure PowerShell bez modułu PowerShellGet za pomocą instalatora MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: b442da364a01cd6022c14cbb32a9b633676ca8c7
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828862"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="ababd-103">Instalowanie programu Azure PowerShell w systemie Windows za pomocą instalatora MSI</span><span class="sxs-lookup"><span data-stu-id="ababd-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="ababd-104">W tym artykule opisano sposób instalowania programu Azure PowerShell w systemie Windows przy użyciu instalatora MSI.</span><span class="sxs-lookup"><span data-stu-id="ababd-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="ababd-105">Tych metod instalacji należy używać tylko wtedy, gdy są one niezbędne w danym systemie.</span><span class="sxs-lookup"><span data-stu-id="ababd-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="ababd-106">Zalecaną metodą instalacji programu Azure PowerShell w systemie Windows jest moduł PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ababd-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="ababd-107">Aby uzyskać instrukcje dotyczące instalowania programu Azure PowerShell przy użyciu modułu PowerShellGet, zobacz [Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ababd-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ababd-108">Instalacja za pomocą Instalatora platformy internetowej nie jest już dostępna dla programu Azure PowerShell w wersji 6.x lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="ababd-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="ababd-109">Jeśli jest wymagane użycie Instalatora platformy internetowej, rozważ użycie zamiast niego instalatora MSI lub zainstaluj starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ababd-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="ababd-110">Aby zainstalować w środowiskach Linux lub macOS, zobacz [Instalowanie programu Azure PowerShell w systemie macOS lub Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="ababd-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="ababd-111">Instalowanie lub aktualizowanie w systemie Windows za pomocą pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="ababd-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="ababd-112">Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="ababd-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="ababd-113">Jeśli zainstalowano wcześniejsze wersje modułów platformy Azure za pomocą pakietu MSI, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="ababd-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="ababd-114">Pakiet MSI instaluje moduły w lokalizacji `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="ababd-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="ababd-115">Zostaną zainstalowane moduły `AzureRM` i `Azure`.</span><span class="sxs-lookup"><span data-stu-id="ababd-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="ababd-116">Używaj modułu `Azure` tylko wtedy, gdy pracujesz z klasycznym modelem wdrażania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ababd-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="ababd-117">Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ababd-117">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="ababd-118">Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="ababd-118">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="ababd-119">Ze względu na strukturę modułu może to potrwać kilka sekund.</span><span class="sxs-lookup"><span data-stu-id="ababd-119">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="ababd-120">Musisz powtórzyć ten krok dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="ababd-120">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="ababd-121">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ababd-121">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
