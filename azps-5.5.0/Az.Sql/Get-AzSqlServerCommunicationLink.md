---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176906"
---
# Get-AzSqlServerCommunicationLink

## SYNOPSIS
Pobiera linki komunikacyjne do elastycznych transakcji bazy danych między serwerami baz danych.

## SKŁADNIA

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzSqlServerCommunicationLink** pobiera linki komunikacji między serwerami w celu elastycznej transakcji bazy danych w usłudze Azure SQL Database.
Określ nazwę linku do komunikacji serwera, aby wyświetlić właściwości tego linku.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich łączy komunikacyjnych dla serwera
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

To polecenie pobiera wszystkie linki komunikacyjne między serwerami dla elastycznych transakcji bazy danych dla serwera o nazwie ContosoServer17.

### Przykład 2. Uzyskiwanie określonego linku do komunikacji dla serwera
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

To polecenie pobiera link do komunikacji między serwerami o nazwie Link01.

### Przykład 3. Uzyskiwanie wszystkich łączy komunikacyjnych dla serwera przy użyciu filtrowania
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

To polecenie pobiera wszystkie linki komunikacyjne między serwerami dla elastycznych transakcji bazy danych dla serwera o nazwie ContosoServer17, których nazwy zaczynają się od "Link".

## PARAMETERS

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

### -LinkName
Określa nazwę łącza do komunikacji serwera, do których otrzymuje to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *ServerName.*

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
Określa nazwę serwera.
Ten serwer zawiera link do komunikacji, który otrzymuje to polecenie cmdlet.

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

## OUTPUTS

### Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql

## LINKI POKREWNE

[New-AzSqlServerCommunicationLink](./New-AzSqlServerCommunicationLink.md)

[Remove-AzSqlServerCommunicationLink](./Remove-AzSqlServerCommunicationLink.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
