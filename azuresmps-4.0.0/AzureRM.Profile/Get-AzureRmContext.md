---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523402"
---
# Get-AzureRmContext

## STRESZCZENIe
Pobiera metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.

## POLECENIA

```
Get-AzureRmContext [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzureRmContext pobiera bieżące metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.

To polecenie cmdlet umożliwia pobieranie konta usługi Active Directory, dzierżawy usługi Active Directory, subskrypcji platformy Azure i ukierunkowanego środowiska platformy Azure.
Polecenia cmdlet usługi Azure Resource Manager domyślnie wykorzystują te ustawienia podczas przeprowadzania żądań Menedżera zasobów platformy Azure.

## Przykłady

### Przykład 1. Uzyskiwanie bieżącego kontekstu
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

W tym przykładzie będziemy logować się na naszym koncie za pomocą subskrypcji usługi Azure przy użyciu dodatku Add-AzureRmAccount, a następnie uzyskujemy kontekst bieżącej sesji przez dzwonienie do funkcji Get-AzureRmContext.

## PARAMETRÓW

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### PSAzureContext
To polecenie cmdlet zwraca konto, dzierżawcę i subskrypcję używane przez polecenia cmdlet Menedżera zasobów platformy Azure.

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRMContext]()

