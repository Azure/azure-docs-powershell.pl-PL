---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378156"
---
# Update-AzRedisEnterpriseCacheDatabase

## STRESZCZENIe
Aktualizowanie bazy danych

## POLECENIA

### UpdateExpanded (domyślny)
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Opis
Aktualizowanie bazy danych

## Przykłady

### Przykład 1: protokół Client Update
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

To polecenie aktualizuje protokół klienta bazy danych dla pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć.

### Przykład 2: aktualizowanie protokołu klienta i zasad wykluczania
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

To polecenie aktualizuje zasady protokołu klienta i wykluczania bazy danych dla pamięci podręcznej Redis Enterprise.

## PARAMETRÓW

### -AsJob
Uruchamianie polecenia jako zadania

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientProtocol
Określa, czy klienci Redis mogą łączyć się przy użyciu protokołów szyfrowania TLS lub Redis.
Wartość domyślna to TLS-Encrypted.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusteringPolicy
Zasady klastrowania — domyślnie OSSCluster.
Określone w czasie tworzenia.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwaklastraname
Nazwa klastra usługi RedisEnterprise.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EvictionPolicy
Zasady wykluczania Redis-domyślnie VolatileLRU

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Module
Opcjonalny zestaw modułów Redis do włączenia w tej bazie danych może być dodawany tylko w czasie tworzenia.
Aby skonstruować, zobacz sekcję notatki dla właściwości modułu i Utwórz tablicę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Wykonywanie polecenia asynchronicznie

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
Port TCP punktu końcowego bazy danych.
Określone w czasie tworzenia.
Domyślnie jest to dostępny port.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
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
Type: System.String
Parameter Sets: UpdateExpanded
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

### Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. IRedisEnterpriseCacheIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. IDatabase

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IRedisEnterpriseCacheIdentity> : parametr Identity
  - `[ClusterName <String>]`: Nazwa klastra usługi RedisEnterprise.
  - `[DatabaseName <String>]`: Nazwa bazy danych.
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[Location <String>]`: Region, w którym znajduje się operacja.
  - `[OperationId <String>]`: Unikatowy identyfikator operacji.
  - `[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego skojarzonego z zasobem platformy Azure
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów.
  - `[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

Moduł <IModule [] >: opcjonalny zestaw modułów Redis do włączenia w tej bazie danych może być dodawany tylko w czasie tworzenia.
  - `Name <String>`: Nazwa modułu, na przykład "RedisBloom", "RediSearch", "RedisTimeSeries"
  - `[Arg <String>]`: Opcje konfiguracji modułu, na przykład "ERROR_RATE 0,00 INITIAL_SIZE 400".

## LINKI POKREWNE

