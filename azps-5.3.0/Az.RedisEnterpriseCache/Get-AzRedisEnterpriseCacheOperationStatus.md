---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378240"
---
# Get-AzRedisEnterpriseCacheOperationStatus

## STRESZCZENIe
Pobiera stan operacji.

## POLECENIA

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Opis
Pobiera stan operacji.

## Przykłady

### Przykład 1: pobieranie stanu operacji
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

To polecenie uzyskuje stan operacji.

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

### — Lokalizacja
Region, w którym znajduje się operacja.

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

### -OperationId
Unikatowy identyfikator operacji.

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
Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. IOperationStatus

## INFORMACYJN

PISUJE

## LINKI POKREWNE

