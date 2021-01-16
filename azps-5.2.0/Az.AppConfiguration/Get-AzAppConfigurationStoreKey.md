---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322560"
---
# Get-AzAppConfigurationStoreKey

## STRESZCZENIe
Wyświetla klucz dostępu do określonego magazynu konfiguracji.

## POLECENIA

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Wyświetla klucz dostępu do określonego magazynu konfiguracji.

## Przykłady

### Przykład 1: wyświetlanie wszystkich kluczy sklepu w magazynie konfiguracji aplikacji
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

To polecenie zawiera listę wszystkich kluczy sklepu w magazynie konfiguracji aplikacji.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa magazynu konfiguracji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, do której należy rejestr kontenera.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subskrypcji
Identyfikator subskrypcji platformy Microsoft Azure.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IApiKey

## INFORMACYJN

PISUJE

## LINKI POKREWNE

