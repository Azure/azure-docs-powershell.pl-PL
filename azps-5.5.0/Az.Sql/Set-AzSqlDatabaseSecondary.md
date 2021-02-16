---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178355"
---
# Set-AzSqlDatabaseSecondary

## SYNOPSIS
Przełącza pomocniczą bazę danych jako podstawową w celu zainicjowania trybu failover.

## SKŁADNIA

### NoOptionsSet (Domyślne)
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFailoverParams
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzSqlDatabaseSecondary** przełącza pomocniczą bazę danych jako podstawową w celu zainicjowania trybu failover.
To polecenie cmdlet jest zaprojektowane jako ogólne polecenie konfiguracji, ale obecnie jest ograniczone do inicjowania trybu failover.
Określ parametr *AllowDataLoss,* aby zainicjować wymuszanie trybu failover podczas awarii.
Nie musisz określać tego parametru podczas wykonywania planowanej operacji, takiej jak przechodzenie do szczegółów odzyskiwania.
W drugim przypadku pomocnicza baza danych jest synchronizowana z podstawową bazą danych przed jej przełączeniem.

## PRZYKŁADY

### Przykład 1. Inicjowanie planowanej trybu failover
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### Przykład 2. Zainicjowanie wymuszonego trybu failover (z potencjalną utratą danych)
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## PARAMETERS

### -AllowDataLoss
Wskazuje, że ta operacja trybu failover zezwala na utratę danych.

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

### -DatabaseName
Określa nazwę pomocniczej bazy danych Azure SQL Database.

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

### - Failover
Oznacza, że ta operacja jest trybem failover.

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
Określa nazwę grupy zasobów, do której jest przypisana partnerska baza danych Azure SQL Database.

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
Określa nazwę grupy zasobów, do której jest przypisana usługa Azure SQL Database Secondary.

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
Określa nazwę serwera SQL hostowego pomocniczego bazy danych Azure SQL Database.

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

### Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel

## NOTATKI

## LINKI POKREWNE

[New-AzSqlDatabaseSecondary](./New-AzSqlDatabaseSecondary.md)

[Remove-AzSqlDatabaseSecondary](./Remove-AzSqlDatabaseSecondary.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
