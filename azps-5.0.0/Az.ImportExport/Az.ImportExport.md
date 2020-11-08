---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231839"
---
# <span data-ttu-id="7a757-101">AZ. ImportExport, moduł</span><span class="sxs-lookup"><span data-stu-id="7a757-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="7a757-102">Opis</span><span class="sxs-lookup"><span data-stu-id="7a757-102">Description</span></span>
<span data-ttu-id="7a757-103">Microsoft Azure PowerShell: polecenia cmdlet ImportExport</span><span class="sxs-lookup"><span data-stu-id="7a757-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="7a757-104">AZ. ImportExport polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a757-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="7a757-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="7a757-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="7a757-106">Pobiera informacje o istniejącym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="7a757-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="7a757-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="7a757-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="7a757-108">Zwraca klucze funkcji BitLocker dla wszystkich dysków w określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="7a757-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="7a757-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="7a757-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="7a757-110">Zwraca szczegóły dotyczące lokalizacji, do której można wysłać dyski skojarzone z zadaniem importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="7a757-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="7a757-111">Lokalizacja to obszar platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a757-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="7a757-112">Nowe — AzImportExport</span><span class="sxs-lookup"><span data-stu-id="7a757-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="7a757-113">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7a757-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="7a757-114">Nowe — AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="7a757-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="7a757-115">Utwórz obiekt DriverList dla ImportExport.</span><span class="sxs-lookup"><span data-stu-id="7a757-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="7a757-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="7a757-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="7a757-117">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="7a757-117">Deletes an existing job.</span></span>
<span data-ttu-id="7a757-118">Można usuwać tylko zadania w Stanach Tworzenie lub ukończone.</span><span class="sxs-lookup"><span data-stu-id="7a757-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="7a757-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="7a757-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="7a757-120">Aktualizuje określone właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="7a757-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="7a757-121">Możesz zadzwonić do tej operacji, aby powiadomić usługę importu/eksportu, że dyski twarde zawierające zadanie importu lub eksportu zostały wysłane do centrum danych firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7a757-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="7a757-122">Można go również użyć, aby anulować istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="7a757-122">It can also be used to cancel an existing job.</span></span>

