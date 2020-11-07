---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719610"
---
# New-AzureRmSqlElasticPool

## STRESZCZENIe
Tworzy pulę Elastic Database dla bazy danych SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmSqlElasticPool** tworzy pulę Elastic Database dla bazy danych SQL Azure.

Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru. Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.  Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

## Przykłady

### Przykład 1. Tworzenie puli elastycznej
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

To polecenie tworzy elastyczną pulę w standardowej warstwie usługi o nazwie ElasticPool01. Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna. Polecenie określa wartości właściwości jednostek DTU dla puli i baz danych w puli.

## PARAMETRÓW

### -DatabaseDtuMax
Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), które mogą być używane przez dowolną pojedynczą bazę danych w puli.
Domyślne wartości różnych wersji są następujące:

- Podstawowym. 5 DTU
- Standard. 100 DTU
- Ubezpieczeni. 125 DTU

Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli rozmiarów w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) 


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

### -DatabaseDtuMin
Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.
Wartość domyślna to zero (0).

Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

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

### -DTU
Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.
Domyślne wartości różnych wersji są następujące:

- Podstawowym.
100 DTU
- Standard.
100 DTU
- Ubezpieczeni.
125 DTU

Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

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

### -Edition
Określa wersję bazy danych SQL Azure używanej dla puli elastycznej.
Dopuszczalne wartości tego parametru to:

- Ubezpieczeni
- Podstawowym
- Standard
- DataWarehouse
- Rozciąga
- Niezależnych
- Składki

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolName
Określa nazwę puli elastycznej, którą tworzy polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje pulę elastyczną.

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

### -Nazwa_serwera
Określa nazwę serwera obsługującego pulę elastyczną.

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

### -StorageMB
Określa limit magazynowania (w megabajtach) dla puli elastycznej. Jeśli nie podano tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości parametru *jednostek DTU* .

Zobacz [limity liczby jednostek eDTU i przestrzeni dyskowej,](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) Aby uzyskać dopuszczalne wartości.

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

### -Tagi
Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z pulą elastyczną. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmSqlElasticPool](./Get-AzureRmSqlElasticPool.md)

[Get-AzureRmSqlElasticPoolActivity](./Get-AzureRmSqlElasticPoolActivity.md)

[Get-AzureRmSqlElasticPoolDatabase](./Get-AzureRmSqlElasticPoolDatabase.md)

[Remove-AzureRmSqlElasticPool](./Remove-AzureRmSqlElasticPool.md)

[Set-AzureRmSqlElasticPool](./Set-AzureRmSqlElasticPool.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
