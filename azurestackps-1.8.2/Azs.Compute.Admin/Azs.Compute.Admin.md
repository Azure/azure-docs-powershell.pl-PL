---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 8b74dd57a85a39403f56840dd0fc54b3f25184f1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055732"
---
# <span data-ttu-id="b20f6-101">AZS. COMPUTE. module</span><span class="sxs-lookup"><span data-stu-id="b20f6-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="b20f6-102">Opis</span><span class="sxs-lookup"><span data-stu-id="b20f6-102">Description</span></span>
<span data-ttu-id="b20f6-103">Wersja zapoznawcza modułu administratora AzureStack COMPUTE, która udostępnia funkcje umożliwiające zarządzanie przydziałami obliczeniowymi, obrazami platformy i rozszerzeniami maszyny wirtualnej oraz zadaniami migracji dysków zarządzanych w celu zrównoważenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="b20f6-103">Preview release of the AzureStack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="b20f6-104">Polecenia cmdlet AZS. COMPUTE. admin</span><span class="sxs-lookup"><span data-stu-id="b20f6-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="b20f6-105">Dodaj-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b20f6-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="b20f6-106">Dodaj obraz platformy maszyny wirtualnej z danej konfiguracji obrazu.</span><span class="sxs-lookup"><span data-stu-id="b20f6-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="b20f6-107">Dodaj-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b20f6-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="b20f6-108">Tworzenie nowego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b20f6-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="b20f6-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b20f6-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="b20f6-110">Zwraca przydziały określające limity przydziałów dla obiektów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="b20f6-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="b20f6-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="b20f6-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="b20f6-112">Zwraca listę zarządzanych dysków, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="b20f6-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="b20f6-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b20f6-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="b20f6-114">Zwraca listę zadań dotyczących migracji dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="b20f6-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="b20f6-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b20f6-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="b20f6-116">Zwraca obrazy maszyny wirtualnej załadowane do repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="b20f6-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="b20f6-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b20f6-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="b20f6-118">Zwraca dostępne obecnie rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b20f6-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="b20f6-119">Nowe — AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b20f6-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="b20f6-120">Utwórz nowy przydział obliczania, który jest wykorzystywany do ograniczania zasobów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="b20f6-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="b20f6-121">Nowe — AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b20f6-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="b20f6-122">Rozpoczyna zadanie migracji dysków zarządzanych w celu migrowania zarządzanych dysków do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="b20f6-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="b20f6-123">Nowy-datadyskobject</span><span class="sxs-lookup"><span data-stu-id="b20f6-123">New-DataDiskObject</span></span>](New-DataDiskObject.md)
<span data-ttu-id="b20f6-124">Tworzy dysk danych, który służy do tworzenia nowego obrazu platformy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b20f6-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="b20f6-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b20f6-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="b20f6-126">Usuwa określony przydział obliczania.</span><span class="sxs-lookup"><span data-stu-id="b20f6-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="b20f6-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b20f6-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="b20f6-128">Usuwanie obrazu maszyny wirtualnej z repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="b20f6-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="b20f6-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b20f6-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="b20f6-130">Umożliwia usunięcie obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b20f6-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="b20f6-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b20f6-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="b20f6-132">Zaktualizuj istniejący przydział obliczeń przy użyciu podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="b20f6-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="b20f6-133">Zatrzymaj — AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b20f6-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="b20f6-134">Anulowanie zadania zarządzanego migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="b20f6-134">Cancel a managed disk migration job.</span></span>

