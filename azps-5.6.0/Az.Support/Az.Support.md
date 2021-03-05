---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979114"
---
# <span data-ttu-id="18bb4-101">Moduł az.support</span><span class="sxs-lookup"><span data-stu-id="18bb4-101">Az.Support Module</span></span>
## <span data-ttu-id="18bb4-102">Opis</span><span class="sxs-lookup"><span data-stu-id="18bb4-102">Description</span></span>
<span data-ttu-id="18bb4-103">Tematy w tej sekcji dokumentują polecenia cmdlet programu Azure PowerShell do tworzenia biletów pomocy technicznej platformy Azure i zarządzania nimi w ramach usługi Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="18bb4-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="18bb4-104">Polecenia cmdlet istnieją w przestrzeni nazw Microsoft.Azure.Commands.Support</span><span class="sxs-lookup"><span data-stu-id="18bb4-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="18bb4-105">Az.Support Cmdlet</span><span class="sxs-lookup"><span data-stu-id="18bb4-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="18bb4-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="18bb4-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="18bb4-107">Pobiera bieżącą listę usług platformy Azure, dla których jest dostępna pomoc techniczna.</span><span class="sxs-lookup"><span data-stu-id="18bb4-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="18bb4-108">Każda usługa Azure ma własny zestaw kategorii nazywany klasyfikacją problemu.</span><span class="sxs-lookup"><span data-stu-id="18bb4-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="18bb4-109">Pobierz bieżącą listę klasyfikacji problemów dla usługi za pomocą funkcji Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="18bb4-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="18bb4-110">Za pomocą identyfikatora GUID klasyfikacji usługi i problemu możesz utworzyć nowy bilet pomocy technicznej przy użyciu new-azSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="18bb4-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="18bb4-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="18bb4-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="18bb4-112">Pobiera bieżącą listę klasyfikacji problemów dla usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="18bb4-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="18bb4-113">Za pomocą identyfikatora GUID klasyfikacji usługi i problemu możesz utworzyć nowy bilet pomocy technicznej przy użyciu new-azSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="18bb4-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="18bb4-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="18bb4-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="18bb4-115">Polecenie cmdlet helper w celu utworzenia obiektu profilu kontaktu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="18bb4-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="18bb4-116">Tego obiektu można użyć do New-AzSupportTicket cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18bb4-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="18bb4-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="18bb4-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="18bb4-118">Tworzy nowy bilet pomocy technicznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18bb4-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="18bb4-119">Ta operacja jest modelowana na zachowaniu strony wniosku o pomoc techniczną Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="18bb4-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="18bb4-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="18bb4-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="18bb4-121">Pobiera listę biletów pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="18bb4-121">Gets the list of support tickets.</span></span> <span data-ttu-id="18bb4-122">Możesz uzyskać szczegółowe informacje o biletach pomocy technicznej według nazwy biletu lub filtrować bilety pomocy technicznej według *stanu* *lub pola CreatedDate.*</span><span class="sxs-lookup"><span data-stu-id="18bb4-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="18bb4-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="18bb4-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="18bb4-124">Zaktualizuj ważność biletu pomocy technicznej, stan lub dane kontaktowe klienta.</span><span class="sxs-lookup"><span data-stu-id="18bb4-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="18bb4-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="18bb4-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="18bb4-126">Pobiera informacje na zgłoszenie do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="18bb4-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="18bb4-127">Możesz również filtrować informacje o biletach pomocy technicznej *według typu CreatedDate* lub *CommunicationType.*</span><span class="sxs-lookup"><span data-stu-id="18bb4-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="18bb4-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="18bb4-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="18bb4-129">Dodaje nową komunikację z klientami do biletu pomocy technicznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18bb4-129">Adds a new customer communication to an Azure support ticket.</span></span> 



