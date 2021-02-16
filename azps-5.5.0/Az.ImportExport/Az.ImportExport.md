---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194315"
---
# <span data-ttu-id="bfeb3-101">Moduł Az.ImportExport</span><span class="sxs-lookup"><span data-stu-id="bfeb3-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="bfeb3-102">Opis</span><span class="sxs-lookup"><span data-stu-id="bfeb3-102">Description</span></span>
<span data-ttu-id="bfeb3-103">Microsoft Azure PowerShell: Polecenie cmdlet ImportExport</span><span class="sxs-lookup"><span data-stu-id="bfeb3-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="bfeb3-104">Az.ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bfeb3-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="bfeb3-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="bfeb3-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="bfeb3-106">Pobiera informacje o istniejącym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="bfeb3-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="bfeb3-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="bfeb3-108">Zwraca klucze funkcji BitLocker dla wszystkich dysków w określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="bfeb3-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="bfeb3-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="bfeb3-110">Zwraca szczegółowe informacje o lokalizacji, w której można wysłać dyskietną skojarzoną z zadaniem importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="bfeb3-111">Lokalizacja to region platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="bfeb3-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="bfeb3-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="bfeb3-113">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="bfeb3-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="bfeb3-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="bfeb3-115">Utwórz obiekt DriverList for ImportExport.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="bfeb3-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="bfeb3-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="bfeb3-117">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-117">Deletes an existing job.</span></span>
<span data-ttu-id="bfeb3-118">Tylko zadania w stanach Tworzenie lub Wykonane można usuwać.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="bfeb3-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="bfeb3-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="bfeb3-120">Aktualizuje określone właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="bfeb3-121">Możesz wywołać tę operację, aby powiadomić usługę importowania/eksportowania, że dyski twarde wywchiwują zadanie importu lub eksportu do centrum danych firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="bfeb3-122">Za jego pomocą można także anulować istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="bfeb3-122">It can also be used to cancel an existing job.</span></span>

