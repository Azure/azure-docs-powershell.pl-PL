---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: eef0b5d4b74f6390044453ec318b5f3de6846814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542188"
---
# Resume-AzureRmSqlDatabase

## STRESZCZENIe
Wznawia bazę danych hurtowni danych SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Resume-AzureRmSqlDatabase** wznawia bazę danych hurtowni danych SQL Azure.

## Przykłady

### Przykład 1: wznawia bazę danych hurtowni danych SQL Azure
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

To polecenie wznawia wstrzymaną bazę danych hurtowni danych SQL Azure.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Określa nazwę bazy danych, która zostanie wznowiona przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisana baza danych.

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
Określa nazwę serwera obsługującego bazę danych, która zostanie wznowiona przez to polecenie cmdlet.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel

## WYSYŁA

### Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel

## INFORMACYJN
* Polecenie cmdlet **Resume-AzureRmSqlDatabase** działa tylko w przypadku baz danych hurtowni danych usługi Azure SQL. Ta operacja nie jest obsługiwana w przypadku usługi Azure SQL Database Basic, wersji Standard i Premium.

## LINKI POKREWNE

[Get-AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[Nowe — AzureRmSqlDatabase](./New-AzureRmSqlDatabase.md)

[Remove-AzureRmSqlDatabase](./Remove-AzureRmSqlDatabase.md)

[Set-AzureRmSqlDatabase](./Set-AzureRmSqlDatabase.md)

[Suspend — AzureRmSqlDatabase](./Suspend-AzureRmSqlDatabase.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)


