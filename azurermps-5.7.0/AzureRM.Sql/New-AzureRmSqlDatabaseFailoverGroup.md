---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524813"
---
# New-AzureRmSqlDatabaseFailoverGroup

## STRESZCZENIe
To polecenie powoduje utworzenie nowej grupy trybu failover bazy danych SQL Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Umożliwia utworzenie nowej grupy trybu failover bazy danych SQL Azure dla określonych serwerów.

Dwa punkty końcowe TDS bazy danych Azure SQL Database są tworzone w witrynie FailoverGroupName. SqlDatabaseDnsSuffix (na przykład FailoverGroupName.database.windows.net) i FailoverGroupName. pomocnicze SqlDatabaseDnsSuffix. Te punkty końcowe mogą być używane do łączenia się z serwerami podstawowymi i pomocniczymi w grupie trybu failover. Jeśli na serwerze podstawowym wpłynie awaria, automatyczna praca awaryjna punktów końcowych i baz danych zostanie wyzwolona jako podyktowana przez zasady pracy awaryjnej grupy trybu failover i okres prolongaty.

Nowo utworzone grupy pracy awaryjnej nie zawierają żadnych baz danych. Aby sterować zestawem baz danych w grupie trybu failover, Użyj poleceń cmdlet "Add-AzureRmSqlDatabaseToFailoverGroup" i "Remove-AzureRmSqlDatabaseFromFailoverGroup".

Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.

## Przykłady

### Przykład 1
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

To polecenie tworzy nową grupę pracy awaryjnej z zasadami pracy awaryjnej dla dwóch serwerów w tej samej grupie zasobów.

### Przykład 2
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

To polecenie tworzy nową grupę trybu failover z zasadami pracy awaryjnej dla dwóch serwerów w różnych grupach zasobów.

## PARAMETRÓW

### -AllowReadOnlyFailoverToPrimary
Czy awaria na serwerze pomocniczym powinna wyzwalać automatyczną pracę awaryjną punktu końcowego tylko do odczytu. Ta funkcja nie jest jeszcze obsługiwana.

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverGroupName
Nazwa grupy trybu failover bazy danych SQL Azure do utworzenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverPolicy
Zasady przełączania awaryjnego grupy usługi Azure SQL Database failover.

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### -GracePeriodWithDataLossHours
Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria i nie można ukończyć pracy awaryjnej bez utraty danych.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
Nazwa grupy pomocniczej zasobu w grupie praca awaryjna bazy danych SQL Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServerName
Nazwa serwera pomocniczego grupy trybu failover bazy danych SQL Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nazwa_serwera
Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. Object

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRmSqlDatabaseFailoverGroup](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[Get-AzureRmSqlDatabaseFailoverGroup](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[Dodaj-AzureRmSqlDatabaseToFailoverGroup](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[Remove-AzureRmSqlDatabaseFromFailoverGroup](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[Przełącznik-AzureRmSqlDatabaseFailoverGroup](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[Remove-AzureRmSqlDatabaseFailoverGroup](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
