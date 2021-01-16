---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352489"
---
# Set-AzRedisCache

## STRESZCZENIe
Modyfikuje pamięć podręczną Redis.

## POLECENIA

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzRedisCache** modyfikuje pamięć podręczną platformy Azure Redis.

## Przykłady

### Przykład 1: modyfikowanie pamięci podręcznej Redis
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

To polecenie aktualizuje zasady maxmemory dla pamięci podręcznej Redis o nazwie moja pamięć.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNonSslPort
Wskazuje, czy port inny niż SSL jest włączony.
Wartość domyślna to $False (port inny niż SSL jest wyłączony).

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
Określ wersję TLS wymaganą przez klientów do łączenia się z pamięcią podręczną.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę pamięci podręcznej Redis do zaktualizowania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisConfiguration
Określa ustawienia konfiguracji Redis.
Dopuszczalne wartości tego parametru to:
- RDB — włączono funkcję kopii zapasowej.
Określa, że Redis danych jest włączona.
Tylko poziom Premium.
- RDB-połączenie typu "pamięć podłączana".
Określa parametry połączenia z kontem magazynu dla Redis danych.
Tylko poziom Premium.
- RDB — częstotliwość wykonywania kopii zapasowych.
Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.
Tylko poziom Premium. 
- maxmemory-zarezerwowane.
Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.
Warstwy standardowe i Premium. 
- maxmemory — zasady.
Konfiguruje zasady wykluczania dla pamięci podręcznej.
Wszystkie warstwy cenowe. 
- Powiadamianie — zdarzenia dotyczące miejsca na znakach.
Konfiguruje powiadomienia dotyczące miejsca na dysku.
Warstwy standardowe i Premium. 
- Hash-Max-ZipList-zapisy.
Konfiguruje optymalizację pamięci dla małych typów danych agregacji.
Warstwy standardowe i Premium. 
- Hash — Max-ZipList-Value.
Konfiguruje optymalizację pamięci dla małych typów danych agregacji.
Warstwy standardowe i Premium. 
- set-max-intset-zapisy.
Konfiguruje optymalizację pamięci dla małych typów danych agregacji.
Warstwy standardowe i Premium. 
- zset-Max-ZipList-zapisy.
Konfiguruje optymalizację pamięci dla małych typów danych agregacji.
Warstwy standardowe i Premium. 
- zset-Max-ZipList-Value.
Konfiguruje optymalizację pamięci dla małych typów danych agregacji.
Warstwy standardowe i Premium. 
- baz danych.
Konfiguruje liczbę baz danych.
Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.
Warstwy standardowe i Premium.
Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShardCount
Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
Określa rozmiar pamięci podręcznej Redis.
Prawidłowe wartości: 
- Punkt
- Punktu
- Przeznaczone
- P4
- P5
- C0
- C1
- C2
- C3
- C4
- C5
- C6
- 250MB
- 1 GB
- 2,5 GB
- 6GB
- 13GB
- 26GB
- 53GB
- 120 GB wartość domyślna to 1 GB lub C1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.
Prawidłowe wartości: 
- Podstawowym
- Standard
- Premium wartość domyślna to standard.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Tabela skrótów przedstawiająca znaczniki.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
Ten parametr jest przestarzały.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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

### System. String

### System. Collections. Hashtable

### System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## WYSYŁA

### Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys

## INFORMACYJN

## LINKI POKREWNE

[Get-AzRedisCache](./Get-AzRedisCache.md)

[Nowe — AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)


