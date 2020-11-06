---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: f1446494d4eb68195ec0cefba248f519039a91ce
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522362"
---
# <span data-ttu-id="08c35-101">Moduł AzureRM. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="08c35-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="08c35-102">Opis</span><span class="sxs-lookup"><span data-stu-id="08c35-102">Description</span></span>
<span data-ttu-id="08c35-103">W tematach w tej sekcji opisano polecenia cmdlet usługi Azure PowerShell dla usługi Azure MarketplaceOrdering w strukturze Menedżera zasobów platformy Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="08c35-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="08c35-104">Polecenia cmdlet istnieją w przestrzeni nazw Microsoft. Azure. Command. MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="08c35-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="08c35-105">Te polecenia cmdlet umożliwiają użytkownikom platformy Azure akceptowanie postanowień prawnych dotyczących oferty rynkowej umożliwiającej dalsze wdrażanie programmtic dla tych rozwiązań.</span><span class="sxs-lookup"><span data-stu-id="08c35-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmtic deployment for these solutions.</span></span> <span data-ttu-id="08c35-106">Użytkownicy mogą również odrzucić zestaw warunków prawnych, które zostały już zaakceptowane.</span><span class="sxs-lookup"><span data-stu-id="08c35-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="08c35-107">Polecenia cmdlet AzureRM. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="08c35-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="08c35-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="08c35-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="08c35-109">Pobierz warunki umowy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="08c35-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="08c35-110">W celu zaakceptowania warunków prawnych należy przekazać do Set-AzureRmMarketplaceTerms obiekt warunki, który jest zwracany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="08c35-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="08c35-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="08c35-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="08c35-112">Zaakceptuj lub Odrzuć postanowienia prawne dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="08c35-112">Accept or reject the legal terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="08c35-113">Skorzystaj z Get-AzureRmMarketplaceTerms, aby uzyskać postanowienia umowy.</span><span class="sxs-lookup"><span data-stu-id="08c35-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>
