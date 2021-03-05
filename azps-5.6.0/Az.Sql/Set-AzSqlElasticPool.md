---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 564bd475b8574f30f8d00cc1a374bc11b4a93ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963601"
---
# Set-AzSqlElasticPool

## SYNOPSIS
Modyfikuje właściwości elastycznej puli baz danych w usłudze Azure SQL Database.

## SKŁADNIA

### DtuBasedPool (domyślne)
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### VcoreBasedPool
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzSqlElasticPool** ustawia właściwości elastycznej puli w usłudze Azure SQL Database. To polecenie cmdlet może modyfikować wartości eDTU na pulę *(Dtu),* maksymalny rozmiar przestrzeni dyskowej na pulę *(StorageMB),* maksymalna liczba jednostek eDTU na bazę danych *(DatabaseDtuMax)* oraz minimalne liczby eDTU na bazę danych *(DatabaseDtuMin).*
Kilka parametrów *(-Dtu, -DatabaseDtuMin i -DatabaseDtuMax)* wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru. Na przykład wartość -DatabaseDtuMax dla puli eDTU Standard 100 można ustawić tylko na wartość 10, 20, 50 lub 100.  Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

## PRZYKŁADY

### Przykład 1. Modyfikowanie właściwości puli elastycznej
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

To polecenie modyfikuje właściwości puli elastycznej o nazwiePoolpool01. Polecenie ustawia liczbę jednostek DTU dla puli elastycznej na 1000 oraz ustawia minimalną i maksymalną liczbę jednostek DTU.

### Przykład 2. Modyfikowanie maksymalnego rozmiaru miejsca do magazynowania elastycznej puli
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

To polecenie modyfikuje właściwości puli elastycznej o nazwiePoolpool01. To polecenie ustawia maksymalną ilość miejsca do magazynowania elastycznego puli na 2 TB.

### Przykład 3

Modyfikuje właściwości elastycznej puli baz danych w usłudze Azure SQL Database. (wygenerowane automatycznie)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

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

### -Compute Zwyrodnienie
Generowanie obliczeniowe do przypisania.

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMax
Określa maksymalną liczbę jednostek DTU, z których może korzystać każda pojedyncza baza danych w puli.
Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Wartości domyślne dla różnych wersji są następujące:
- Podstawowe.  5 DTU
- Standardowe. 100 DTU
- Premium. 125 DTU

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMin
Określa minimalną liczbę jednostek DTU, które elastyczna pula gwarantuje wszystkim bazom danych w puli.
Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Wartość domyślna to zero (0).

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMax
Maksymalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMin
Minimalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### - Dtu
Określa całkowitą liczbę współużytkonych jednostek DTU dla puli elastycznej.
Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Wartości domyślne dla różnych wersji są następujące:
- Podstawowe. 100 DTU
- Standardowe. 100 DTU
- Premium. 125 DTU

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — wersja
Określa wersję bazy danych Azure SQL Database dla puli elastycznej. Nie można zmienić wersji. Dopuszczalne wartości dla tego parametru to:
- Brak
- Podstawowe
- Standardowe
- Premium
- DataWarehouse
- Bezpłatne
- Rozciągnięcie
- GeneralPurpose
- BusinessCritical

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nawiązywane_buforyNazwa
Określa nazwę puli elastycznej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseType
Typ licencji dla bazy danych Azure Sql Database.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - MaintenanceConfigurationId
Identyfikator konfiguracji konserwacji puli elastycznej SQL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisana pula elastyczna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Określa nazwę serwera hostowego elastyczną pulę.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — StorageMB
Określa limit magazynowania puli elastycznej (w megabajtach). Aby uzyskać więcej informacji, zobacz New-AzSqlElasticPool cmdlet.

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

### — Tagi
Określa słownik par klucz-wartość, który to polecenie cmdlet skojarzy z elastyczną pulą w postaci tabeli skrótów. Na przykład: `@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — VCore
Całkowita udostępniona liczba procesorów Vcore dla puli sql Azure 2010 r.

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
Nadmiarowość stref, która ma być skojarzana z pulą Azure Sql 2010

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Sql.NawiązywekPoola.Model.AzureSqlElasticPoolModel

## NOTATKI

## LINKI POKREWNE

[Get-AzSqlElasticPool](./Get-AzSqlElasticPool.md)

[Get-AzSqlElasticPoolActivity](./Get-AzSqlElasticPoolActivity.md)

[Get-AzSqlElasticPoolDatabase](./Get-AzSqlElasticPoolDatabase.md)

[New-AzSqlElasticPool](./New-AzSqlElasticPool.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
