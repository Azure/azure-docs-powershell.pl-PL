---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b453c11d7a6e63e5365bca5cd186002f66ed13cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995863"
---
# <span data-ttu-id="7db90-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7db90-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="7db90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7db90-102">SYNOPSIS</span></span>
<span data-ttu-id="7db90-103">Tworzy regułę maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7db90-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="7db90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7db90-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7db90-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7db90-105">DESCRIPTION</span></span>
<span data-ttu-id="7db90-106">Polecenie **cmdlet New-AzSqlDatabaseDataMaskingRule** tworzy regułę maskowania danych dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7db90-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="7db90-107">Aby użyć polecenia cmdlet, zidentyfikuj regułę za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName.*</span><span class="sxs-lookup"><span data-stu-id="7db90-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="7db90-108">Podaj wartości *TableName (Nazwa_tabeli)* i *ColumnName* (Nazwa Kolumny), aby określić element docelowy reguły, oraz parametr *MaskingFunction* w celu zdefiniowania sposobu maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="7db90-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="7db90-109">Jeśli *funkcja MaskingFunction* ma wartość Number (Liczba) lub Text (Tekst), można określić parametry *NumberFrom* i *NumberTo* (maskowanie liczb) lub (w przypadku maskowania liczb) lub *PrefixSize*(Rozmiar *Prefiksu), ReplacementString*(Sufiks) i *SufiksSize* (RozmiarSufiku) dla maskowania tekstu.</span><span class="sxs-lookup"><span data-stu-id="7db90-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="7db90-110">Jeśli polecenie się powiedzie i zostanie użyty parametr *PassThru,* polecenie cmdlet zwróci oprócz identyfikatorów reguł obiekt opisujący właściwości reguły maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="7db90-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="7db90-111">Do identyfikatorów reguł należą między innymi nazwa *ResourceGroupName,* *nazwa_serwera,* nazwa_bazy danych i *identyfikator reguły.* </span><span class="sxs-lookup"><span data-stu-id="7db90-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="7db90-112">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7db90-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7db90-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7db90-113">EXAMPLES</span></span>

### <span data-ttu-id="7db90-114">Przykład 1. Tworzenie reguły maskowania danych dla kolumny liczb w bazie danych</span><span class="sxs-lookup"><span data-stu-id="7db90-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="7db90-115">To polecenie tworzy regułę maskowania danych dla kolumny o nazwie Kolumna01 w tabeli o nazwie Tabela01 w schemacie o nazwie Schema01.</span><span class="sxs-lookup"><span data-stu-id="7db90-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="7db90-116">Baza danych o nazwie Database01 zawiera wszystkie te elementy.</span><span class="sxs-lookup"><span data-stu-id="7db90-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="7db90-117">Reguła jest regułą maskowania liczb, która używa liczby losowej zamiejscowej od 5 do 14 jako wartości maski.</span><span class="sxs-lookup"><span data-stu-id="7db90-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="7db90-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7db90-118">PARAMETERS</span></span>

### <span data-ttu-id="7db90-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7db90-119">-ColumnName</span></span>
<span data-ttu-id="7db90-120">Określa nazwę kolumny docelowej przez regułę maskowania.</span><span class="sxs-lookup"><span data-stu-id="7db90-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="7db90-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7db90-121">-DatabaseName</span></span>
<span data-ttu-id="7db90-122">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7db90-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="7db90-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db90-123">-DefaultProfile</span></span>
<span data-ttu-id="7db90-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7db90-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7db90-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="7db90-125">-MaskingFunction</span></span>
<span data-ttu-id="7db90-126">Określa funkcję maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="7db90-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="7db90-127">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7db90-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7db90-128">Domyślne</span><span class="sxs-lookup"><span data-stu-id="7db90-128">Default</span></span>
- <span data-ttu-id="7db90-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="7db90-129">NoMasking</span></span>
- <span data-ttu-id="7db90-130">Tekst</span><span class="sxs-lookup"><span data-stu-id="7db90-130">Text</span></span>
- <span data-ttu-id="7db90-131">Numer</span><span class="sxs-lookup"><span data-stu-id="7db90-131">Number</span></span>
- <span data-ttu-id="7db90-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="7db90-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="7db90-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="7db90-133">CreditCardNumber</span></span>
- <span data-ttu-id="7db90-134">Wiadomość e-mail Wartość domyślna to Domyślna.</span><span class="sxs-lookup"><span data-stu-id="7db90-134">Email The default value is Default.</span></span>

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

