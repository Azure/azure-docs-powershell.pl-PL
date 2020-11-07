---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 4194899ad20356c8cde68110553495558d3816d5
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/17/2019
ms.locfileid: "93704398"
---
# <span data-ttu-id="7675b-101">AZS. COMPUTE. module</span><span class="sxs-lookup"><span data-stu-id="7675b-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="7675b-102">Opis</span><span class="sxs-lookup"><span data-stu-id="7675b-102">Description</span></span>
<span data-ttu-id="7675b-103">Wersja zapoznawcza modułu operatorów obliczeniowych AzureStack, która udostępnia funkcje do zarządzania przydziałami obliczeniowymi, obrazami platformy i rozszerzeniami maszyny wirtualnej oraz zadaniami migracji dysków zarządzanych w celu zrównoważenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="7675b-103">Preview release of the AzureStack Compute operator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="7675b-104">Polecenia cmdlet AZS. COMPUTE. admin</span><span class="sxs-lookup"><span data-stu-id="7675b-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="7675b-105">Dodaj-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="7675b-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="7675b-106">Dodaj obraz platformy maszyny wirtualnej z danej konfiguracji obrazu.</span><span class="sxs-lookup"><span data-stu-id="7675b-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="7675b-107">Dodaj-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="7675b-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="7675b-108">Tworzenie nowego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7675b-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="7675b-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="7675b-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="7675b-110">Zwraca przydziały określające limity przydziałów dla obiektów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="7675b-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="7675b-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="7675b-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="7675b-112">Zwraca listę zarządzanych dysków, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="7675b-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="7675b-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7675b-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="7675b-114">Zwraca listę zadań dotyczących migracji dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="7675b-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="7675b-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="7675b-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="7675b-116">Zwraca obrazy maszyny wirtualnej załadowane do repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="7675b-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="7675b-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="7675b-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="7675b-118">Zwraca dostępne obecnie rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7675b-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="7675b-119">Nowe — AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="7675b-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="7675b-120">Utwórz nowy przydział obliczania, który jest wykorzystywany do ograniczania zasobów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="7675b-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="7675b-121">Nowe — AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7675b-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="7675b-122">Rozpoczyna zadanie migracji dysków zarządzanych w celu migrowania zarządzanych dysków do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="7675b-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="7675b-123">Nowe — AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="7675b-123">New-AzsDataDiskObject</span></span>](New-AzsDataDiskObject.md)
<span data-ttu-id="7675b-124">Tworzy dysk danych, który służy do tworzenia nowego obrazu platformy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7675b-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="7675b-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="7675b-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="7675b-126">Usuwa określony przydział obliczania.</span><span class="sxs-lookup"><span data-stu-id="7675b-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="7675b-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="7675b-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="7675b-128">Usuwanie obrazu maszyny wirtualnej z repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="7675b-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="7675b-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="7675b-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="7675b-130">Umożliwia usunięcie obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7675b-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="7675b-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="7675b-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="7675b-132">Zaktualizuj istniejący przydział obliczeń przy użyciu podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="7675b-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="7675b-133">Zatrzymaj — AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7675b-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="7675b-134">Anulowanie zadania zarządzanego migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="7675b-134">Cancel a managed disk migration job.</span></span>

