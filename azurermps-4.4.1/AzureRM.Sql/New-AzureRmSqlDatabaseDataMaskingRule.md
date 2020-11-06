---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 6facaef4255d37ccaa0e2c192c40c8888d485357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553740"
---
# <span data-ttu-id="dcab7-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="dcab7-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="dcab7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcab7-102">SYNOPSIS</span></span>
<span data-ttu-id="dcab7-103">Tworzy regułę maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dcab7-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcab7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcab7-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcab7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dcab7-105">DESCRIPTION</span></span>
<span data-ttu-id="dcab7-106">Polecenie cmdlet **New-AzureRmSqlDatabaseDataMaskingRule** tworzy regułę maskowania danych dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dcab7-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="dcab7-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły.</span><span class="sxs-lookup"><span data-stu-id="dcab7-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="dcab7-108">Podaj wartości *tabelaname* i *ColumnName* , aby określić element docelowy reguły i parametr *MaskingFunction* , aby zdefiniować sposób maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="dcab7-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="dcab7-109">Jeśli *MaskingFunction* ma wartość liczby lub tekstu, możesz określić parametry *numer* i *NumberTo* , w przypadku maskowania numerów lub *PrefixSize* , *ReplacementString* i *SuffixSize* w celu maskowania tekstu.</span><span class="sxs-lookup"><span data-stu-id="dcab7-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="dcab7-110">Jeśli wykonanie polecenia powiedzie się i użyto parametru *PassThru* , polecenie cmdlet zwraca obiekt opisujący właściwości reguły maskowania danych oprócz identyfikatorów reguł.</span><span class="sxs-lookup"><span data-stu-id="dcab7-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="dcab7-111">Identyfikatory reguł obejmują, ale nie są ograniczone do, *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID*.</span><span class="sxs-lookup"><span data-stu-id="dcab7-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="dcab7-112">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="dcab7-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="dcab7-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcab7-113">EXAMPLES</span></span>

### <span data-ttu-id="dcab7-114">Przykład 1. Tworzenie reguły maskowania danych dla kolumny liczb w bazie danych</span><span class="sxs-lookup"><span data-stu-id="dcab7-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="dcab7-115">To polecenie tworzy regułę maskowania danych dla kolumny o nazwie Column01 w tabeli o nazwie Table01 w schemacie o nazwie Schema01.</span><span class="sxs-lookup"><span data-stu-id="dcab7-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="dcab7-116">Baza danych o nazwie Database01 zawiera wszystkie te elementy.</span><span class="sxs-lookup"><span data-stu-id="dcab7-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="dcab7-117">Reguła jest regułą maskowania liczb, która używa liczby losowej z przedziału od 5 do 14 jako wartości maski.</span><span class="sxs-lookup"><span data-stu-id="dcab7-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="dcab7-118">Reguła nosi nazwę Rule01.</span><span class="sxs-lookup"><span data-stu-id="dcab7-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="dcab7-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcab7-119">PARAMETERS</span></span>

### <span data-ttu-id="dcab7-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="dcab7-120">-ColumnName</span></span>
<span data-ttu-id="dcab7-121">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="dcab7-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="dcab7-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dcab7-122">-DatabaseName</span></span>
<span data-ttu-id="dcab7-123">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dcab7-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="dcab7-124">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="dcab7-124">-MaskingFunction</span></span>
<span data-ttu-id="dcab7-125">Określa funkcja maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="dcab7-125">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="dcab7-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dcab7-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dcab7-127">Domyślne</span><span class="sxs-lookup"><span data-stu-id="dcab7-127">Default</span></span>
- <span data-ttu-id="dcab7-128">Nomaskowanie</span><span class="sxs-lookup"><span data-stu-id="dcab7-128">NoMasking</span></span>
- <span data-ttu-id="dcab7-129">SMS</span><span class="sxs-lookup"><span data-stu-id="dcab7-129">Text</span></span>
- <span data-ttu-id="dcab7-130">Ilości</span><span class="sxs-lookup"><span data-stu-id="dcab7-130">Number</span></span>
- <span data-ttu-id="dcab7-131">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="dcab7-131">SocialSecurityNumber</span></span>
- <span data-ttu-id="dcab7-132">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="dcab7-132">CreditCardNumber</span></span>
- <span data-ttu-id="dcab7-133">Adres e-mail</span><span class="sxs-lookup"><span data-stu-id="dcab7-133">Email</span></span>

