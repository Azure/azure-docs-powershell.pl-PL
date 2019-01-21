---
title: Rozpoczynanie pracy z programem Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 483e74d7d047562b1c170c3767495161b9c5eb2f
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342138"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="304b9-102">Rozpoczynanie pracy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304b9-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="304b9-103">Program Azure PowerShell jest przeznaczony do zarządzania i administrowania zasobami platformy Azure z wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="304b9-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="304b9-104">Za pomocą programu Azure PowerShell możesz tworzyć zautomatyzowane narzędzia korzystające z modelu usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="304b9-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="304b9-105">Wypróbuj go w przeglądarce przy użyciu [usługi Azure Cloud Shell](/azure/cloud-shell/overview) lub zainstaluj go na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="304b9-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="304b9-106">W tym artykule przedstawiono podstawowe pojęcia związane z programem Azure PowerShell, które ułatwiają rozpoczęcie korzystania z niego.</span><span class="sxs-lookup"><span data-stu-id="304b9-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="304b9-107">Instalowanie lub uruchamianie w usłudze Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="304b9-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="304b9-108">Najprostszym sposobem rozpoczęcia pracy z programem Azure PowerShell jest wypróbowanie go w środowisku usługi Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="304b9-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="304b9-109">Aby rozpocząć pracę z usługą Cloud Shell, zobacz [Przewodnik Szybki start dotyczący programu PowerShell w usłudze Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="304b9-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="304b9-110">Usługa Cloud Shell uruchamia program PowerShell 6 w kontenerze systemu Linux, więc funkcje specyficzne dla systemu Windows są niedostępne.</span><span class="sxs-lookup"><span data-stu-id="304b9-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="304b9-111">Jeśli chcesz zainstalować program Azure PowerShell na komputerze lokalnym, wykonaj instrukcje podane w temacie [Instalowanie modułu Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="304b9-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="304b9-112">Logowanie do platformy Azure</span><span class="sxs-lookup"><span data-stu-id="304b9-112">Sign in to Azure</span></span>

