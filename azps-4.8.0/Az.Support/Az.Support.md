---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220207"
---
# <span data-ttu-id="60bd9-101">AZ. moduł pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="60bd9-101">Az.Support Module</span></span>
## <span data-ttu-id="60bd9-102">Opis</span><span class="sxs-lookup"><span data-stu-id="60bd9-102">Description</span></span>
<span data-ttu-id="60bd9-103">W tematach w tej sekcji opisano polecenia cmdlet programu Azure PowerShell dotyczące tworzenia biletów usługi Azure support i zarządzania nimi w ramach usługi Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="60bd9-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="60bd9-104">Polecenia cmdlet istnieją w obszarze nazw Microsoft. Azure. Commands. Support</span><span class="sxs-lookup"><span data-stu-id="60bd9-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="60bd9-105">AZ. Obsługa poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="60bd9-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="60bd9-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="60bd9-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="60bd9-107">Pobiera bieżącą listę usług platformy Azure, dla której jest dostępna obsługa.</span><span class="sxs-lookup"><span data-stu-id="60bd9-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="60bd9-108">Każda usługa Azure ma swój własny zestaw kategorii o nazwie Klasyfikacja problemu.</span><span class="sxs-lookup"><span data-stu-id="60bd9-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="60bd9-109">Zapoznaj się z bieżącą listą klasyfikacji problemu dla usługi, korzystając z polecenia Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="60bd9-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="60bd9-110">Możesz użyć identyfikatora GUID usługi i klasyfikacji problemu, aby utworzyć nowy bilet pomocy technicznej przy użyciu nowych-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="60bd9-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="60bd9-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="60bd9-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="60bd9-112">Pobiera bieżącą listę klasyfikacji problemu dla usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60bd9-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="60bd9-113">Możesz użyć identyfikatora GUID usługi i klasyfikacji problemu, aby utworzyć nowy bilet pomocy technicznej przy użyciu nowych-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="60bd9-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="60bd9-114">Nowe — AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="60bd9-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="60bd9-115">Polecenie cmdlet Helper, aby utworzyć obiekt profilu kontaktu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="60bd9-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="60bd9-116">Za pomocą tego obiektu można New-AzSupportTicket polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60bd9-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="60bd9-117">Nowe — AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="60bd9-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="60bd9-118">Tworzy nowy bilet pomocy technicznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60bd9-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="60bd9-119">Ta operacja jest modelowana na temat zachowania [nowej strony żądania obsługi](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60bd9-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="60bd9-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="60bd9-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="60bd9-121">Pobiera listę biletów pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="60bd9-121">Gets the list of support tickets.</span></span> <span data-ttu-id="60bd9-122">Możesz uzyskać pełne informacje o biletach pomocy technicznej według nazwy biletu lub filtrować bilety pomocy technicznej według *statusu* lub *polach CreatedDate*.</span><span class="sxs-lookup"><span data-stu-id="60bd9-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="60bd9-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="60bd9-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="60bd9-124">Zaktualizuj ważność biletu pomocy technicznej, status lub dane kontaktowe klienta.</span><span class="sxs-lookup"><span data-stu-id="60bd9-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="60bd9-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="60bd9-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="60bd9-126">Pobiera komunikat o pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="60bd9-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="60bd9-127">Możesz również filtrować powiadomienia biletów pomocy technicznej według *polach CreatedDate*   lub *komunikacji*.</span><span class="sxs-lookup"><span data-stu-id="60bd9-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="60bd9-128">Nowe — AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="60bd9-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="60bd9-129">Dodaje nową komunikację z klientem do biletu pomocy technicznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60bd9-129">Adds a new customer communication to an Azure support ticket.</span></span> 



