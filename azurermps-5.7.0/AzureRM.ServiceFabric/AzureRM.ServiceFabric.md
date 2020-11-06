---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522289"
---
# <span data-ttu-id="2e19d-101">Moduł AzureRM. servicefabric</span><span class="sxs-lookup"><span data-stu-id="2e19d-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="2e19d-102">Opis</span><span class="sxs-lookup"><span data-stu-id="2e19d-102">Description</span></span>
<span data-ttu-id="2e19d-103">Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.</span><span class="sxs-lookup"><span data-stu-id="2e19d-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="2e19d-104">Polecenia cmdlet AzureRM. servicefabric</span><span class="sxs-lookup"><span data-stu-id="2e19d-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="2e19d-105">Dodaj-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="2e19d-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="2e19d-106">Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="2e19d-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="2e19d-107">Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2e19d-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="2e19d-108">Dodaj-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2e19d-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="2e19d-109">Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="2e19d-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="2e19d-110">Dodaj-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2e19d-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="2e19d-111">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="2e19d-112">Dodaj-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2e19d-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="2e19d-113">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e19d-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="2e19d-114">Dodaj-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2e19d-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="2e19d-115">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="2e19d-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2e19d-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="2e19d-117">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="2e19d-118">Nowe — AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2e19d-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="2e19d-119">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2e19d-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="2e19d-120">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="2e19d-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="2e19d-121">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e19d-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="2e19d-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2e19d-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="2e19d-123">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e19d-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="2e19d-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2e19d-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="2e19d-125">Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="2e19d-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2e19d-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="2e19d-127">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="2e19d-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2e19d-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="2e19d-129">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="2e19d-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2e19d-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="2e19d-131">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="2e19d-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2e19d-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="2e19d-133">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="2e19d-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2e19d-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="2e19d-135">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="2e19d-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="2e19d-136">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2e19d-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="2e19d-137">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e19d-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="2e19d-138">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2e19d-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="2e19d-139">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e19d-139">Update the reliability tier of the primary node type in a cluster.</span></span>

