---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489358"
---
# Get-AzSqlDatabaseUpgradeHint

## STRESZCZENIe
Pobiera wskazówki dotyczące warstwy cenowej dla bazy danych.

## POLECENIA

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzSqlDatabaseUpgradeHint** pobiera wskazówki dotyczące warstwy cenowej umożliwiające uaktualnienie bazy danych SQL Azure.
Bazy danych, które nadal znajdują się w warstwach cenowych w sieci Web i w firmie, uzyskują wskazówkę umożliwiającą uaktualnienie nowych warstw cenowych podstawowych, standardowych i Premium.
To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.

## Przykłady

### Przykład 1: uzyskiwanie rekomendacji dla wszystkich baz danych na serwerze
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych na serwerze o nazwie Server01.

### Przykład 2: uzyskiwanie rekomendacji dla konkretnej bazy danych
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

To polecenie zwraca wskazówki dotyczące uaktualniania dla konkretnej bazy danych.

### Przykład 3: uzyskiwanie rekomendacji dla wszystkich baz danych, które nie należą do puli Elastic Database
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych, które nie należą do puli Elastic Database.

### Przykład 4: uzyskiwanie rekomendacji dla wszystkich baz danych na serwerze przy użyciu filtrowania
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych na serwerze o nazwie Server01, których nazwy rozpoczynają się od "bazy danych".

## PARAMETRÓW

### -DatabaseName
Określa nazwę bazy danych SQL, dla której to polecenie cmdlet pobiera wskazówkę o uaktualnieniu.
Jeśli baza danych nie zostanie określona, to polecenie cmdlet będzie pobierać wskazówki dotyczące wszystkich baz danych na serwerze logicznym.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -ExcludeElasticPoolCandidates
Wskazuje, czy bazy danych w pulach Elastic Database są wykluczone z zwróconych rekomendacji.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisana baza danych.

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
Określa nazwę serwera obsługującego bazę danych, dla której ten aplet polecenia uzyskuje wskazówkę o uaktualnieniu.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Boolean

## WYSYŁA

### Microsoft. Azure. Management. SQL. LegacySdk. MODELES. RecommendedDatabaseProperties

## INFORMACYJN

## LINKI POKREWNE

[Get-AzSqlDatabaseExpanded](./Get-AzSqlDatabaseExpanded.md)

[Get-AzSqlElasticPoolRecommendation](./Get-AzSqlElasticPoolRecommendation.md)


