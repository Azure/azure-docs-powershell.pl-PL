---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b53b32b30e1b69da94ac8319ed3a5f4eee7ffc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524821"
---
# <span data-ttu-id="2f260-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f260-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="2f260-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f260-102">SYNOPSIS</span></span>
<span data-ttu-id="2f260-103">Tworzy regułę maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2f260-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f260-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f260-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f260-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f260-105">DESCRIPTION</span></span>
<span data-ttu-id="2f260-106">Polecenie cmdlet **New-AzureRmSqlDatabaseDataMaskingRule** tworzy regułę maskowania danych dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2f260-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="2f260-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły.</span><span class="sxs-lookup"><span data-stu-id="2f260-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="2f260-108">Podaj wartości *tabelaname* i *ColumnName* , aby określić element docelowy reguły i parametr *MaskingFunction* , aby zdefiniować sposób maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="2f260-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="2f260-109">Jeśli *MaskingFunction* ma wartość liczby lub tekstu, możesz określić parametry *numer* i *NumberTo* , w przypadku maskowania numerów lub *PrefixSize* , *ReplacementString* i *SuffixSize* w celu maskowania tekstu.</span><span class="sxs-lookup"><span data-stu-id="2f260-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="2f260-110">Jeśli wykonanie polecenia powiedzie się i użyto parametru *PassThru* , polecenie cmdlet zwraca obiekt opisujący właściwości reguły maskowania danych oprócz identyfikatorów reguł.</span><span class="sxs-lookup"><span data-stu-id="2f260-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="2f260-111">Identyfikatory reguł obejmują, ale nie są ograniczone do, *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID*.</span><span class="sxs-lookup"><span data-stu-id="2f260-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="2f260-112">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2f260-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2f260-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f260-113">EXAMPLES</span></span>

### <span data-ttu-id="2f260-114">Przykład 1. Tworzenie reguły maskowania danych dla kolumny liczb w bazie danych</span><span class="sxs-lookup"><span data-stu-id="2f260-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="2f260-115">To polecenie tworzy regułę maskowania danych dla kolumny o nazwie Column01 w tabeli o nazwie Table01 w schemacie o nazwie Schema01.</span><span class="sxs-lookup"><span data-stu-id="2f260-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="2f260-116">Baza danych o nazwie Database01 zawiera wszystkie te elementy.</span><span class="sxs-lookup"><span data-stu-id="2f260-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="2f260-117">Reguła jest regułą maskowania liczb, która używa liczby losowej z przedziału od 5 do 14 jako wartości maski.</span><span class="sxs-lookup"><span data-stu-id="2f260-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="2f260-118">Reguła nosi nazwę Rule01.</span><span class="sxs-lookup"><span data-stu-id="2f260-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="2f260-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f260-119">PARAMETERS</span></span>

### <span data-ttu-id="2f260-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2f260-120">-ColumnName</span></span>
<span data-ttu-id="2f260-121">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="2f260-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="2f260-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f260-122">-DatabaseName</span></span>
<span data-ttu-id="2f260-123">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2f260-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f260-124">-DefaultProfile</span></span>
<span data-ttu-id="2f260-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f260-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f260-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="2f260-126">-MaskingFunction</span></span>
<span data-ttu-id="2f260-127">Określa funkcja maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="2f260-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="2f260-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2f260-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f260-129">Domyślne</span><span class="sxs-lookup"><span data-stu-id="2f260-129">Default</span></span>
- <span data-ttu-id="2f260-130">Nomaskowanie</span><span class="sxs-lookup"><span data-stu-id="2f260-130">NoMasking</span></span>
- <span data-ttu-id="2f260-131">SMS</span><span class="sxs-lookup"><span data-stu-id="2f260-131">Text</span></span>
- <span data-ttu-id="2f260-132">Ilości</span><span class="sxs-lookup"><span data-stu-id="2f260-132">Number</span></span>
- <span data-ttu-id="2f260-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="2f260-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="2f260-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="2f260-134">CreditCardNumber</span></span>
- <span data-ttu-id="2f260-135">Adres e-mail</span><span class="sxs-lookup"><span data-stu-id="2f260-135">Email</span></span>

<span data-ttu-id="2f260-136">Domyślną wartością jest wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="2f260-136">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-137">-Numer</span><span class="sxs-lookup"><span data-stu-id="2f260-137">-NumberFrom</span></span>
<span data-ttu-id="2f260-138">Określa dolną liczbę powiązaną interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="2f260-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2f260-139">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="2f260-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2f260-140">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="2f260-140">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="2f260-141">-NumberTo</span></span>
<span data-ttu-id="2f260-142">Określa górną granicę interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="2f260-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2f260-143">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="2f260-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2f260-144">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="2f260-144">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f260-145">-PassThru</span></span>
<span data-ttu-id="2f260-146">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2f260-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f260-147">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2f260-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f260-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="2f260-148">-PrefixSize</span></span>
<span data-ttu-id="2f260-149">Określa liczbę znaków na początku tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="2f260-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="2f260-150">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="2f260-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2f260-151">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="2f260-151">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="2f260-152">-ReplacementString</span></span>
<span data-ttu-id="2f260-153">Określa liczbę znaków na końcu tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="2f260-153">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="2f260-154">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="2f260-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2f260-155">Wartość domyślna to pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="2f260-155">The default value is an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f260-156">-ResourceGroupName</span></span>
<span data-ttu-id="2f260-157">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="2f260-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2f260-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2f260-158">-SchemaName</span></span>
<span data-ttu-id="2f260-159">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="2f260-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="2f260-160">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2f260-160">-ServerName</span></span>
<span data-ttu-id="2f260-161">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="2f260-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2f260-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="2f260-162">-SuffixSize</span></span>
<span data-ttu-id="2f260-163">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="2f260-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="2f260-164">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="2f260-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2f260-165">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="2f260-165">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="2f260-166">-TableName</span></span>
<span data-ttu-id="2f260-167">Określa nazwę tabeli bazy danych, która zawiera kolumnę zamaskowane.</span><span class="sxs-lookup"><span data-stu-id="2f260-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="2f260-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f260-168">-Confirm</span></span>
<span data-ttu-id="2f260-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f260-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f260-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f260-170">-WhatIf</span></span>
<span data-ttu-id="2f260-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f260-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f260-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f260-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f260-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f260-173">CommonParameters</span></span>
<span data-ttu-id="2f260-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f260-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f260-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f260-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f260-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f260-176">INPUTS</span></span>

###  
<span data-ttu-id="2f260-177">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="2f260-177">None.</span></span>

## <span data-ttu-id="2f260-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f260-178">OUTPUTS</span></span>

### <span data-ttu-id="2f260-179">Microsoft. Azure. Commands. SQL. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="2f260-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="2f260-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f260-180">NOTES</span></span>

## <span data-ttu-id="2f260-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f260-181">RELATED LINKS</span></span>

[<span data-ttu-id="2f260-182">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f260-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2f260-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f260-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2f260-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f260-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2f260-185">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2f260-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


