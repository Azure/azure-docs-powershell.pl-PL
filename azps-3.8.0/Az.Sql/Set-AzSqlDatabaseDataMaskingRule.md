---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 10afb514284fb3083110c068b33ffd189afd4039
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895793"
---
# Set-AzSqlDatabaseDataMaskingRule

## STRESZCZENIe
Ustawia właściwości reguły maskowania danych dla bazy danych.

## POLECENIA

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzSqlDatabaseDataMaskingRule** ustawia regułę maskowania danych dla bazy danych SQL Azure.
Aby użyć polecenia cmdlet, podaj parametry *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły.
Aby przekierować regułę, możesz podać dowolne parametry *SchemaName* , *TableName* i *ColumnName (ColumnName* ).
Określ parametr *MaskingFunction* , aby zmodyfikować sposób maskowania danych.
Jeśli określisz wartość liczbową lub tekst dla *MaskingFunction* , możesz określić parametry *numer* i *NumberTo* na potrzeby maskowania numerów lub parametry *PrefixSize* , *ReplacementString* i *SuffixSize* w celu maskowania tekstu.
Jeśli wykonanie polecenia powiedzie się, a jeśli określisz parametr *PassThru* , polecenie cmdlet zwróci obiekt opisujący właściwości reguły maskowania danych i identyfikatory reguł.
Identyfikatory reguł obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** , **DatabaseName** i **RuleID**.
To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.

## Przykłady

### Przykład 1: Zmienianie zakresu reguły maskowania danych w bazie danych
```
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

To polecenie modyfikuje regułę maskowania danych o IDENTYFIKATORze Rule17.
Ta reguła działa w bazie danych o nazwie Database01 na serwerze Server01.
To polecenie zmienia granice interwału, w którym jest generowana liczba losowa jako wartość maskowania.
Nowy zakres to od 23 do 42.

## PARAMETRÓW

### -ColumnName
Określa nazwę kolumny docelowej reguły maskowania.

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

### -MaskingFunction
Określa funkcja maskowania używaną przez regułę.
Dopuszczalne wartości tego parametru to:
- Domyślne
- Nomaskowanie
- SMS
- Ilości
- SocialSecurityNumber
- CreditCardNumber
- Wiadomość e-mail domyślna wartość jest domyślna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Numer
Określa dolną liczbę powiązaną interwału, od którego jest wybierana wartość losowa.
Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .
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
Określa górną granicę interwału, od którego jest wybierana wartość losowa.
Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .
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
Określa liczbę znaków na początku tekstu, który nie jest maskowany.
Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .
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

### -ReplacementString
Określa liczbę znaków na końcu tekstu, który nie jest maskowany.
Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .
Wartość domyślna to 0.

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

### -Nazwa_serwera
Określa nazwę serwera, na którym jest przechowywana baza danych.

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

### -SuffixSize
Określa liczbę znaków na końcu tekstu, który nie jest maskowany.
Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .
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
Określa nazwę tabeli bazy danych, która zawiera kolumnę zamaskowane.

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

### System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Nullable "1 [[System. Double, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## WYSYŁA

### Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingRuleModel

## INFORMACYJN

## LINKI POKREWNE

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[Nowe — AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)


