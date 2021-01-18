---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501442"
---
# <span data-ttu-id="9ccbe-101">AZ. ManagedServices, moduł</span><span class="sxs-lookup"><span data-stu-id="9ccbe-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="9ccbe-102">Opis</span><span class="sxs-lookup"><span data-stu-id="9ccbe-102">Description</span></span>
<span data-ttu-id="9ccbe-103">Ta funkcja jest używana przez klientów zarządzanych dostawców usług (MSPs).</span><span class="sxs-lookup"><span data-stu-id="9ccbe-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="9ccbe-104">Klienci oferują MSP możliwość zarządzania abonamentem lub grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="9ccbe-105">Oprócz udzielania dostępu klient może również usunąć dostęp lub wyświetlić istniejący dostęp.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="9ccbe-106">MSPs mogą wyświetlać listę klientów, którym udzielono im dostępu do abonamentów.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="9ccbe-107">Ten proces obejmuje dwa obiekty: definicja rejestracji określająca MSP i definicje ról przyznane użytkownikom MSP.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="9ccbe-108">MSP może opcjonalnie zdefiniować ten obiekt, korzystając ze sklepu z usługami zarządzanymi oferującymi przypisania dostępu, które kojarzą abonament z definicją.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="9ccbe-109">AZ. ManagedServices polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="9ccbe-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="9ccbe-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="9ccbe-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="9ccbe-111">Pobiera określone zadanie rejestracji lub listę przydziałów rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="9ccbe-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9ccbe-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="9ccbe-113">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="9ccbe-114">Nowe — AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="9ccbe-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="9ccbe-115">Umożliwia utworzenie lub zaktualizowanie zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="9ccbe-116">Nowe — AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9ccbe-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="9ccbe-117">Tworzenie lub aktualizowanie definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="9ccbe-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="9ccbe-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="9ccbe-119">Usuwa zadanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="9ccbe-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9ccbe-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="9ccbe-121">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9ccbe-121">Removes a registration definition.</span></span>
