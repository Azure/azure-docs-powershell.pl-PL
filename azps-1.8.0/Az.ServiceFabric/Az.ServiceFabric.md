---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93704379"
---
# <span data-ttu-id="2e5b3-101">AZ. moduł servicefabric</span><span class="sxs-lookup"><span data-stu-id="2e5b3-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="2e5b3-102">Opis</span><span class="sxs-lookup"><span data-stu-id="2e5b3-102">Description</span></span>
<span data-ttu-id="2e5b3-103">Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="2e5b3-104">AZ. polecenia cmdlet w usłudze servicefabric</span><span class="sxs-lookup"><span data-stu-id="2e5b3-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="2e5b3-105">Dodaj-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="2e5b3-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="2e5b3-106">Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="2e5b3-107">Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="2e5b3-108">Dodaj-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2e5b3-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2e5b3-109">Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="2e5b3-110">Dodaj-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2e5b3-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2e5b3-111">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="2e5b3-112">Dodaj-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2e5b3-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="2e5b3-113">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="2e5b3-114">Dodaj-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2e5b3-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="2e5b3-115">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="2e5b3-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2e5b3-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="2e5b3-117">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="2e5b3-118">Nowe — AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2e5b3-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="2e5b3-119">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="2e5b3-120">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="2e5b3-121">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="2e5b3-122">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2e5b3-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2e5b3-123">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="2e5b3-124">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2e5b3-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2e5b3-125">Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="2e5b3-126">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2e5b3-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="2e5b3-127">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="2e5b3-128">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2e5b3-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="2e5b3-129">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="2e5b3-130">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2e5b3-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="2e5b3-131">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="2e5b3-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2e5b3-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="2e5b3-133">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="2e5b3-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2e5b3-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="2e5b3-135">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="2e5b3-136">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2e5b3-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="2e5b3-137">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="2e5b3-138">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2e5b3-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="2e5b3-139">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-139">Update the reliability tier of the primary node type in a cluster.</span></span>