<span data-ttu-id="dcab7-134">Domyślną wartością jest wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="dcab7-134">The default value is Default.</span></span>

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

### <span data-ttu-id="dcab7-135">-Numer</span><span class="sxs-lookup"><span data-stu-id="dcab7-135">-NumberFrom</span></span>
<span data-ttu-id="dcab7-136">Określa dolną liczbę powiązaną interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="dcab7-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="dcab7-137">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="dcab7-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="dcab7-138">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="dcab7-138">The default value is 0.</span></span>

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

### <span data-ttu-id="dcab7-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="dcab7-139">-NumberTo</span></span>
<span data-ttu-id="dcab7-140">Określa górną granicę interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="dcab7-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="dcab7-141">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="dcab7-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="dcab7-142">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="dcab7-142">The default value is 0.</span></span>

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

### <span data-ttu-id="dcab7-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcab7-143">-PassThru</span></span>
<span data-ttu-id="dcab7-144">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="dcab7-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dcab7-145">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dcab7-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dcab7-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="dcab7-146">-PrefixSize</span></span>
<span data-ttu-id="dcab7-147">Określa liczbę znaków na początku tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="dcab7-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="dcab7-148">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="dcab7-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="dcab7-149">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="dcab7-149">The default value is 0.</span></span>

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

### <span data-ttu-id="dcab7-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="dcab7-150">-ReplacementString</span></span>
<span data-ttu-id="dcab7-151">Określa liczbę znaków na końcu tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="dcab7-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="dcab7-152">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="dcab7-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="dcab7-153">Wartość domyślna to pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="dcab7-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="dcab7-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcab7-154">-ResourceGroupName</span></span>
<span data-ttu-id="dcab7-155">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="dcab7-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="dcab7-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dcab7-156">-SchemaName</span></span>
<span data-ttu-id="dcab7-157">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="dcab7-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="dcab7-158">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="dcab7-158">-ServerName</span></span>
<span data-ttu-id="dcab7-159">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="dcab7-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="dcab7-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="dcab7-160">-SuffixSize</span></span>
<span data-ttu-id="dcab7-161">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="dcab7-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="dcab7-162">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="dcab7-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="dcab7-163">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="dcab7-163">The default value is 0.</span></span>

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

### <span data-ttu-id="dcab7-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="dcab7-164">-TableName</span></span>
<span data-ttu-id="dcab7-165">Określa nazwę tabeli bazy danych, która zawiera kolumnę zamaskowane.</span><span class="sxs-lookup"><span data-stu-id="dcab7-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="dcab7-166">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcab7-166">-Confirm</span></span>
<span data-ttu-id="dcab7-167">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcab7-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcab7-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcab7-168">-WhatIf</span></span>
<span data-ttu-id="dcab7-169">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcab7-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcab7-170">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dcab7-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcab7-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcab7-171">-DefaultProfile</span></span>
<span data-ttu-id="dcab7-172">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcab7-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcab7-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcab7-173">CommonParameters</span></span>
<span data-ttu-id="dcab7-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcab7-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcab7-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcab7-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcab7-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcab7-176">INPUTS</span></span>

###  
<span data-ttu-id="dcab7-177">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="dcab7-177">None.</span></span>

## <span data-ttu-id="dcab7-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcab7-178">OUTPUTS</span></span>

### <span data-ttu-id="dcab7-179">Microsoft. Azure. Commands. SQL. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="dcab7-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="dcab7-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcab7-180">NOTES</span></span>

## <span data-ttu-id="dcab7-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcab7-181">RELATED LINKS</span></span>

[<span data-ttu-id="dcab7-182">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="dcab7-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="dcab7-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="dcab7-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="dcab7-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="dcab7-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="dcab7-185">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="dcab7-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


