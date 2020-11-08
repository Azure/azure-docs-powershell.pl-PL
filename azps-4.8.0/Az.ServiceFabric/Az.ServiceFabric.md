---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064754"
---
# <span data-ttu-id="71177-101">AZ. moduł servicefabric</span><span class="sxs-lookup"><span data-stu-id="71177-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="71177-102">Opis</span><span class="sxs-lookup"><span data-stu-id="71177-102">Description</span></span>
<span data-ttu-id="71177-103">Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.</span><span class="sxs-lookup"><span data-stu-id="71177-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="71177-104">AZ. polecenia cmdlet w usłudze servicefabric</span><span class="sxs-lookup"><span data-stu-id="71177-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="71177-105">Dodaj-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="71177-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="71177-106">Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="71177-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="71177-107">Dodaj-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="71177-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="71177-108">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="71177-109">Dodaj-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="71177-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="71177-110">Dodawanie nazwy pospolitej certyfikatu lub odcisku palca do klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="71177-111">Spowoduje to ponowne zarejestrowanie certyfikatu w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="71177-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="71177-112">Dodaj-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="71177-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="71177-113">Dodaj rozszerzenie maszyny wirtualnej do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="71177-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="71177-114">Dodaj-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="71177-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="71177-115">Dodaj klucz tajny certyfikatu do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="71177-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="71177-116">Dodaj-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="71177-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="71177-117">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="71177-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="71177-118">Dodaj-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="71177-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="71177-119">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="71177-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71177-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="71177-121">Pobierz szczegóły aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="71177-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="71177-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71177-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="71177-123">Pobieranie szczegółów typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="71177-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="71177-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71177-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="71177-125">Uzyskiwanie szczegółowych informacji o wersji typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="71177-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="71177-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="71177-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="71177-127">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="71177-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="71177-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="71177-129">Uzyskiwanie szczegółów zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="71177-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="71177-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="71177-131">Pobierz szczegóły zasobu typu zarządzanego węzła.</span><span class="sxs-lookup"><span data-stu-id="71177-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="71177-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="71177-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="71177-133">Pobierz szczegóły usługi programu Service Fabric w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="71177-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="71177-134">Nowe — AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71177-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="71177-135">Utwórz nową aplikację sieci szkieletowej usługi w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="71177-136">Nowe — AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71177-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="71177-137">Utwórz nowy typ aplikacji sieci szkieletowej usług pod określoną grupą zasobów i klastrem.</span><span class="sxs-lookup"><span data-stu-id="71177-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="71177-138">Nowe — AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71177-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="71177-139">Tworzenie nowej wersji typu aplikacji w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="71177-140">Nowe — AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="71177-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="71177-141">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="71177-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="71177-142">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="71177-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="71177-143">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="71177-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="71177-144">Nowe — AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="71177-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="71177-145">Tworzenie nowego zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="71177-146">Nowe — AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="71177-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="71177-147">Tworzenie nowego zasobu typu węzeł.</span><span class="sxs-lookup"><span data-stu-id="71177-147">Create new node type resource.</span></span>

### [<span data-ttu-id="71177-148">Nowe — AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="71177-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="71177-149">Tworzenie nowej usługi programu Fabric Service w ramach określonej aplikacji i klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="71177-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71177-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="71177-151">Usuwanie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-151">Remove an application from the cluster.</span></span> <span data-ttu-id="71177-152">Spowoduje to usunięcie wszystkich usług objętych aplikacją.</span><span class="sxs-lookup"><span data-stu-id="71177-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="71177-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71177-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="71177-154">Usuwanie usługi Fabric typ aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="71177-155">Spowoduje to usunięcie wszystkich wersji typów w obszarze ten zasób.</span><span class="sxs-lookup"><span data-stu-id="71177-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="71177-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71177-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="71177-157">Usuwanie usługi sieci szkieletowej w wersji typu aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="71177-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="71177-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="71177-159">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="71177-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="71177-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="71177-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="71177-161">Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="71177-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="71177-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="71177-163">Usuń zasób klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="71177-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="71177-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="71177-165">Remvoe certyfikat klienta według odcisku palca lub nazwy pospolitej.</span><span class="sxs-lookup"><span data-stu-id="71177-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="71177-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="71177-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="71177-167">Usuwanie typu węzła lub określonych węzłów w obrębie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="71177-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="71177-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="71177-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="71177-169">Usuń rozszerzenie maszyny wirtualnej z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="71177-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="71177-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="71177-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="71177-171">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="71177-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="71177-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="71177-173">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="71177-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="71177-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="71177-175">Usuwanie usługi z klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="71177-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="71177-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="71177-177">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="71177-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="71177-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="71177-179">Ponownie uruchom określone węzły z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="71177-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="71177-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="71177-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="71177-181">Ustawianie właściwości zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="71177-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="71177-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="71177-183">Ustawia właściwości zasobu typu węzła lub uruchamia akcje ponownego tworzenia obrazów dla konkretnej usługi NDES typu węzła z parametrem-Reimage.</span><span class="sxs-lookup"><span data-stu-id="71177-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="71177-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="71177-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="71177-185">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="71177-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="71177-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="71177-187">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="71177-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="71177-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71177-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="71177-189">Aktualizowanie aplikacji sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="71177-189">Update a service fabric application.</span></span> <span data-ttu-id="71177-190">Umożliwia to zaktualizowanie parametrów aplikacji i/lub uaktualnienie wersji typu aplikacji, która wyzwoli uaktualnienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="71177-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="71177-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="71177-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="71177-192">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="71177-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="71177-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="71177-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="71177-194">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="71177-194">Update the reliability tier of the primary node type in a cluster.</span></span>

