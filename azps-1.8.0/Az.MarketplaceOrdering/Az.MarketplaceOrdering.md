---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93704344"
---
# <span data-ttu-id="88fdb-101">AZ. MarketplaceOrdering, moduł</span><span class="sxs-lookup"><span data-stu-id="88fdb-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="88fdb-102">Opis</span><span class="sxs-lookup"><span data-stu-id="88fdb-102">Description</span></span>
<span data-ttu-id="88fdb-103">W tematach w tej sekcji opisano polecenia cmdlet usługi Azure PowerShell dla usługi Azure MarketplaceOrdering w strukturze Menedżera zasobów platformy Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="88fdb-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="88fdb-104">Polecenia cmdlet istnieją w przestrzeni nazw Microsoft. Azure. Command. MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="88fdb-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="88fdb-105">Te polecenia cmdlet umożliwiają użytkownikom platformy Azure akceptowanie postanowień prawnych dotyczących oferty rynkowej, które pozwalają na wdrożenie programistyczne tych rozwiązań.</span><span class="sxs-lookup"><span data-stu-id="88fdb-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="88fdb-106">Użytkownicy mogą również odrzucić zestaw warunków prawnych, które zostały już zaakceptowane.</span><span class="sxs-lookup"><span data-stu-id="88fdb-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="88fdb-107">AZ. MarketplaceOrdering polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="88fdb-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="88fdb-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="88fdb-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="88fdb-109">Pobierz warunki umowy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="88fdb-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="88fdb-110">W celu zaakceptowania warunków prawnych należy przekazać do Set-AzMarketplaceTerms obiekt warunki, który jest zwracany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="88fdb-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="88fdb-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="88fdb-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="88fdb-112">Zaakceptuj lub Odrzuć warunki związane z danym identyfikatorem wydawcy (wydawcy), identyfikatorem oferty (produktu) i identyfikatorem planu (Name).</span><span class="sxs-lookup"><span data-stu-id="88fdb-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="88fdb-113">Skorzystaj z Get-AzMarketplaceTerms, aby uzyskać postanowienia umowy.</span><span class="sxs-lookup"><span data-stu-id="88fdb-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

