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
# Moduł AzureRM. MarketplaceOrdering
## Opis
W tematach w tej sekcji opisano polecenia cmdlet usługi Azure PowerShell dla usługi Azure MarketplaceOrdering w strukturze Menedżera zasobów platformy Azure (ARM). Polecenia cmdlet istnieją w przestrzeni nazw Microsoft. Azure. Command. MarketplaceOrdering. Te polecenia cmdlet umożliwiają użytkownikom platformy Azure akceptowanie postanowień prawnych dotyczących oferty rynkowej umożliwiającej dalsze wdrażanie programmtic dla tych rozwiązań. Użytkownicy mogą również odrzucić zestaw warunków prawnych, które zostały już zaakceptowane.

## Polecenia cmdlet AzureRM. MarketplaceOrdering
### [Get-AzureRmMarketplaceTerms](Get-AzureRmMarketplaceTerms.md)
Pobierz warunki umowy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name). W celu zaakceptowania warunków prawnych należy przekazać do Set-AzureRmMarketplaceTerms obiekt warunki, który jest zwracany przez to polecenie.

### [Set-AzureRmMarketplaceTerms](Set-AzureRmMarketplaceTerms.md)
Zaakceptuj lub Odrzuć postanowienia prawne dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name). Skorzystaj z Get-AzureRmMarketplaceTerms, aby uzyskać postanowienia umowy.

