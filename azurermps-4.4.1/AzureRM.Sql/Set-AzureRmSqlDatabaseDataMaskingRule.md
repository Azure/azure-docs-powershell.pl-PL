---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527193"
---
# <span data-ttu-id="5467a-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5467a-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="5467a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5467a-102">SYNOPSIS</span></span>
<span data-ttu-id="5467a-103">Ustawia właściwości reguły maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5467a-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5467a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5467a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5467a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5467a-105">DESCRIPTION</span></span>
<span data-ttu-id="5467a-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseDataMaskingRule** ustawia regułę maskowania danych dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5467a-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="5467a-107">Aby użyć polecenia cmdlet, podaj parametry *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły.</span><span class="sxs-lookup"><span data-stu-id="5467a-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="5467a-108">Aby przekierować regułę, możesz podać dowolne parametry *SchemaName* , *TableName* i *ColumnName (ColumnName* ).</span><span class="sxs-lookup"><span data-stu-id="5467a-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="5467a-109">Określ parametr *MaskingFunction* , aby zmodyfikować sposób maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="5467a-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="5467a-110">Jeśli określisz wartość liczbową lub tekst dla *MaskingFunction* , możesz określić parametry *numer* i *NumberTo* na potrzeby maskowania numerów lub parametry *PrefixSize* , *ReplacementString* i *SuffixSize* w celu maskowania tekstu.</span><span class="sxs-lookup"><span data-stu-id="5467a-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="5467a-111">Jeśli wykonanie polecenia powiedzie się, a jeśli określisz parametr *PassThru* , polecenie cmdlet zwróci obiekt opisujący właściwości reguły maskowania danych i identyfikatory reguł.</span><span class="sxs-lookup"><span data-stu-id="5467a-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="5467a-112">Identyfikatory reguł obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** , **DatabaseName** i **RuleID**.</span><span class="sxs-lookup"><span data-stu-id="5467a-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="5467a-113">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5467a-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5467a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5467a-114">EXAMPLES</span></span>

### <span data-ttu-id="5467a-115">Przykład 1: Zmienianie zakresu reguły maskowania danych w bazie danych</span><span class="sxs-lookup"><span data-stu-id="5467a-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="5467a-116">To polecenie modyfikuje regułę maskowania danych o IDENTYFIKATORze Rule17.</span><span class="sxs-lookup"><span data-stu-id="5467a-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="5467a-117">Ta reguła działa w bazie danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="5467a-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="5467a-118">To polecenie zmienia granice interwału, w którym jest generowana liczba losowa jako wartość maskowania.</span><span class="sxs-lookup"><span data-stu-id="5467a-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="5467a-119">Nowy zakres to od 23 do 42.</span><span class="sxs-lookup"><span data-stu-id="5467a-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="5467a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5467a-120">PARAMETERS</span></span>

### <span data-ttu-id="5467a-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5467a-121">-ColumnName</span></span>
<span data-ttu-id="5467a-122">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="5467a-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="5467a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5467a-123">-DatabaseName</span></span>
<span data-ttu-id="5467a-124">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5467a-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5467a-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="5467a-125">-MaskingFunction</span></span>
<span data-ttu-id="5467a-126">Określa funkcja maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="5467a-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="5467a-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5467a-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5467a-128">Domyślne</span><span class="sxs-lookup"><span data-stu-id="5467a-128">Default</span></span>
- <span data-ttu-id="5467a-129">Nomaskowanie</span><span class="sxs-lookup"><span data-stu-id="5467a-129">NoMasking</span></span>
- <span data-ttu-id="5467a-130">SMS</span><span class="sxs-lookup"><span data-stu-id="5467a-130">Text</span></span>
- <span data-ttu-id="5467a-131">Ilości</span><span class="sxs-lookup"><span data-stu-id="5467a-131">Number</span></span>
- <span data-ttu-id="5467a-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="5467a-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="5467a-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="5467a-133">CreditCardNumber</span></span>
- <span data-ttu-id="5467a-134">Adres e-mail</span><span class="sxs-lookup"><span data-stu-id="5467a-134">Email</span></span>

<span data-ttu-id="5467a-135">Domyślną wartością jest wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="5467a-135">The default value is Default.</span></span>

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

### <span data-ttu-id="5467a-136">-Numer</span><span class="sxs-lookup"><span data-stu-id="5467a-136">-NumberFrom</span></span>
<span data-ttu-id="5467a-137">Określa dolną liczbę powiązaną interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="5467a-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="5467a-138">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="5467a-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5467a-139">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="5467a-139">The default value is 0.</span></span>

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

### <span data-ttu-id="5467a-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="5467a-140">-NumberTo</span></span>
<span data-ttu-id="5467a-141">Określa górną granicę interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="5467a-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="5467a-142">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="5467a-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5467a-143">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="5467a-143">The default value is 0.</span></span>

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

### <span data-ttu-id="5467a-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5467a-144">-PassThru</span></span>
<span data-ttu-id="5467a-145">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5467a-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5467a-146">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5467a-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5467a-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="5467a-147">-PrefixSize</span></span>
<span data-ttu-id="5467a-148">Określa liczbę znaków na początku tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="5467a-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="5467a-149">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="5467a-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5467a-150">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="5467a-150">The default value is 0.</span></span>

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

### <span data-ttu-id="5467a-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="5467a-151">-ReplacementString</span></span>
<span data-ttu-id="5467a-152">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="5467a-152">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="5467a-153">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="5467a-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5467a-154">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="5467a-154">The default value is 0.</span></span>

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

### <span data-ttu-id="5467a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5467a-155">-ResourceGroupName</span></span>
<span data-ttu-id="5467a-156">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="5467a-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5467a-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5467a-157">-SchemaName</span></span>
<span data-ttu-id="5467a-158">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="5467a-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="5467a-159">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5467a-159">-ServerName</span></span>
<span data-ttu-id="5467a-160">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="5467a-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5467a-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="5467a-161">-SuffixSize</span></span>
<span data-ttu-id="5467a-162">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="5467a-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="5467a-163">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="5467a-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5467a-164">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="5467a-164">The default value is 0.</span></span>

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

### <span data-ttu-id="5467a-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="5467a-165">-TableName</span></span>
<span data-ttu-id="5467a-166">Określa nazwę tabeli bazy danych, która zawiera kolumnę zamaskowane.</span><span class="sxs-lookup"><span data-stu-id="5467a-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="5467a-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5467a-167">-Confirm</span></span>
<span data-ttu-id="5467a-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5467a-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5467a-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5467a-169">-WhatIf</span></span>
<span data-ttu-id="5467a-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5467a-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5467a-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5467a-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5467a-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5467a-172">-DefaultProfile</span></span>
<span data-ttu-id="5467a-173">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5467a-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5467a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5467a-174">CommonParameters</span></span>
<span data-ttu-id="5467a-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5467a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5467a-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5467a-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5467a-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5467a-177">INPUTS</span></span>

###  
<span data-ttu-id="5467a-178">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5467a-178">None</span></span>

## <span data-ttu-id="5467a-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5467a-179">OUTPUTS</span></span>

### <span data-ttu-id="5467a-180">Microsoft. Azure. Commands. SQL. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="5467a-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="5467a-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5467a-181">NOTES</span></span>

## <span data-ttu-id="5467a-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5467a-182">RELATED LINKS</span></span>

[<span data-ttu-id="5467a-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5467a-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5467a-184">Nowe — AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5467a-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5467a-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5467a-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5467a-186">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5467a-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


