---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 33c6f65e258ee16b0ffb6a4616ffd1c7c5f16c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962906"
---
# <span data-ttu-id="316ea-101">Moduł Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="316ea-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="316ea-102">Opis</span><span class="sxs-lookup"><span data-stu-id="316ea-102">Description</span></span>
<span data-ttu-id="316ea-103">Ta funkcja jest używana przez klientów dostawców usług zarządzanych (MSP).</span><span class="sxs-lookup"><span data-stu-id="316ea-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="316ea-104">Klienci zapewniają programowi MSP możliwość zarządzania swoją grupą subskrypcji lub zasobów.</span><span class="sxs-lookup"><span data-stu-id="316ea-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="316ea-105">Oprócz udzielenia dostępu klient może również usunąć dostęp lub wyświetlić istniejący dostęp.</span><span class="sxs-lookup"><span data-stu-id="316ea-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="316ea-106">Klienci, którzy przyznali im dostęp do subskrypcji, mogą wyświetlać listę klientów.</span><span class="sxs-lookup"><span data-stu-id="316ea-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="316ea-107">W tym procesie biorą udział dwa obiekty: definicja rejestracji identyfikująca program MSP i definicje ról, które zostały udzielone użytkownikom tego oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="316ea-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="316ea-108">Program MSP może opcjonalnie zdefiniować ten obiekt przy użyciu witryny marketplace usług zarządzanych oferującej przypisania programu Access, które skojarzą subskrypcję z definicją.</span><span class="sxs-lookup"><span data-stu-id="316ea-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="316ea-109">Az.ManagedServices Cmdlet</span><span class="sxs-lookup"><span data-stu-id="316ea-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="316ea-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="316ea-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="316ea-111">Pobiera konkretne zadanie rejestru lub listę zadań rejestracji.</span><span class="sxs-lookup"><span data-stu-id="316ea-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="316ea-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="316ea-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="316ea-113">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="316ea-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="316ea-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="316ea-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="316ea-115">Tworzy lub aktualizuje zadanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="316ea-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="316ea-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="316ea-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="316ea-117">Tworzy lub aktualizuje definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="316ea-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="316ea-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="316ea-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="316ea-119">Usuwa przypisanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="316ea-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="316ea-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="316ea-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="316ea-121">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="316ea-121">Removes a registration definition.</span></span>
