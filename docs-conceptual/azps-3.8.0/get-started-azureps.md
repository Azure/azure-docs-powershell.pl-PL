---
title: Rozpoczynanie pracy z programem Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.openlocfilehash: 718f0dc0f1ef9b0c2aa3d0630ca099fa5cec7ec0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740358"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="cc794-102">Rozpoczynanie pracy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc794-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="cc794-103">Program Azure PowerShell jest przeznaczony do zarządzania i administrowania zasobami platformy Azure z wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="cc794-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="cc794-104">Za pomocą programu Azure PowerShell możesz tworzyć zautomatyzowane narzędzia korzystające z modelu usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="cc794-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="cc794-105">Wypróbuj go w przeglądarce przy użyciu [usługi Azure Cloud Shell](/azure/cloud-shell/overview) lub zainstaluj go na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="cc794-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="cc794-106">W tym artykule przedstawiono podstawowe pojęcia związane z programem Azure PowerShell, które ułatwiają rozpoczęcie korzystania z niego.</span><span class="sxs-lookup"><span data-stu-id="cc794-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="cc794-107">Instalowanie lub uruchamianie w usłudze Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="cc794-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="cc794-108">Najprostszym sposobem rozpoczęcia pracy z programem Azure PowerShell jest wypróbowanie go w środowisku usługi Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="cc794-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="cc794-109">Aby rozpocząć pracę z usługą Cloud Shell, zobacz [Przewodnik Szybki start dotyczący programu PowerShell w usłudze Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="cc794-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="cc794-110">Usługa Cloud Shell uruchamia program PowerShell 6 w kontenerze systemu Linux, więc funkcje specyficzne dla systemu Windows są niedostępne.</span><span class="sxs-lookup"><span data-stu-id="cc794-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="cc794-111">Jeśli chcesz zainstalować program Azure PowerShell na komputerze lokalnym, wykonaj instrukcje podane w temacie [Instalowanie modułu Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="cc794-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="cc794-112">Logowanie do platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cc794-112">Sign in to Azure</span></span>

