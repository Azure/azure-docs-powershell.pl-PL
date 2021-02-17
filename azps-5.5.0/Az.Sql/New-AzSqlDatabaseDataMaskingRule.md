---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178426"
---
# New-AzSqlDatabaseDataMaskingRule

## SYNOPSIS
Tworzy regułę maskowania danych dla bazy danych.

## SKŁADNIA

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzSqlDatabaseDataMaskingRule** tworzy regułę maskowania danych dla bazy danych Azure SQL.
Aby użyć polecenia cmdlet, zidentyfikuj regułę za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName.*
Podaj wartości *TableName (Nazwa_tabeli)* i *ColumnName* (Nazwa Kolumny), aby określić obiekt docelowy reguły, oraz parametr *MaskingFunction* w celu zdefiniowania sposobu maskowania danych.
Jeśli *funkcja MaskingFunction* ma wartość Number (Liczba) lub Text (Tekst), można określić parametry *NumberFrom* i *NumberTo* (maskowanie liczb) lub (w przypadku maskowania liczb) lub *PrefixSize*(Rozmiar *Prefiksu), ReplacementString*(Sufiks) i *SufiksSize* (RozmiarSufiku) dla maskowania tekstu.
Jeśli polecenie się powiedzie i zostanie użyty parametr *PassThru,* polecenie cmdlet oprócz identyfikatorów reguł zwróci obiekt opisujący właściwości reguły maskowania danych.
Do identyfikatorów reguł należą między innymi nazwa *ResourceGroupName,* *nazwa_serwera,* nazwa_bazy danych i *identyfikator reguły.* 
To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.

## PRZYKŁADY

### Przykład 1. Tworzenie reguły maskowania danych dla kolumny liczb w bazie danych
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

To polecenie tworzy regułę maskowania danych dla kolumny o nazwie Kolumna01 w tabeli o nazwie Tabela01 w schemacie o nazwie Schema01.
Baza danych o nazwie Database01 zawiera wszystkie te elementy.
Reguła jest regułą maskowania liczb, która używa liczby losowej zamiejscowej od 5 do 14.

## PARAMETERS

### -ColumnName
Określa nazwę kolumny docelowej przez regułę maskowania.

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

### -DatabaseName
Określa nazwę bazy danych.

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

### -MaskingFunction
Określa funkcję maskowania używaną przez regułę.
Dopuszczalne wartości dla tego parametru to:
- Domyślne
- NoMasking
- Tekst
- Numer
- SocialSecurityNumber
- CreditCardNumber
- Wiadomość e-mail Wartość domyślna to Domyślna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
Określa dolną liczbę powiązaną interwału, z którego jest wybierana losowa wartość.
Określ ten parametr tylko w przypadku określenia wartości Number dla *parametru MaskingFunction.*
Wartość domyślna to 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
Określa górną liczbę powiązaną interwału, z którego jest wybierana losowa wartość.
Określ ten parametr tylko w przypadku określenia wartości Number dla *parametru MaskingFunction.*
Wartość domyślna to 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

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

### -PrefixSize
Określa liczbę znaków na początku tekstu, które nie są maskowane.
Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.
Wartość domyślna to 0.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - ReplacementString
Określa liczbę znaków na końcu tekstu, które nie są maskowane.
Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.
Wartość domyślna jest ciągiem pustym.

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

### -SchemaName
Określa nazwę schematu.

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

### -ServerName
Określa nazwę serwera hostowego bazę danych.

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

### -SufiksSize
Określa liczbę znaków na końcu tekstu, które nie są maskowane.
Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.
Wartość domyślna to 0.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableName
Określa nazwę tabeli bazy danych zawierającej zamaskowana kolumnę.

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

### System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUTS

### Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel

## NOTATKI

## LINKI POKREWNE

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Set-AzSqlDatabaseDataMaskingRule](./Set-AzSqlDatabaseDataMaskingRule.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)


