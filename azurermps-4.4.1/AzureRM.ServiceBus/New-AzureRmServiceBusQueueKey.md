---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719242"
---
# New-AzureRmServiceBusQueueKey

## STRESZCZENIe
Generuje podstawowe lub pomocnicze ciągi połączeń dla kolejki usługi Service Bus.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmServiceBusQueueKey** generuje ponownie podstawowy lub pomocniczy ciąg połączenia dla określonej kolejki usługi Service Bus i reguły autoryzacji.

## Przykłady

### Przykład 1
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

Generuje ponownie główne parametry połączenia dla obszaru nazw.

### Przykład 2
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

Generuje ponownie parametry połączenia pomocniczego dla obszaru nazw.

## PARAMETRÓW

### -AuthorizationRuleName
Nazwa reguły autoryzacji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
Nazwa obszaru nazw usługi Service Bus.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -QueueName
Nazwa kolejki usługi Service Bus.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegenerateKeys
Określa, czy ponownie wygenerować klucze podstawowe i pomocnicze.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### -ResourceName
 System. String
 

### -NamespaceName
 System. String
 

### -AuthorizationRuleName
 System. String
 

### -QueueName
 System. String
 

### -RegenerateKeys
 System. String

## WYSYŁA

### Microsoft. Azure. Management. ServiceBus. MODELES. ResourceListKeys
PrimaryConnectionString: punkt końcowy = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {wartość PrimaryKey} SecondaryKey: {SecondaryKey wartość} NazwaKlucza: SBAuthoRule1

## INFORMACYJN

## LINKI POKREWNE

