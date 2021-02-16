---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180266"
---
# <span data-ttu-id="d3ee1-101">Az.MarketplaceOrdering Module</span><span class="sxs-lookup"><span data-stu-id="d3ee1-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="d3ee1-102">Opis</span><span class="sxs-lookup"><span data-stu-id="d3ee1-102">Description</span></span>
<span data-ttu-id="d3ee1-103">Tematy w tej sekcji dokumentuj polecenia cmdlet programu Azure PowerShell dla usługi Azure MarketplaceOrdering w ramach usługi Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="d3ee1-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="d3ee1-104">Polecenia cmdlet istnieją w przestrzeni nazw Microsoft.Azure.Commands.MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="d3ee1-105">Te polecenia cmdlet umożliwiają użytkownikom platformy Azure zaakceptowanie postanowień prawnych witryny marketplace oferującej dalsze wdrożenie programowe tych rozwiązań.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="d3ee1-106">Użytkownicy mogą również odrzucić zaakceptowany wcześniej zestaw warunków prawnych.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="d3ee1-107">Az.MarketplaceOrdering Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d3ee1-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="d3ee1-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d3ee1-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="d3ee1-109">Uzyskaj warunki umowy dotyczące danego identyfikatora wydawcy(Publisher), identyfikatora oferty(Produktu) i identyfikatora planu (Nazwa).</span><span class="sxs-lookup"><span data-stu-id="d3ee1-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d3ee1-110">Obiekt "terminy" zwrócony za pomocą tego polecenia powinien zostać przekazany Set-AzMarketplaceTerms w celu zaakceptowania postanowień prawnych.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="d3ee1-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d3ee1-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="d3ee1-112">Akceptowanie lub odrzucanie warunków dla danego identyfikatora wydawcy(Publisher), identyfikatora oferty (Produkt) i identyfikatora planu (Nazwa).</span><span class="sxs-lookup"><span data-stu-id="d3ee1-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d3ee1-113">Skorzystaj z Get-AzMarketplaceTerms, aby uzyskać warunki umowy.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

