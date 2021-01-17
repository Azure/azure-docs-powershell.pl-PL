---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378184"
---
# Remove-AzRedisEnterpriseCache

## STRESZCZENIe
Usuwa klaster pamięci podręcznej RedisEnterprise.

## POLECENIA

### Usuń (domyślnie)
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Usuwa klaster pamięci podręcznej RedisEnterprise.

## Przykłady

### Przykład 1: usunięcie Redis pamięci podręcznej przedsiębiorstwa i zwrócenie wyniku
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

To polecenie usuwa Redis pamięci podręcznej przedsiębiorstwa i wyświetla, czy operacja jest udana.

### Przykład 2: usunięcie Redis pamięci podręcznej przedsiębiorstwa i nie Wyświetlanie wyniku
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

To polecenie usuwa pamięć podręczną przedsiębiorstwa Redis.
Ponieważ parametr PassThru nie jest określony, wynik operacji nie jest wyświetlany.

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

### -Nazwaklastraname
Nazwa klastra usługi RedisEnterprise.

```yaml
Type: System.String
Parameter Sets: Delete
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

### -Inputobject
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -PassThru
Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.

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

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: Delete
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
Parameter Sets: Delete
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

### System. Boolean

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

## LINKI POKREWNE