<span data-ttu-id="304b9-113">Zaloguj się interakcyjnie przy użyciu polecenia cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="304b9-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="304b9-114">Pomiń ten krok, jeśli korzystasz z usługi Cloud Shell: Sesja usługi Azure Cloud Shell jest już uwierzytelniona dla danego środowiska, subskrypcji i dzierżawy, w których uruchomiono sesję usługi Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="304b9-114">Skip this step if you use Cloud Shell: Your Auzre Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="304b9-115">Jeśli jesteś w regionie innym niż Stany Zjednoczone, użyj parametru `-Environment`, aby się zalogować.</span><span class="sxs-lookup"><span data-stu-id="304b9-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="304b9-116">Uzyskaj nazwę środowiska dla swojego regionu, używając polecenia cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="304b9-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="304b9-117">Aby na przykład zalogować się do platformy Azure w Chinach — 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="304b9-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="304b9-118">Uzyskasz token do użycia w witrynie https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="304b9-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="304b9-119">Otwórz tę stronę w przeglądarce i wprowadź token, a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure i autoryzuj program Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="304b9-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="304b9-120">Po zalogowaniu użyj poleceń cmdlet programu Azure PowerShell, aby uzyskiwać dostęp do zasobów w subskrypcji i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="304b9-120">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="304b9-121">Aby dowiedzieć się więcej na temat procesu logowania i metod uwierzytelniania, zobacz [Logowanie się w programie Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="304b9-121">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="304b9-122">Znajdowanie poleceń</span><span class="sxs-lookup"><span data-stu-id="304b9-122">Find commands</span></span>

<span data-ttu-id="304b9-123">Polecenia cmdlet programu Azure PowerShell używają standardowej konwencji nazewnictwa dla programu PowerShell: `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="304b9-123">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="304b9-124">Czasownik opisuje akcję (przykłady: `Create`, `Get`, `Set`, `Delete`), a rzeczownik opisuje typ zasobu (przykłady: `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="304b9-124">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="304b9-125">Rzeczowniki w programie Azure PowerShell zawsze rozpoczynają się prefiksem `Az`.</span><span class="sxs-lookup"><span data-stu-id="304b9-125">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="304b9-126">Aby uzyskać pełną listę standardowych czasowników, zobacz [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Zatwierdzone czasowniki dla poleceń programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="304b9-126">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="304b9-127">Znajomość dostępnych rzeczowników, czasowników i modułów programu Azure PowerShell ułatwia znajdowanie poleceń za pomocą polecenia cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="304b9-127">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="304b9-128">Aby na przykład znaleźć wszystkie polecenia dotyczące maszyn wirtualnych i używające czasownika `Get`:</span><span class="sxs-lookup"><span data-stu-id="304b9-128">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="304b9-129">Aby ułatwić znajdowanie typowych poleceń, w poniższej tabeli podano typy zasobów, odpowiednie moduły programu Azure PowerShell i prefiksy rzeczowników do używania z poleceniem `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="304b9-129">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="304b9-130">Typ zasobu</span><span class="sxs-lookup"><span data-stu-id="304b9-130">Resource type</span></span> | <span data-ttu-id="304b9-131">Moduł programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304b9-131">Azure PowerShell module</span></span> | <span data-ttu-id="304b9-132">Prefiks rzeczownika</span><span class="sxs-lookup"><span data-stu-id="304b9-132">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="304b9-133">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="304b9-133">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="304b9-134">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="304b9-134">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="304b9-135">Maszyny wirtualne</span><span class="sxs-lookup"><span data-stu-id="304b9-135">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="304b9-136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="304b9-136">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="304b9-137">Konta magazynu</span><span class="sxs-lookup"><span data-stu-id="304b9-137">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="304b9-138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="304b9-138">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="304b9-139">Usługa Key Vault</span><span class="sxs-lookup"><span data-stu-id="304b9-139">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="304b9-140">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="304b9-140">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="304b9-141">Aplikacje internetowe</span><span class="sxs-lookup"><span data-stu-id="304b9-141">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="304b9-142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="304b9-142">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="304b9-143">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="304b9-143">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="304b9-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="304b9-144">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="304b9-145">Aby uzyskać pełną listę modułów w programie Azure PowerShell, zobacz [listę modułów programu Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hostowaną w serwisie GitHub.</span><span class="sxs-lookup"><span data-stu-id="304b9-145">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="304b9-146">Nauka podstaw programu Azure PowerShell za pomocą samouczków i przewodników Szybki start</span><span class="sxs-lookup"><span data-stu-id="304b9-146">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="304b9-147">Aby rozpocząć pracę z programem Azure PowerShell, wypróbuj szczegółowy samouczek na temat konfigurowania maszyn wirtualnych i wykonywania dotyczących ich zapytań.</span><span class="sxs-lookup"><span data-stu-id="304b9-147">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="304b9-148">Tworzenie maszyn wirtualnych przy użyciu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304b9-148">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="304b9-149">Dostępne są też przewodniki Szybki start dla programu Azure PowerShell dotyczące innych popularnych usług platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="304b9-149">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="304b9-150">Tworzenie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="304b9-150">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="304b9-151">Transferowanie obiektów do i z usługi Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="304b9-151">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="304b9-152">Tworzenie i pobieranie wpisów tajnych w usłudze Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="304b9-152">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="304b9-153">Tworzenie bazy danych Azure SQL i zapory</span><span class="sxs-lookup"><span data-stu-id="304b9-153">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="304b9-154">Uruchamianie kontenera w usłudze Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="304b9-154">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="304b9-155">Tworzenie zestawu skalowania maszyn wirtualnych (VMSS)</span><span class="sxs-lookup"><span data-stu-id="304b9-155">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="304b9-156">Tworzenie modułu równoważenia obciążenia w warstwie Standardowa</span><span class="sxs-lookup"><span data-stu-id="304b9-156">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="304b9-157">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="304b9-157">Next steps</span></span>

* [<span data-ttu-id="304b9-158">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304b9-158">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="304b9-159">Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304b9-159">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="304b9-160">Tworzenie jednostek usługi przy użyciu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304b9-160">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="304b9-161">Uzyskiwanie pomocy od społeczności:</span><span class="sxs-lookup"><span data-stu-id="304b9-161">Get help from the community:</span></span>
  * [<span data-ttu-id="304b9-162">Forum platformy Azure w witrynie MSDN</span><span class="sxs-lookup"><span data-stu-id="304b9-162">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="304b9-163">Serwis Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="304b9-163">Stacki Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
