---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963626"
---
# <span data-ttu-id="62268-101">Moduł Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="62268-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="62268-102">Opis</span><span class="sxs-lookup"><span data-stu-id="62268-102">Description</span></span>
<span data-ttu-id="62268-103">Moduł Azure Service Fabric, za pomocą który można zautomatyzować operacje end-2-end, takie jak tworzenie bezpiecznego klastrów, przewczasowanie certyfikatów klastrów, dodawanie lub usunięcie węzłów z klastrem itp. Poniżej znajduje się pełna lista wszystkich operacji.</span><span class="sxs-lookup"><span data-stu-id="62268-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="62268-104">Az.ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="62268-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="62268-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62268-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="62268-106">Dodaj nazwę pospolitą lub thumbprint do klastrów na potrzeby uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="62268-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="62268-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="62268-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="62268-108">Dodawanie certyfikatu klasteru pomocniczego do klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="62268-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62268-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="62268-110">Dodaj nazwę pospolitą certyfikatu lub thumbprint do klastra.</span><span class="sxs-lookup"><span data-stu-id="62268-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="62268-111">Spowoduje to zarejestrowanie certyfikatu ponownie dla klastrów na potrzeby uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="62268-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="62268-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="62268-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="62268-113">Dodaj rozszerzenie maszyny wirtualnej do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="62268-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="62268-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="62268-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="62268-115">Dodaj klucz tajny certyfikatu do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="62268-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="62268-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="62268-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="62268-117">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="62268-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="62268-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="62268-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="62268-119">Dodaj nowy typ węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="62268-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="62268-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="62268-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="62268-121">Uzyskaj szczegóły aplikacji Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="62268-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="62268-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="62268-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="62268-123">Uzyskaj szczegółowe informacje o typie aplikacji Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="62268-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="62268-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="62268-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="62268-125">Uzyskaj szczegółowe informacje o wersji typu materiału usługowego.</span><span class="sxs-lookup"><span data-stu-id="62268-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="62268-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="62268-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="62268-127">Pobierz szczegóły zasobów klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="62268-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="62268-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="62268-129">Uzyskaj szczegółowe informacje dotyczące zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="62268-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="62268-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="62268-131">Pobierz szczegóły zasobu typu węzła zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="62268-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="62268-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="62268-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="62268-133">Uzyskaj szczegóły usługi Service Fabric w ramach określonej aplikacji i klastra.</span><span class="sxs-lookup"><span data-stu-id="62268-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="62268-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="62268-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="62268-135">Utwórz nową aplikację szkieletową usług w ramach określonej grupy zasobów i klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="62268-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="62268-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="62268-137">Utwórz nowy typ aplikacji sieci szkieletowej usług w ramach określonej grupy zasobów i klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="62268-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="62268-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="62268-139">Utwórz nową wersję typu aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="62268-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="62268-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="62268-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="62268-141">To polecenie używa certyfikatów, które ty dostarczasz, lub certyfikatów wygenerowanych przez system z podpisem własnym w celu skonfigurowania nowego klastru materiału usługowego.</span><span class="sxs-lookup"><span data-stu-id="62268-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="62268-142">Może on używać szablonu domyślnego lub niestandardowego, który możesz udostępnić.</span><span class="sxs-lookup"><span data-stu-id="62268-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="62268-143">Możesz określić folder, aby wyeksportować certyfikaty z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="62268-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="62268-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="62268-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="62268-145">Tworzenie nowego klastru zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="62268-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="62268-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="62268-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="62268-147">Tworzenie nowego zasobu typu węzła.</span><span class="sxs-lookup"><span data-stu-id="62268-147">Create new node type resource.</span></span>

### [<span data-ttu-id="62268-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="62268-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="62268-149">Utwórz nową usługę szkieletową usług w ramach określonej aplikacji i klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="62268-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="62268-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="62268-151">Usuń aplikację z klastra.</span><span class="sxs-lookup"><span data-stu-id="62268-151">Remove an application from the cluster.</span></span> <span data-ttu-id="62268-152">Spowoduje to usunięcie wszystkich usług w ramach aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62268-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="62268-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="62268-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="62268-154">Usuń sieć szkieletową usługi z klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="62268-155">Spowoduje to usunięcie wszystkich wersji tego typu w ramach tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="62268-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="62268-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="62268-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="62268-157">Usuń sieć szkieletową usługi z wersji aplikacji o typie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62268-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="62268-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62268-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="62268-159">Usuwanie certyfikatów klientów lub podmiotów certyfikatów z uwierzytelniania klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="62268-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="62268-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="62268-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="62268-161">Usuwanie certyfikatu klastrów z zabezpieczeń klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="62268-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="62268-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="62268-163">Usuwanie zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="62268-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62268-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="62268-165">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="62268-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="62268-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="62268-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="62268-167">Usuń typ węzła lub określone węzły w obrębie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="62268-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="62268-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="62268-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="62268-169">Usuń rozszerzenie maszyny wirtualnej z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="62268-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="62268-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="62268-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="62268-171">Usuwanie węzłów z określonego typu węzła z klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="62268-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="62268-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="62268-173">Usuwanie pełnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="62268-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="62268-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="62268-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="62268-175">Usuń usługę z klastra.</span><span class="sxs-lookup"><span data-stu-id="62268-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="62268-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="62268-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="62268-177">Usuń jedno lub wiele ustawień usługi Fabric z klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="62268-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="62268-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="62268-179">Ponowne uruchamianie określonych węzłów z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="62268-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="62268-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="62268-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="62268-181">Ustawianie właściwości zasobów klastrów.</span><span class="sxs-lookup"><span data-stu-id="62268-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="62268-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="62268-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="62268-183">Ustawia właściwości zasobu typu węzła lub uruchamiaj akcje ponownego projektu dla określonych ndes typu węzła za pomocą parametru -Reimage.</span><span class="sxs-lookup"><span data-stu-id="62268-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="62268-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="62268-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="62268-185">Dodawanie lub aktualizowanie jednego lub wielu ustawień usługi Fabric do klastrowania.</span><span class="sxs-lookup"><span data-stu-id="62268-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="62268-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="62268-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="62268-187">Zmienianie typu uaktualniania sieci szkieletów usług w klastrze.</span><span class="sxs-lookup"><span data-stu-id="62268-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="62268-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="62268-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="62268-189">Aktualizowanie aplikacji do obsługi szkieletów usług.</span><span class="sxs-lookup"><span data-stu-id="62268-189">Update a service fabric application.</span></span> <span data-ttu-id="62268-190">Pozwala to zaktualizować parametry aplikacji i/lub uaktualnić wersję typu aplikacji, co spowoduje uruchomienie uaktualnienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62268-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="62268-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="62268-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="62268-192">Aktualizowanie warstwy niezawodności lub maszyny wirtualnej typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="62268-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="62268-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="62268-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="62268-194">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="62268-194">Update the reliability tier of the primary node type in a cluster.</span></span>