<span data-ttu-id="cc794-113">Zaloguj się interakcyjnie przy użyciu polecenia cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="cc794-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="cc794-114">Pomiń ten krok, jeśli korzystasz z usługi Cloud Shell: Sesja usługi Azure Cloud Shell jest już uwierzytelniona dla danego środowiska, subskrypcji i dzierżawy, w których uruchomiono sesję usługi Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="cc794-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="cc794-115">Jeśli jesteś w regionie innym niż Stany Zjednoczone, użyj parametru `-Environment`, aby się zalogować.</span><span class="sxs-lookup"><span data-stu-id="cc794-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="cc794-116">Uzyskaj nazwę środowiska dla swojego regionu, używając polecenia cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="cc794-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="cc794-117">Aby na przykład zalogować się do platformy Azure w Chinach — 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="cc794-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="cc794-118">W środowiskach PowerShell 5.1 jest wyświetlane okno dialogowe logowania, w którym można podać nazwę użytkownika i hasło konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc794-118">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="cc794-119">W przypadku każdej innej wersji programu PowerShell uzyskasz token do użycia na stronie [https://microsoft.com/devicelogin ].</span><span class="sxs-lookup"><span data-stu-id="cc794-119">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="cc794-120">Otwórz tę stronę w przeglądarce i wprowadź token, a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure i autoryzuj program Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cc794-120">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="cc794-121">Po zalogowaniu zobaczysz informacje wskazujące, która subskrypcja platformy Azure jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="cc794-121">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="cc794-122">Jeśli masz wiele subskrypcji platformy Azure w ramach konta i chcesz wybrać inną, pobierz dostępne subskrypcje przy użyciu polecenia [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription), a następnie użyj polecenia cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) z identyfikatorem subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cc794-122">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="cc794-123">Aby uzyskać więcej informacji o zarządzaniu subskrypcjami platformy Azure w programie Azure PowerShell, zobacz [Use multiple Azure subscriptions (Używanie wielu subskrypcji platformy Azure)](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="cc794-123">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="cc794-124">Po zalogowaniu użyj poleceń cmdlet programu Azure PowerShell, aby uzyskiwać dostęp do zasobów w subskrypcji i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="cc794-124">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="cc794-125">Aby dowiedzieć się więcej na temat procesu logowania i metod uwierzytelniania, zobacz [Logowanie się w programie Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="cc794-125">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="cc794-126">Znajdowanie poleceń</span><span class="sxs-lookup"><span data-stu-id="cc794-126">Find commands</span></span>

<span data-ttu-id="cc794-127">Polecenia cmdlet programu Azure PowerShell używają standardowej konwencji nazewnictwa dla programu PowerShell: `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="cc794-127">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="cc794-128">Czasownik (verb) opisuje akcję (przykłady: `New`, `Get`, `Set`, `Remove`), a rzeczownik (noun) opisuje typ zasobu (przykłady: `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="cc794-128">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="cc794-129">Rzeczowniki w programie Azure PowerShell zawsze rozpoczynają się prefiksem `Az`.</span><span class="sxs-lookup"><span data-stu-id="cc794-129">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="cc794-130">Aby uzyskać pełną listę standardowych czasowników, zobacz [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Zatwierdzone czasowniki dla poleceń programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="cc794-130">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="cc794-131">Znajomość dostępnych rzeczowników, czasowników i modułów programu Azure PowerShell ułatwia znajdowanie poleceń za pomocą polecenia cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="cc794-131">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="cc794-132">Aby na przykład znaleźć wszystkie polecenia dotyczące maszyn wirtualnych i używające czasownika `Get`:</span><span class="sxs-lookup"><span data-stu-id="cc794-132">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="cc794-133">Aby ułatwić znajdowanie typowych poleceń, w poniższej tabeli podano typy zasobów, odpowiednie moduły programu Azure PowerShell i prefiksy rzeczowników do używania z poleceniem `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="cc794-133">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="cc794-134">Typ zasobu</span><span class="sxs-lookup"><span data-stu-id="cc794-134">Resource type</span></span> | <span data-ttu-id="cc794-135">Moduł programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc794-135">Azure PowerShell module</span></span> | <span data-ttu-id="cc794-136">Prefiks rzeczownika</span><span class="sxs-lookup"><span data-stu-id="cc794-136">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="cc794-137">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="cc794-137">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="cc794-138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cc794-138">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="cc794-139">Maszyny wirtualne</span><span class="sxs-lookup"><span data-stu-id="cc794-139">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="cc794-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cc794-140">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="cc794-141">Konta magazynu</span><span class="sxs-lookup"><span data-stu-id="cc794-141">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="cc794-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cc794-142">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="cc794-143">Usługa Key Vault</span><span class="sxs-lookup"><span data-stu-id="cc794-143">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="cc794-144">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cc794-144">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="cc794-145">Aplikacje internetowe</span><span class="sxs-lookup"><span data-stu-id="cc794-145">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="cc794-146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cc794-146">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="cc794-147">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="cc794-147">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="cc794-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cc794-148">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="cc794-149">Aby uzyskać pełną listę modułów w programie Azure PowerShell, zobacz [listę modułów programu Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hostowaną w serwisie GitHub.</span><span class="sxs-lookup"><span data-stu-id="cc794-149">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="cc794-150">Nauka podstaw programu Azure PowerShell za pomocą samouczków i przewodników Szybki start</span><span class="sxs-lookup"><span data-stu-id="cc794-150">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="cc794-151">Aby rozpocząć pracę z programem Azure PowerShell, wypróbuj szczegółowy samouczek na temat konfigurowania maszyn wirtualnych i wykonywania dotyczących ich zapytań.</span><span class="sxs-lookup"><span data-stu-id="cc794-151">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="cc794-152">Tworzenie maszyn wirtualnych przy użyciu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc794-152">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="cc794-153">Dostępne są też przewodniki Szybki start dla programu Azure PowerShell dotyczące innych popularnych usług platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="cc794-153">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="cc794-154">Tworzenie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="cc794-154">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="cc794-155">Transferowanie obiektów do i z usługi Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="cc794-155">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="cc794-156">Tworzenie i pobieranie wpisów tajnych w usłudze Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="cc794-156">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="cc794-157">Tworzenie bazy danych Azure SQL Database i zapory</span><span class="sxs-lookup"><span data-stu-id="cc794-157">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="cc794-158">Uruchamianie kontenera w usłudze Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="cc794-158">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="cc794-159">Tworzenie zestawu skalowania maszyn wirtualnych (VMSS)</span><span class="sxs-lookup"><span data-stu-id="cc794-159">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="cc794-160">Tworzenie modułu równoważenia obciążenia w warstwie Standardowa</span><span class="sxs-lookup"><span data-stu-id="cc794-160">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="cc794-161">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="cc794-161">Next steps</span></span>

* [<span data-ttu-id="cc794-162">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc794-162">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="cc794-163">Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc794-163">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="cc794-164">Tworzenie jednostek usługi przy użyciu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc794-164">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="cc794-165">Uzyskiwanie pomocy od społeczności:</span><span class="sxs-lookup"><span data-stu-id="cc794-165">Get help from the community:</span></span>
  * [<span data-ttu-id="cc794-166">Forum platformy Azure w witrynie MSDN</span><span class="sxs-lookup"><span data-stu-id="cc794-166">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="cc794-167">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="cc794-167">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
