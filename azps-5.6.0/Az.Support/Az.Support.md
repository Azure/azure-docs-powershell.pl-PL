---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979114"
---
# Moduł az.support
## Opis
Tematy w tej sekcji dokumentują polecenia cmdlet programu Azure PowerShell do tworzenia biletów pomocy technicznej platformy Azure i zarządzania nimi w ramach usługi Azure Resource Manager (ARM). Polecenia cmdlet istnieją w przestrzeni nazw Microsoft.Azure.Commands.Support

## Az.Support Cmdlet
### [Get-AzSupportService](Get-AzSupportService.md)
Pobiera bieżącą listę usług platformy Azure, dla których jest dostępna pomoc techniczna. Każda usługa Azure ma własny zestaw kategorii nazywany klasyfikacją problemu. Pobierz bieżącą listę klasyfikacji problemów dla usługi za pomocą funkcji Get-AzSupportProblemClassification. Za pomocą identyfikatora GUID klasyfikacji usługi i problemu możesz utworzyć nowy bilet pomocy technicznej przy użyciu new-azSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Pobiera bieżącą listę klasyfikacji problemów dla usługi Azure. Za pomocą identyfikatora GUID klasyfikacji usługi i problemu możesz utworzyć nowy bilet pomocy technicznej przy użyciu new-azSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Polecenie cmdlet helper w celu utworzenia obiektu profilu kontaktu pomocy technicznej. Tego obiektu można użyć do New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Tworzy nowy bilet pomocy technicznej platformy Azure. Ta operacja jest modelowana na zachowaniu strony wniosku o pomoc techniczną Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Pobiera listę biletów pomocy technicznej. Możesz uzyskać szczegółowe informacje o biletach pomocy technicznej według nazwy biletu lub filtrować bilety pomocy technicznej według *stanu* *lub pola CreatedDate.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Zaktualizuj ważność biletu pomocy technicznej, stan lub dane kontaktowe klienta.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Pobiera informacje na zgłoszenie do pomocy technicznej. Możesz również filtrować informacje o biletach pomocy technicznej *według typu CreatedDate* lub *CommunicationType.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Dodaje nową komunikację z klientami do biletu pomocy technicznej platformy Azure. 



