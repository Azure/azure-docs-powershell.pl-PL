---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: eb5e809b3f48403a6095f84643af0a169b2cecf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707869"
---
# <span data-ttu-id="47e19-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="47e19-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="47e19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47e19-102">SYNOPSIS</span></span>
<span data-ttu-id="47e19-103">Tworzy regułę maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="47e19-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="47e19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47e19-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47e19-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47e19-105">DESCRIPTION</span></span>
<span data-ttu-id="47e19-106">Polecenie cmdlet **New-AzSqlDatabaseDataMaskingRule** tworzy regułę maskowania danych dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="47e19-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="47e19-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły.</span><span class="sxs-lookup"><span data-stu-id="47e19-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="47e19-108">Podaj wartości *tabelaname* i *ColumnName* , aby określić element docelowy reguły i parametr *MaskingFunction* , aby zdefiniować sposób maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="47e19-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="47e19-109">Jeśli *MaskingFunction* ma wartość liczby lub tekstu, możesz określić parametry *numer* i *NumberTo* , w przypadku maskowania numerów lub *PrefixSize* , *ReplacementString* i *SuffixSize* w celu maskowania tekstu.</span><span class="sxs-lookup"><span data-stu-id="47e19-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="47e19-110">Jeśli wykonanie polecenia powiedzie się i użyto parametru *PassThru* , polecenie cmdlet zwraca obiekt opisujący właściwości reguły maskowania danych oprócz identyfikatorów reguł.</span><span class="sxs-lookup"><span data-stu-id="47e19-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="47e19-111">Identyfikatory reguł obejmują, ale nie są ograniczone do, *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID*.</span><span class="sxs-lookup"><span data-stu-id="47e19-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="47e19-112">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="47e19-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="47e19-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47e19-113">EXAMPLES</span></span>

### <span data-ttu-id="47e19-114">Przykład 1. Tworzenie reguły maskowania danych dla kolumny liczb w bazie danych</span><span class="sxs-lookup"><span data-stu-id="47e19-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="47e19-115">To polecenie tworzy regułę maskowania danych dla kolumny o nazwie Column01 w tabeli o nazwie Table01 w schemacie o nazwie Schema01.</span><span class="sxs-lookup"><span data-stu-id="47e19-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="47e19-116">Baza danych o nazwie Database01 zawiera wszystkie te elementy.</span><span class="sxs-lookup"><span data-stu-id="47e19-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="47e19-117">Reguła jest regułą maskowania liczb, która używa liczby losowej z przedziału od 5 do 14 jako wartości maski.</span><span class="sxs-lookup"><span data-stu-id="47e19-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="47e19-118">Reguła nosi nazwę Rule01.</span><span class="sxs-lookup"><span data-stu-id="47e19-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="47e19-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47e19-119">PARAMETERS</span></span>

### <span data-ttu-id="47e19-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="47e19-120">-ColumnName</span></span>
<span data-ttu-id="47e19-121">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="47e19-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="47e19-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47e19-122">-DatabaseName</span></span>
<span data-ttu-id="47e19-123">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="47e19-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="47e19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e19-124">-DefaultProfile</span></span>
<span data-ttu-id="47e19-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="47e19-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47e19-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="47e19-126">-MaskingFunction</span></span>
<span data-ttu-id="47e19-127">Określa funkcja maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="47e19-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="47e19-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="47e19-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47e19-129">Domyślne</span><span class="sxs-lookup"><span data-stu-id="47e19-129">Default</span></span>
- <span data-ttu-id="47e19-130">Nomaskowanie</span><span class="sxs-lookup"><span data-stu-id="47e19-130">NoMasking</span></span>
- <span data-ttu-id="47e19-131">SMS</span><span class="sxs-lookup"><span data-stu-id="47e19-131">Text</span></span>
- <span data-ttu-id="47e19-132">Ilości</span><span class="sxs-lookup"><span data-stu-id="47e19-132">Number</span></span>
- <span data-ttu-id="47e19-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="47e19-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="47e19-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="47e19-134">CreditCardNumber</span></span>
- <span data-ttu-id="47e19-135">Wiadomość e-mail domyślna wartość jest domyślna.</span><span class="sxs-lookup"><span data-stu-id="47e19-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="47e19-136">-Numer</span><span class="sxs-lookup"><span data-stu-id="47e19-136">-NumberFrom</span></span>
<span data-ttu-id="47e19-137">Określa dolną liczbę powiązaną interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="47e19-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="47e19-138">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="47e19-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="47e19-139">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="47e19-139">The default value is 0.</span></span>

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

### <span data-ttu-id="47e19-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="47e19-140">-NumberTo</span></span>
<span data-ttu-id="47e19-141">Określa górną granicę interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="47e19-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="47e19-142">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="47e19-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="47e19-143">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="47e19-143">The default value is 0.</span></span>

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

### <span data-ttu-id="47e19-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47e19-144">-PassThru</span></span>
<span data-ttu-id="47e19-145">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="47e19-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="47e19-146">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="47e19-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="47e19-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="47e19-147">-PrefixSize</span></span>
<span data-ttu-id="47e19-148">Określa liczbę znaków na początku tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="47e19-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="47e19-149">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="47e19-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="47e19-150">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="47e19-150">The default value is 0.</span></span>

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

### <span data-ttu-id="47e19-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="47e19-151">-ReplacementString</span></span>
<span data-ttu-id="47e19-152">Określa liczbę znaków na końcu tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="47e19-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="47e19-153">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="47e19-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="47e19-154">Wartość domyślna to pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="47e19-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="47e19-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e19-155">-ResourceGroupName</span></span>
<span data-ttu-id="47e19-156">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="47e19-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="47e19-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="47e19-157">-SchemaName</span></span>
<span data-ttu-id="47e19-158">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="47e19-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="47e19-159">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="47e19-159">-ServerName</span></span>
<span data-ttu-id="47e19-160">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="47e19-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="47e19-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="47e19-161">-SuffixSize</span></span>
<span data-ttu-id="47e19-162">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="47e19-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="47e19-163">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="47e19-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="47e19-164">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="47e19-164">The default value is 0.</span></span>

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

### <span data-ttu-id="47e19-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="47e19-165">-TableName</span></span>
<span data-ttu-id="47e19-166">Określa nazwę tabeli bazy danych, która zawiera kolumnę zamaskowane.</span><span class="sxs-lookup"><span data-stu-id="47e19-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="47e19-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47e19-167">-Confirm</span></span>
<span data-ttu-id="47e19-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e19-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e19-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e19-169">-WhatIf</span></span>
<span data-ttu-id="47e19-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e19-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e19-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47e19-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e19-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e19-172">CommonParameters</span></span>
<span data-ttu-id="47e19-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e19-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e19-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47e19-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e19-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47e19-175">INPUTS</span></span>

### <span data-ttu-id="47e19-176">System. String</span><span class="sxs-lookup"><span data-stu-id="47e19-176">System.String</span></span>

### <span data-ttu-id="47e19-177">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="47e19-177">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="47e19-178">System. Nullable "1 [[System. Double, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="47e19-178">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="47e19-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47e19-179">OUTPUTS</span></span>

### <span data-ttu-id="47e19-180">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="47e19-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="47e19-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47e19-181">NOTES</span></span>

## <span data-ttu-id="47e19-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47e19-182">RELATED LINKS</span></span>

[<span data-ttu-id="47e19-183">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="47e19-183">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="47e19-184">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="47e19-184">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="47e19-185">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="47e19-185">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="47e19-186">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="47e19-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

