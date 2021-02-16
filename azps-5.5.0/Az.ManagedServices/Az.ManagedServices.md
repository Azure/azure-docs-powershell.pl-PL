---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187491"
---
# <span data-ttu-id="db953-101">Moduł Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="db953-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="db953-102">Opis</span><span class="sxs-lookup"><span data-stu-id="db953-102">Description</span></span>
<span data-ttu-id="db953-103">Ta funkcja jest używana przez klientów dostawców usług zarządzanych (MSP).</span><span class="sxs-lookup"><span data-stu-id="db953-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="db953-104">Klienci zapewniają programowi MSP możliwość zarządzania swoją grupą subskrypcji lub zasobów.</span><span class="sxs-lookup"><span data-stu-id="db953-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="db953-105">Oprócz udzielenia dostępu klient może również usunąć dostęp lub wyświetlić istniejący dostęp.</span><span class="sxs-lookup"><span data-stu-id="db953-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="db953-106">Klienci, którzy przyznali im dostęp do subskrypcji, mogą wyświetlać listę klientów.</span><span class="sxs-lookup"><span data-stu-id="db953-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="db953-107">W tym procesie biorą udział dwa obiekty: definicja rejestracji identyfikująca program MSP i definicje ról, które zostały udzielone użytkownikom tego oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="db953-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="db953-108">Program MSP może opcjonalnie zdefiniować ten obiekt przy użyciu witryny marketplace usług zarządzanych oferującej przypisania programu Access, które skojarzą subskrypcję z definicją.</span><span class="sxs-lookup"><span data-stu-id="db953-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="db953-109">Az.ManagedServices Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db953-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="db953-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="db953-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="db953-111">Pobiera konkretne zadanie rejestru lub listę zadań rejestracji.</span><span class="sxs-lookup"><span data-stu-id="db953-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="db953-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="db953-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="db953-113">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="db953-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="db953-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="db953-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="db953-115">Tworzy lub aktualizuje zadanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="db953-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="db953-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="db953-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="db953-117">Tworzy lub aktualizuje definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="db953-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="db953-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="db953-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="db953-119">Usuwa przypisanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="db953-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="db953-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="db953-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="db953-121">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="db953-121">Removes a registration definition.</span></span>
