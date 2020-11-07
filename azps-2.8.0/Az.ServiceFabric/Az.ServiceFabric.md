---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2019
ms.locfileid: "93704570"
---
# <span data-ttu-id="416fa-101">AZ. moduł servicefabric</span><span class="sxs-lookup"><span data-stu-id="416fa-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="416fa-102">Opis</span><span class="sxs-lookup"><span data-stu-id="416fa-102">Description</span></span>
<span data-ttu-id="416fa-103">Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.</span><span class="sxs-lookup"><span data-stu-id="416fa-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="416fa-104">AZ. polecenia cmdlet w usłudze servicefabric</span><span class="sxs-lookup"><span data-stu-id="416fa-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="416fa-105">Dodaj-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="416fa-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="416fa-106">Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="416fa-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="416fa-107">Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.</span><span class="sxs-lookup"><span data-stu-id="416fa-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="416fa-108">Dodaj-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="416fa-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="416fa-109">Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="416fa-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="416fa-110">Dodaj-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="416fa-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="416fa-111">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="416fa-112">Dodaj-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="416fa-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="416fa-113">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="416fa-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="416fa-114">Dodaj-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="416fa-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="416fa-115">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="416fa-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="416fa-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="416fa-117">Pobierz szczegóły aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="416fa-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="416fa-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="416fa-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="416fa-119">Pobieranie szczegółów typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="416fa-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="416fa-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="416fa-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="416fa-121">Uzyskiwanie szczegółowych informacji o wersji typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="416fa-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="416fa-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="416fa-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="416fa-123">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="416fa-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="416fa-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="416fa-125">Pobierz szczegóły usługi programu Service Fabric w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="416fa-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="416fa-126">Nowe — AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="416fa-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="416fa-127">Utwórz nową aplikację sieci szkieletowej usługi w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="416fa-128">Nowe — AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="416fa-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="416fa-129">Utwórz nowy typ aplikacji sieci szkieletowej usług pod określoną grupą zasobów i klastrem.</span><span class="sxs-lookup"><span data-stu-id="416fa-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="416fa-130">Nowe — AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="416fa-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="416fa-131">Tworzenie nowej wersji typu aplikacji w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="416fa-132">Nowe — AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="416fa-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="416fa-133">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="416fa-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="416fa-134">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="416fa-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="416fa-135">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="416fa-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="416fa-136">Nowe — AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="416fa-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="416fa-137">Tworzenie nowej usługi programu Fabric Service w ramach określonej aplikacji i klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="416fa-138">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="416fa-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="416fa-139">Usuwanie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-139">Remove an application from the cluster.</span></span> <span data-ttu-id="416fa-140">Spowoduje to usunięcie wszystkich usług objętych aplikacją.</span><span class="sxs-lookup"><span data-stu-id="416fa-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="416fa-141">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="416fa-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="416fa-142">Usuwanie usługi Fabric typ aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="416fa-143">Spowoduje to usunięcie wszystkich wersji typów w obszarze ten zasób.</span><span class="sxs-lookup"><span data-stu-id="416fa-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="416fa-144">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="416fa-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="416fa-145">Usuwanie usługi sieci szkieletowej w wersji typu aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="416fa-146">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="416fa-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="416fa-147">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="416fa-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="416fa-148">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="416fa-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="416fa-149">Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="416fa-150">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="416fa-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="416fa-151">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="416fa-152">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="416fa-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="416fa-153">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="416fa-154">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="416fa-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="416fa-155">Usuwanie usługi z klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="416fa-156">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="416fa-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="416fa-157">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="416fa-158">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="416fa-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="416fa-159">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="416fa-160">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="416fa-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="416fa-161">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="416fa-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="416fa-162">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="416fa-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="416fa-163">Aktualizowanie aplikacji sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="416fa-163">Update a service fabric application.</span></span> <span data-ttu-id="416fa-164">Umożliwia to zaktualizowanie parametrów aplikacji i/lub uaktualnienie wersji typu aplikacji, która wyzwoli uaktualnienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="416fa-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="416fa-165">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="416fa-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="416fa-166">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="416fa-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="416fa-167">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="416fa-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="416fa-168">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="416fa-168">Update the reliability tier of the primary node type in a cluster.</span></span>

