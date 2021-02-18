---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: d8dc345ae9f307bbd5f1cd003edf1cba4a7ea6b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193162"
---
# Get-AzPostgreSqlFlexibleServer

## SYNOPSIS
Pobiera informacje o serwerze.

## SKŁADNIA

### Lista1 (domyślna)
```
Get-AzPostgreSqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Lista
```
Get-AzPostgreSqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## OPIS
Pobiera informacje o serwerze.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie serwera PostgreSql z kontekstem domyślnym
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

To polecenie cmdlet pobiera serwery PostgreSql z kontekstem domyślnym.

### Przykład 2. Uzyskiwanie serwera PostgreSql według nazwy grupy zasobów i serwera
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

To polecenie cmdlet pobiera serwery PostgreSql według nazw serwerów i grup zasobów.

### Przykład 3. Lista wszystkich serwerów PostgreSql w określonej grupie zasobów
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----             -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test  eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
postgresql-test2 eastus   postgresql-test     12     32768                   Standard_42s_v3 GeneralPurpose
```

To polecenie cmdlet wyświetla listę wszystkich serwerów PostgreSql w określonej grupie zasobów.

### Przykład 4. Uzyskiwanie serwera PostgreSql według tożsamości
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Get-AzPostgreSqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test         12     32768                    Standard_D2s_v3 GeneralPurpose
```

Te listy polecenia cmdlet pobierają serwery PostgreSql według tożsamości.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa serwera.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

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

### - SubscriptionId
Identyfikator subskrypcji docelowej.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
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

### Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości
  - `[ConfigurationName <String>]`: nazwa konfiguracji serwera.
  - `[DatabaseName <String>]`: nazwa bazy danych.
  - `[FirewallRuleName <String>]`: nazwa reguły zapory serwera.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[LocationName <String>]`: nazwa lokalizacji.
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów. W nazwie nie jest uwzględniania liter.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.
  - `[ServerName <String>]`: nazwa serwera.
  - `[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.
  - `[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.

## LINKI POKREWNE

