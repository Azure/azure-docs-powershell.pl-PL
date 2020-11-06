---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 85dc7d386dc64f8c384f9aae7925379375b95a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542820"
---
# Set-AzureRmSqlDatabaseSecondary

## STRESZCZENIe
Przełącza pomocniczą bazę danych na podstawową w celu zainicjowania trybu failover.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### NoOptionsSet (domyślny)
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFailoverParams
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmSqlDatabaseSecondary** przełącza pomocniczą bazę danych w celu zainicjowania trybu failover.
To polecenie cmdlet jest przeznaczone do obsługi poleceń konfiguracji ogólnej, ale jest obecnie ograniczone do inicjowania pracy awaryjnej.
Określ parametr *AllowDataLoss* , aby zainicjować wymuszoną pracę awaryjną podczas awarii.
Nie trzeba określać tego parametru podczas wykonywania planowanej operacji, na przykład funkcji drążenia do odzyskiwania.
W tym ostatnim przypadku pomocnicza baza danych jest synchronizowana z podstawowym, zanim zostanie przełączona.

## Przykłady

## PARAMETRÓW

### -AllowDataLoss
Wskazuje, że ta operacja trybu failover umożliwia utratę danych.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Określa nazwę pomocniczej bazy danych SQL Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Praca awaryjna
Wskazuje, że ta operacja jest przejściem do trybu failover.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL partnera.

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

### -ResourceGroupName
Określa nazwę grupy zasobów, do której przypisano pomocnicza baza danych SQL Azure.

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
Określa nazwę serwera SQL obsługującego pomocniczą bazę danych SQL Azure.

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

###  
Możesz popotokować wystąpienia obiektu **bazy danych** dla pomocniczej bazy danych w celu przeprowadzenia awaryjnego przepełnienia i utworzyć podstawową bazę danych tego polecenia cmdlet.

## WYSYŁA

###  
To polecenie cmdlet zwraca **ReplicationLink**.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmSqlDatabaseSecondary](./New-AzureRmSqlDatabaseSecondary.md)

[Remove-AzureRmSqlDatabaseSecondary](./Remove-AzureRmSqlDatabaseSecondary.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
