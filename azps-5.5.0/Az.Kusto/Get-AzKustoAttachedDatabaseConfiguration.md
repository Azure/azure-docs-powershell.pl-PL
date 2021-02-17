---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b1a042eb96c1fa6acbcc22fbdd33aefd9d4d46b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185291"
---
# Get-AzKustoAttachedDatabaseConfiguration

## SYNOPSIS
Zwraca załączoną konfigurację bazy danych.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## OPIS
Zwraca załączoną konfigurację bazy danych.

## PRZYKŁADY

### Przykład 1. Lista wszystkich pól AttachedDatabaseConfigurations w klastrze
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

Powyższe polecenie zawiera listę wszystkich konfiguracji AttachedDatabaseConfigurations w klastrze "testnewkustoclusterf".

### Przykład 2. Uzyskiwanie konkretnej konfiguracji AttachedDatabaseConfiguration w klastrze
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

Powyższe polecenie zwraca wartość danych AttachedDatabaseConfigurations o nazwie "myfollowerconfiguration" w klastrze "testnewkustoclusterf".

## PARAMETERS

### -ClusterName
Nazwa klastru Kusto.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa dołączonej konfiguracji bazy danych.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów zawierającej klaster Kusto.

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
Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.

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

### Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IKustoIdentity> Parametr tożsamości
  - `[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.
  - `[ClusterName <String>]`: nazwa klastra Kusto.
  - `[DataConnectionName <String>]`: nazwa połączenia danych.
  - `[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[Location <String>]`: lokalizacja na platformie Azure.
  - `[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.
  - `[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.

## LINKI POKREWNE

