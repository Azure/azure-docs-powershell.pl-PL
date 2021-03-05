---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: c6c298b9ec4a233c5db784e5e661af86bca2cb8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014762"
---
# Get-AzSqlDatabaseReplicationLink

## SYNOPSIS
Pobiera linki replikacji geograficznej między usługą Azure SQL Database a grupą zasobów lub programem SQL Server.

## SKŁADNIA

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzSqlDatabaseReplicationLink** zastępuje polecenie cmdlet **Get-AzSqlDatabaseCopy.**
Pobiera ona wszystkie linki replikacji geograficznej między określoną bazą danych Azure SQL Database a grupą zasobów lub programem AzureSQL Server.

## PRZYKŁADY

### Przykład 1

Pobiera linki replikacji geograficznej między usługą Azure SQL Database a grupą zasobów lub programem SQL Server. (wygenerowane automatycznie)

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlDatabaseReplicationLink -DatabaseName db1 -PartnerResourceGroupName rg2 -ResourceGroupName MyResourceGroup -ServerName s1
```

## PARAMETERS

### -DatabaseName
Określa nazwę bazy danych SQL, dla której mają być pobierane linki.

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

### -PartnerResourceGroupName
Określa nazwę grupy zasobów, do której jest przydzielony partner.

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

### -PartnerServerName
Określa nazwę serwera Azure SQL Server partnera.

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
Określa nazwę grupy zasobów platformy Azure dla bazy danych, dla której mają być pobierane linki.

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
Określa nazwę serwera SQL dla bazy danych, dla których mają być pobierane linki.

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
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

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
