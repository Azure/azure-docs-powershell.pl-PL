---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522561"
---
# <span data-ttu-id="cc236-101">Moduł AzureRM. servicefabric</span><span class="sxs-lookup"><span data-stu-id="cc236-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="cc236-102">Opis</span><span class="sxs-lookup"><span data-stu-id="cc236-102">Description</span></span>
<span data-ttu-id="cc236-103">Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.</span><span class="sxs-lookup"><span data-stu-id="cc236-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="cc236-104">Polecenia cmdlet AzureRM. servicefabric</span><span class="sxs-lookup"><span data-stu-id="cc236-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="cc236-105">Dodaj-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="cc236-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="cc236-106">Dodawanie certyfikatu, który będzie służył jako certyfikat aplikacji</span><span class="sxs-lookup"><span data-stu-id="cc236-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="cc236-107">Dodaj-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc236-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="cc236-108">Dodawanie nazwy pospolitej lub odcisku palca do ustawień klastra dla uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="cc236-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="cc236-109">Dodaj-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cc236-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="cc236-110">Dodawanie pomocniczego certyfikatu klastra do klastra w celu przetaczania istniejącego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="cc236-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="cc236-111">Dodaj-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="cc236-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="cc236-112">Dodawanie węzłów/maszyn wirtualnych do określonego typu węzła do klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="cc236-113">Dodaj-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="cc236-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="cc236-114">Dodawanie typu węzła/maszyn wirtualnych do istniejącego klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="cc236-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cc236-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="cc236-116">Uzyskiwanie szczegółowych informacji o zasobie klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="cc236-117">Nowe — AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cc236-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="cc236-118">Utwórz nowy klaster servicefabric.</span><span class="sxs-lookup"><span data-stu-id="cc236-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="cc236-119">To polecenie ma wiele przeciążeń, które obejmują różne scenariusze</span><span class="sxs-lookup"><span data-stu-id="cc236-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="cc236-120">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc236-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="cc236-121">Usuwanie certyfikatu klienta z używania w celu uzyskania dostępu do klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="cc236-122">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cc236-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="cc236-123">Usuwanie certyfikatu klastra za pomocą zabezpieczeń klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="cc236-124">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="cc236-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="cc236-125">Usuwanie węzłów z określonego typu węzła z poziomu klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="cc236-126">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="cc236-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="cc236-127">Usuwanie typu węzła z klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="cc236-128">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="cc236-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="cc236-129">Usuwanie z klastra co najmniej jednego ustawienia usługi servicefabric</span><span class="sxs-lookup"><span data-stu-id="cc236-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="cc236-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="cc236-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="cc236-131">Dodawanie lub aktualizowanie co najmniej jednego ustawienia usługi servicefabric do klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="cc236-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="cc236-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="cc236-133">Zmienianie typu uaktualnienia usługi servicefabric dla klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="cc236-134">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="cc236-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="cc236-135">Zmienianie warstwy trwałości klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="cc236-136">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="cc236-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="cc236-137">Zmienianie warstwy niezawodności klastra</span><span class="sxs-lookup"><span data-stu-id="cc236-137">Change the reliability tier of a cluster</span></span>
