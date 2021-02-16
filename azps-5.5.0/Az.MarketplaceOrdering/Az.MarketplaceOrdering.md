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
# Az.MarketplaceOrdering Module
## Opis
Tematy w tej sekcji dokumentuj polecenia cmdlet programu Azure PowerShell dla usługi Azure MarketplaceOrdering w ramach usługi Azure Resource Manager (ARM). Polecenia cmdlet istnieją w przestrzeni nazw Microsoft.Azure.Commands.MarketplaceOrdering. Te polecenia cmdlet umożliwiają użytkownikom platformy Azure zaakceptowanie postanowień prawnych witryny marketplace oferującej dalsze wdrożenie programowe tych rozwiązań. Użytkownicy mogą również odrzucić zaakceptowany wcześniej zestaw warunków prawnych.

## Az.MarketplaceOrdering Cmdlet
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Uzyskaj warunki umowy dotyczące danego identyfikatora wydawcy(Publisher), identyfikatora oferty(Produktu) i identyfikatora planu (Nazwa). Obiekt "terminy" zwrócony za pomocą tego polecenia powinien zostać przekazany Set-AzMarketplaceTerms w celu zaakceptowania postanowień prawnych.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Akceptowanie lub odrzucanie warunków dla danego identyfikatora wydawcy(Publisher), identyfikatora oferty (Produkt) i identyfikatora planu (Nazwa). Skorzystaj z Get-AzMarketplaceTerms, aby uzyskać warunki umowy.

