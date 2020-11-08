---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231492"
---
# <span data-ttu-id="3bfe8-101">AZ. moduł servicefabric</span><span class="sxs-lookup"><span data-stu-id="3bfe8-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="3bfe8-102">Opis</span><span class="sxs-lookup"><span data-stu-id="3bfe8-102">Description</span></span>
<span data-ttu-id="3bfe8-103">Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="3bfe8-104">AZ. polecenia cmdlet w usłudze servicefabric</span><span class="sxs-lookup"><span data-stu-id="3bfe8-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="3bfe8-105">Dodaj-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3bfe8-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="3bfe8-106">Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="3bfe8-107">Dodaj-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3bfe8-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="3bfe8-108">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="3bfe8-109">Dodaj-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3bfe8-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="3bfe8-110">Dodawanie nazwy pospolitej certyfikatu lub odcisku palca do klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="3bfe8-111">Spowoduje to ponowne zarejestrowanie certyfikatu w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="3bfe8-112">Dodaj-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="3bfe8-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="3bfe8-113">Dodaj rozszerzenie maszyny wirtualnej do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="3bfe8-114">Dodaj-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="3bfe8-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="3bfe8-115">Dodaj klucz tajny certyfikatu do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="3bfe8-116">Dodaj-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3bfe8-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="3bfe8-117">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="3bfe8-118">Dodaj-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="3bfe8-119">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="3bfe8-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3bfe8-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="3bfe8-121">Pobierz szczegóły aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="3bfe8-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="3bfe8-123">Pobieranie szczegółów typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="3bfe8-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3bfe8-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="3bfe8-125">Uzyskiwanie szczegółowych informacji o wersji typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="3bfe8-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3bfe8-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="3bfe8-127">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="3bfe8-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3bfe8-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3bfe8-129">Uzyskiwanie szczegółów zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="3bfe8-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3bfe8-131">Pobierz szczegóły zasobu typu zarządzanego węzła.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="3bfe8-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3bfe8-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="3bfe8-133">Pobierz szczegóły usługi programu Service Fabric w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="3bfe8-134">Nowe — AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3bfe8-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="3bfe8-135">Utwórz nową aplikację sieci szkieletowej usługi w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="3bfe8-136">Nowe — AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="3bfe8-137">Utwórz nowy typ aplikacji sieci szkieletowej usług pod określoną grupą zasobów i klastrem.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="3bfe8-138">Nowe — AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3bfe8-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="3bfe8-139">Tworzenie nowej wersji typu aplikacji w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="3bfe8-140">Nowe — AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3bfe8-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="3bfe8-141">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="3bfe8-142">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="3bfe8-143">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="3bfe8-144">Nowe — AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3bfe8-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3bfe8-145">Tworzenie nowego zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="3bfe8-146">Nowe — AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3bfe8-147">Tworzenie nowego zasobu typu węzeł.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-147">Create new node type resource.</span></span>

### [<span data-ttu-id="3bfe8-148">Nowe — AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3bfe8-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="3bfe8-149">Tworzenie nowej usługi programu Fabric Service w ramach określonej aplikacji i klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="3bfe8-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3bfe8-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="3bfe8-151">Usuwanie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-151">Remove an application from the cluster.</span></span> <span data-ttu-id="3bfe8-152">Spowoduje to usunięcie wszystkich usług objętych aplikacją.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="3bfe8-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="3bfe8-154">Usuwanie usługi Fabric typ aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="3bfe8-155">Spowoduje to usunięcie wszystkich wersji typów w obszarze ten zasób.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="3bfe8-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3bfe8-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="3bfe8-157">Usuwanie usługi sieci szkieletowej w wersji typu aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="3bfe8-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3bfe8-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="3bfe8-159">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="3bfe8-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3bfe8-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="3bfe8-161">Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="3bfe8-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3bfe8-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3bfe8-163">Usuń zasób klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="3bfe8-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3bfe8-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="3bfe8-165">Remvoe certyfikat klienta według odcisku palca lub nazwy pospolitej.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="3bfe8-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3bfe8-167">Usuwanie typu węzła lub określonych węzłów w obrębie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="3bfe8-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="3bfe8-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="3bfe8-169">Usuń rozszerzenie maszyny wirtualnej z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="3bfe8-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3bfe8-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="3bfe8-171">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="3bfe8-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="3bfe8-173">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="3bfe8-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3bfe8-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="3bfe8-175">Usuwanie usługi z klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="3bfe8-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="3bfe8-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="3bfe8-177">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="3bfe8-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3bfe8-179">Ponownie uruchom określone węzły z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="3bfe8-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3bfe8-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3bfe8-181">Ustawianie właściwości zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="3bfe8-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3bfe8-183">Ustawia właściwości zasobu typu węzła lub uruchamia akcje ponownego tworzenia obrazów dla konkretnej usługi NDES typu węzła z parametrem-Reimage.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="3bfe8-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="3bfe8-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="3bfe8-185">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="3bfe8-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="3bfe8-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="3bfe8-187">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="3bfe8-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3bfe8-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="3bfe8-189">Aktualizowanie aplikacji sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-189">Update a service fabric application.</span></span> <span data-ttu-id="3bfe8-190">Umożliwia to zaktualizowanie parametrów aplikacji i/lub uaktualnienie wersji typu aplikacji, która wyzwoli uaktualnienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="3bfe8-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="3bfe8-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="3bfe8-192">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="3bfe8-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="3bfe8-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="3bfe8-194">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3bfe8-194">Update the reliability tier of the primary node type in a cluster.</span></span>

