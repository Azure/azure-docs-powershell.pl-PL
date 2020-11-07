---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2019
ms.locfileid: "93704554"
---
# <span data-ttu-id="6d445-101">AZ. ManagedServices, moduł</span><span class="sxs-lookup"><span data-stu-id="6d445-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="6d445-102">Opis</span><span class="sxs-lookup"><span data-stu-id="6d445-102">Description</span></span>
<span data-ttu-id="6d445-103">Ta funkcja jest używana przez klientów zarządzanych dostawców usług (MSPs).</span><span class="sxs-lookup"><span data-stu-id="6d445-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="6d445-104">Klienci oferują MSP możliwość zarządzania abonamentem.</span><span class="sxs-lookup"><span data-stu-id="6d445-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="6d445-105">Oprócz udzielania dostępu klient może również usuwać lub wyświetlać istniejące delegacje programu Access.</span><span class="sxs-lookup"><span data-stu-id="6d445-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="6d445-106">MSPs mogą wyświetlać listę klientów, którym udzielono im dostępu do abonamentów.</span><span class="sxs-lookup"><span data-stu-id="6d445-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="6d445-107">Ten proces obejmuje dwa obiekty: definicja rejestracji określająca MSP i definicje ról przydzielone do pliku MSP.</span><span class="sxs-lookup"><span data-stu-id="6d445-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="6d445-108">MSP może opcjonalnie zdefiniować ten obiekt, korzystając ze sklepu z usługami zarządzanymi oferującymi przypisania dostępu, które kojarzą abonament z definicją.</span><span class="sxs-lookup"><span data-stu-id="6d445-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="6d445-109">AZ. ManagedServices polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="6d445-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="6d445-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6d445-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="6d445-111">Pobiera listę przydziałów rejestracji.</span><span class="sxs-lookup"><span data-stu-id="6d445-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="6d445-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6d445-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="6d445-113">Pobiera listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="6d445-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="6d445-114">Nowe — AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6d445-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="6d445-115">Umożliwia utworzenie zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="6d445-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="6d445-116">Nowe — AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6d445-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="6d445-117">Tworzy definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="6d445-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="6d445-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6d445-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="6d445-119">Umożliwia usunięcie zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="6d445-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="6d445-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6d445-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="6d445-121">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="6d445-121">Deletes the registration definition.</span></span>

