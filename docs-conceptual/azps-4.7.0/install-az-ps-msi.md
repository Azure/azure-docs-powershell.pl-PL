---
title: Instalowanie programu Azure PowerShell za pomocą pakietu MSI
description: Jak zainstalować program Azure PowerShell bez modułu PowerShellGet za pomocą instalatora MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 193e8c5d14f1bf2fe9c84a9da2defac50be97ec7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "91833268"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="ac7bf-103">Instalowanie programu Azure PowerShell w systemie Windows za pomocą instalatora MSI</span><span class="sxs-lookup"><span data-stu-id="ac7bf-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="ac7bf-104">W tym artykule opisano sposób instalowania programu Azure PowerShell w systemie Windows przy użyciu instalatora MSI.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="ac7bf-105">Instalator MSI jest udostępniany na potrzeby środowisk, w których galeria programu PowerShell może być zablokowana przez zaporę, lub w których wymagany jest instalator w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="ac7bf-106">Zalecaną metodą instalacji programu Azure PowerShell jest moduł PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="ac7bf-107">Aby uzyskać instrukcje dotyczące instalowania programu Azure PowerShell przy użyciu modułu PowerShellGet, zobacz [Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7bf-108">Wymagania</span><span class="sxs-lookup"><span data-stu-id="ac7bf-108">Requirements</span></span>

<span data-ttu-id="ac7bf-109">Instalator MSI w systemie Windows jest zaprojektowany wyłącznie do instalowania programu Azure PowerShell dla programu PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="ac7bf-110">W przypadku instalacji na platformach innych niż Windows lub starszych wersji programu PowerShell, zobacz [Instalowanie za pomocą modułu PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="ac7bf-111">Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:</span><span class="sxs-lookup"><span data-stu-id="ac7bf-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="ac7bf-112">Aby użyć programu Azure PowerShell w programie PowerShell 5.1:</span><span class="sxs-lookup"><span data-stu-id="ac7bf-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="ac7bf-113">Jeśli to konieczne, przeprowadź aktualizację do programu [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="ac7bf-114">Jeśli używasz systemu Windows 10, masz już zainstalowany program PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="ac7bf-115">Zainstaluj program [.NET Framework 4.7.2 lub nowszy](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="ac7bf-116">Instalowanie lub aktualizowanie w systemie Windows za pomocą pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="ac7bf-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="ac7bf-117">Pakiet MSI dla programu Azure PowerShell jest dostępny w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases):</span><span class="sxs-lookup"><span data-stu-id="ac7bf-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="ac7bf-118">Przejdź do adresu https://github.com/Azure/azure-powershell/releases.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="ac7bf-119">Wyszukaj najnowszy moduł galerii dla programu Azure PowerShell (są one wyświetlane chronologicznie i zwykle są to tylko wersje wydania bez nazwy, np. „4.7.0”).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="ac7bf-120">Przewiń na sam dół informacji o poprawce i kliknij strzałkę obok pozycji „Zasoby”, aby wyświetlić opcje pakietu MSI.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="ac7bf-121">Kliknij wybrane polecenie Az pakietu MSI, aby rozpocząć pobieranie.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="ac7bf-122">Jeśli wcześniejsze wersje programu Azure PowerShell zainstalowano za pomocą pakietu MSI, instalator automatycznie je usunie.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="ac7bf-123">Pakiet MSI instaluje moduły w lokalizacji `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="ac7bf-124">Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="ac7bf-125">Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="ac7bf-126">Ze względu na strukturę modułu może to potrwać maksymalnie minutę.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="ac7bf-127">Musisz powtórzyć ten krok dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="ac7bf-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="ac7bf-128">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="ac7bf-129">Przekazywanie opinii</span><span class="sxs-lookup"><span data-stu-id="ac7bf-129">Provide feedback</span></span>

<span data-ttu-id="ac7bf-130">Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="ac7bf-131">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ac7bf-132">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="ac7bf-132">Next Steps</span></span>

<span data-ttu-id="ac7bf-133">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="ac7bf-134">Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="ac7bf-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>