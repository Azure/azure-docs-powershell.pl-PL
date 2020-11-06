---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523554"
---
# Set-AzureRmContext

## STRESZCZENIe
Ustawia dzierżawę, abonament i środowisko dla poleceń cmdlet, które mają być używane w bieżącej sesji.

## POLECENIA

### Abonamentname (domyślnie)
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Świetle
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Subskrypcji
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Set-AzureRmContext ustawia informacje uwierzytelniające dotyczące apletów poleceń uruchomionych w bieżącej sesji.
Kontekst obejmuje informacje dotyczące dzierżawy, abonamentu i środowiska.

## Przykłady

### Przykład 1. Ustawianie kontekstu subskrypcji
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

To polecenie umożliwia ustawienie kontekstu do korzystania z określonej subskrypcji.

## PARAMETRÓW

### -Context
Określa kontekst bieżącej sesji.

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Subskrypcji
Określa identyfikator subskrypcji dla kontekstu, który jest ustawiany przez to polecenie cmdlet dla bieżącej sesji.

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Określa nazwę subskrypcji dla kontekstu, który jest ustawiany przez to polecenie cmdlet dla bieżącej sesji.

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Dzierżawy
Określa identyfikator dzierżawy dla kontekstu, który jest ustawiany przez to polecenie cmdlet dla bieżącej sesji.

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### PSAzureContext

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRMContext]()

