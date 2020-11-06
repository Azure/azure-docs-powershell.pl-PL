---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523398"
---
# Get-AzureRmSubscription

## STRESZCZENIe
Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.

## POLECENIA

### ListByIdInTenant (domyślny)
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### ListByNameInTenant
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzureRmSubscription Pobiera identyfikator subskrypcji, nazwę subskrypcji i dzierżawę domową dla subskrypcji, do których może uzyskać dostęp bieżące konto.

## Przykłady

### Przykład 1. Uzyskaj wszystkie subskrypcje we wszystkich dzierżawach
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

To polecenie pobiera wszystkie subskrypcje wszystkich dzierżawców autoryzowanych jako bieżące konto.

### Przykład 2: uzyskiwanie wszystkich subskrypcji dla konkretnego dzierżawy
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

Wyświetlanie wszystkich subskrypcji w danej dzierżawie autoryzowanych dla bieżącego konta.

### Przykład 3: uzyskiwanie wszystkich subskrypcji w bieżącej dzierżawie
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

To polecenie umożliwia pobieranie wszystkich subskrypcji w bieżącej dzierżawie autoryzowanych dla bieżącego użytkownika.

### Przykład 4: Zmienianie bieżącego kontekstu w celu korzystania z określonej subskrypcji
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

To polecenie pobiera określoną subskrypcję, a następnie ustawia bieżący kontekst, aby go używać.
Wszystkie kolejne polecenia cmdlet w tej sesji domyślnie używają nowego abonamentu (subskrypcja contoso 1).

## PARAMETRÓW

### -Subskrypcji
Określa identyfikator subskrypcji, którą należy uzyskać.

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Określa nazwę subskrypcji, którą należy uzyskać.

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Dzierżawy
Określa identyfikator dzierżawy, który zawiera abonamenty do pobrania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### PSAzureSubscription

## INFORMACYJN

## LINKI POKREWNE