### <span data-ttu-id="7db90-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="7db90-135">-NumberFrom</span></span>
<span data-ttu-id="7db90-136">Określa dolną liczbę powiązaną interwału, z którego jest wybierana losowa wartość.</span><span class="sxs-lookup"><span data-stu-id="7db90-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="7db90-137">Określ ten parametr tylko w przypadku określenia wartości number dla *parametru MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="7db90-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7db90-138">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="7db90-138">The default value is 0.</span></span>

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

### <span data-ttu-id="7db90-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="7db90-139">-NumberTo</span></span>
<span data-ttu-id="7db90-140">Określa górną liczbę powiązaną interwału, z którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="7db90-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="7db90-141">Określ ten parametr tylko w przypadku określenia wartości number dla *parametru MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="7db90-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7db90-142">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="7db90-142">The default value is 0.</span></span>

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

### <span data-ttu-id="7db90-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7db90-143">-PassThru</span></span>
<span data-ttu-id="7db90-144">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7db90-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7db90-145">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7db90-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7db90-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="7db90-146">-PrefixSize</span></span>
<span data-ttu-id="7db90-147">Określa liczbę znaków na początku tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="7db90-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="7db90-148">Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.</span><span class="sxs-lookup"><span data-stu-id="7db90-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7db90-149">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="7db90-149">The default value is 0.</span></span>

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

### <span data-ttu-id="7db90-150">- ReplacementString</span><span class="sxs-lookup"><span data-stu-id="7db90-150">-ReplacementString</span></span>
<span data-ttu-id="7db90-151">Określa liczbę znaków na końcu tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="7db90-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="7db90-152">Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.</span><span class="sxs-lookup"><span data-stu-id="7db90-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7db90-153">Wartość domyślna jest ciągiem pustym.</span><span class="sxs-lookup"><span data-stu-id="7db90-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="7db90-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db90-154">-ResourceGroupName</span></span>
<span data-ttu-id="7db90-155">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="7db90-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7db90-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7db90-156">-SchemaName</span></span>
<span data-ttu-id="7db90-157">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="7db90-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="7db90-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7db90-158">-ServerName</span></span>
<span data-ttu-id="7db90-159">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7db90-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7db90-160">-SufiksSize</span><span class="sxs-lookup"><span data-stu-id="7db90-160">-SuffixSize</span></span>
<span data-ttu-id="7db90-161">Określa liczbę znaków na końcu tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="7db90-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="7db90-162">Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.</span><span class="sxs-lookup"><span data-stu-id="7db90-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7db90-163">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="7db90-163">The default value is 0.</span></span>

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

### <span data-ttu-id="7db90-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="7db90-164">-TableName</span></span>
<span data-ttu-id="7db90-165">Określa nazwę tabeli bazy danych zawierającej zamaskowana kolumnę.</span><span class="sxs-lookup"><span data-stu-id="7db90-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="7db90-166">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7db90-166">-Confirm</span></span>
<span data-ttu-id="7db90-167">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7db90-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db90-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db90-168">-WhatIf</span></span>
<span data-ttu-id="7db90-169">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7db90-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7db90-170">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7db90-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db90-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db90-171">CommonParameters</span></span>
<span data-ttu-id="7db90-172">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db90-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db90-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7db90-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db90-174">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7db90-174">INPUTS</span></span>

### <span data-ttu-id="7db90-175">System.String</span><span class="sxs-lookup"><span data-stu-id="7db90-175">System.String</span></span>

### <span data-ttu-id="7db90-176">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7db90-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7db90-177">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7db90-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7db90-178">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7db90-178">OUTPUTS</span></span>

### <span data-ttu-id="7db90-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="7db90-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="7db90-180">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7db90-180">NOTES</span></span>

## <span data-ttu-id="7db90-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7db90-181">RELATED LINKS</span></span>

[<span data-ttu-id="7db90-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7db90-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7db90-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7db90-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7db90-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7db90-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7db90-185">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7db90-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


