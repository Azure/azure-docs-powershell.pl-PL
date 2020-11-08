---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220207"
---
# AZ. moduł pomocy technicznej
## Opis
W tematach w tej sekcji opisano polecenia cmdlet programu Azure PowerShell dotyczące tworzenia biletów usługi Azure support i zarządzania nimi w ramach usługi Azure Resource Manager (ARM). Polecenia cmdlet istnieją w obszarze nazw Microsoft. Azure. Commands. Support

## AZ. Obsługa poleceń cmdlet
### [Get-AzSupportService](Get-AzSupportService.md)
Pobiera bieżącą listę usług platformy Azure, dla której jest dostępna obsługa. Każda usługa Azure ma swój własny zestaw kategorii o nazwie Klasyfikacja problemu. Zapoznaj się z bieżącą listą klasyfikacji problemu dla usługi, korzystając z polecenia Get-AzSupportProblemClassification. Możesz użyć identyfikatora GUID usługi i klasyfikacji problemu, aby utworzyć nowy bilet pomocy technicznej przy użyciu nowych-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Pobiera bieżącą listę klasyfikacji problemu dla usługi platformy Azure. Możesz użyć identyfikatora GUID usługi i klasyfikacji problemu, aby utworzyć nowy bilet pomocy technicznej przy użyciu nowych-AzSupportTicket. 

### [Nowe — AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Polecenie cmdlet Helper, aby utworzyć obiekt profilu kontaktu pomocy technicznej. Za pomocą tego obiektu można New-AzSupportTicket polecenia cmdlet.

### [Nowe — AzSupportTicket](New-AzSupportTicket.md)
Tworzy nowy bilet pomocy technicznej platformy Azure. Ta operacja jest modelowana na temat zachowania [nowej strony żądania obsługi](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)platformy Azure.

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Pobiera listę biletów pomocy technicznej. Możesz uzyskać pełne informacje o biletach pomocy technicznej według nazwy biletu lub filtrować bilety pomocy technicznej według *statusu* lub *polach CreatedDate*.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Zaktualizuj ważność biletu pomocy technicznej, status lub dane kontaktowe klienta.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Pobiera komunikat o pomocy technicznej. Możesz również filtrować powiadomienia biletów pomocy technicznej według *polach CreatedDate*   lub *komunikacji*. 

### [Nowe — AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Dodaje nową komunikację z klientem do biletu pomocy technicznej platformy Azure. 



