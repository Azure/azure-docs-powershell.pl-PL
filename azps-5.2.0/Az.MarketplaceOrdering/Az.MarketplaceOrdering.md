---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329881"
---
# AZ. MarketplaceOrdering, moduł
## Opis
W tematach w tej sekcji opisano polecenia cmdlet usługi Azure PowerShell dla usługi Azure MarketplaceOrdering w strukturze Menedżera zasobów platformy Azure (ARM). Polecenia cmdlet istnieją w przestrzeni nazw Microsoft. Azure. Command. MarketplaceOrdering. Te polecenia cmdlet umożliwiają użytkownikom platformy Azure akceptowanie postanowień prawnych dotyczących oferty rynkowej, które pozwalają na wdrożenie programistyczne tych rozwiązań. Użytkownicy mogą również odrzucić zestaw warunków prawnych, które zostały już zaakceptowane.

## AZ. MarketplaceOrdering polecenia cmdlet
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Pobierz warunki umowy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name). W celu zaakceptowania warunków prawnych należy przekazać do Set-AzMarketplaceTerms obiekt warunki, który jest zwracany przez to polecenie.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Zaakceptuj lub Odrzuć warunki związane z danym identyfikatorem wydawcy (wydawcy), identyfikatorem oferty (produktu) i identyfikatorem planu (Name). Skorzystaj z Get-AzMarketplaceTerms, aby uzyskać postanowienia umowy.

