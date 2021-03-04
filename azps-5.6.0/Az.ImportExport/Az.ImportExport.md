---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: cce265bc3d61f445c6843b0c1ca340ad921e1089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975786"
---
# <span data-ttu-id="983ad-101">Moduł Az.ImportExport</span><span class="sxs-lookup"><span data-stu-id="983ad-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="983ad-102">Opis</span><span class="sxs-lookup"><span data-stu-id="983ad-102">Description</span></span>
<span data-ttu-id="983ad-103">Microsoft Azure PowerShell: Polecenie cmdlet ImportExport</span><span class="sxs-lookup"><span data-stu-id="983ad-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="983ad-104">Az.ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="983ad-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="983ad-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="983ad-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="983ad-106">Pobiera informacje o istniejącym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="983ad-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="983ad-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="983ad-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="983ad-108">Zwraca klucze funkcji BitLocker dla wszystkich dysków w określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="983ad-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="983ad-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="983ad-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="983ad-110">Zwraca szczegółowe informacje o lokalizacji, do której można wysłać dyskietki skojarzone z zadaniem importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="983ad-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="983ad-111">Lokalizacja to region platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="983ad-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="983ad-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="983ad-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="983ad-113">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="983ad-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="983ad-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="983ad-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="983ad-115">Utwórz obiekt DriverList for ImportExport.</span><span class="sxs-lookup"><span data-stu-id="983ad-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="983ad-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="983ad-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="983ad-117">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="983ad-117">Deletes an existing job.</span></span>
<span data-ttu-id="983ad-118">Można usuwać tylko zadania w stanach Tworzenie lub Ukończone.</span><span class="sxs-lookup"><span data-stu-id="983ad-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="983ad-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="983ad-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="983ad-120">Aktualizuje określone właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="983ad-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="983ad-121">Tę operację można wywołać w celu powiadomienia usługi importowania/eksportowania, że dyski twarde wywchiwują zadanie importu lub eksportu do centrum danych firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="983ad-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="983ad-122">Za jego pomocą można także anulować istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="983ad-122">It can also be used to cancel an existing job.</span></span>

