---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 8dca573eb0d527beb08bb591b0c8fa3b2fc6e30a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011962"
---
# Get-AzMySqlFlexibleServerConfiguration

## SYNOPSIS
Pobiera informacje o konfiguracji serwera.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## OPIS
Pobiera informacje o konfiguracji serwera.

## PRZYKŁADY

### Przykład 1. Lista wszystkich konfiguracji na określonym serwerze MySql
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

To polecenie cmdlet wyświetla listę wszystkich konfiguracji na określonym serwerze MySql.

### Przykład 2. Uzyskiwanie określonej konfiguracji mysql według nazwy
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

To polecenie cmdlet określa konfigurację mysql według nazwy.

### Przykład 3. Konfiguracja listy według tożsamości
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

To polecenie cmdlet jest określane przez tożsamość w konfiguracji mysql.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa konfiguracji serwera.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.
W nazwie nie jest uwzględniania liter.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Nazwa serwera.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji docelowej.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości
  - `[ConfigurationName <String>]`: nazwa konfiguracji serwera.
  - `[DatabaseName <String>]`: nazwa bazy danych.
  - `[FirewallRuleName <String>]`: nazwa reguły zapory serwera.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[KeyName <String>]`: nazwa klucza serwera.
  - `[LocationName <String>]`: nazwa lokalizacji.
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów. W nazwie nie jest uwzględniania liter.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.
  - `[ServerName <String>]`: nazwa serwera.
  - `[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.
  - `[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.

## LINKI POKREWNE

