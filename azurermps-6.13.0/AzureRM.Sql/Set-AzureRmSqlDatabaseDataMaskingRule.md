---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 4e5f2578d0e9dbb2139b330ec0a7c2fe81b3124e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527774"
---
# <span data-ttu-id="fad9a-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fad9a-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="fad9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fad9a-102">SYNOPSIS</span></span>
<span data-ttu-id="fad9a-103">Ustawia właściwości reguły maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fad9a-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fad9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fad9a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fad9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fad9a-105">DESCRIPTION</span></span>
<span data-ttu-id="fad9a-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseDataMaskingRule** ustawia regułę maskowania danych dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fad9a-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="fad9a-107">Aby użyć polecenia cmdlet, podaj parametry *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły.</span><span class="sxs-lookup"><span data-stu-id="fad9a-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="fad9a-108">Aby przekierować regułę, możesz podać dowolne parametry *SchemaName* , *TableName* i *ColumnName (ColumnName* ).</span><span class="sxs-lookup"><span data-stu-id="fad9a-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="fad9a-109">Określ parametr *MaskingFunction* , aby zmodyfikować sposób maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="fad9a-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="fad9a-110">Jeśli określisz wartość liczbową lub tekst dla *MaskingFunction* , możesz określić parametry *numer* i *NumberTo* na potrzeby maskowania numerów lub parametry *PrefixSize* , *ReplacementString* i *SuffixSize* w celu maskowania tekstu.</span><span class="sxs-lookup"><span data-stu-id="fad9a-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="fad9a-111">Jeśli wykonanie polecenia powiedzie się, a jeśli określisz parametr *PassThru* , polecenie cmdlet zwróci obiekt opisujący właściwości reguły maskowania danych i identyfikatory reguł.</span><span class="sxs-lookup"><span data-stu-id="fad9a-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="fad9a-112">Identyfikatory reguł obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** , **DatabaseName** i **RuleID**.</span><span class="sxs-lookup"><span data-stu-id="fad9a-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="fad9a-113">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fad9a-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fad9a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fad9a-114">EXAMPLES</span></span>

### <span data-ttu-id="fad9a-115">Przykład 1: Zmienianie zakresu reguły maskowania danych w bazie danych</span><span class="sxs-lookup"><span data-stu-id="fad9a-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="fad9a-116">To polecenie modyfikuje regułę maskowania danych o IDENTYFIKATORze Rule17.</span><span class="sxs-lookup"><span data-stu-id="fad9a-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="fad9a-117">Ta reguła działa w bazie danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="fad9a-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="fad9a-118">To polecenie zmienia granice interwału, w którym jest generowana liczba losowa jako wartość maskowania.</span><span class="sxs-lookup"><span data-stu-id="fad9a-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="fad9a-119">Nowy zakres to od 23 do 42.</span><span class="sxs-lookup"><span data-stu-id="fad9a-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="fad9a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fad9a-120">PARAMETERS</span></span>

### <span data-ttu-id="fad9a-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="fad9a-121">-ColumnName</span></span>
<span data-ttu-id="fad9a-122">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="fad9a-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="fad9a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fad9a-123">-DatabaseName</span></span>
<span data-ttu-id="fad9a-124">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fad9a-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fad9a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad9a-125">-DefaultProfile</span></span>
<span data-ttu-id="fad9a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fad9a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fad9a-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="fad9a-127">-MaskingFunction</span></span>
<span data-ttu-id="fad9a-128">Określa funkcja maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="fad9a-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="fad9a-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fad9a-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fad9a-130">Domyślne</span><span class="sxs-lookup"><span data-stu-id="fad9a-130">Default</span></span>
- <span data-ttu-id="fad9a-131">Nomaskowanie</span><span class="sxs-lookup"><span data-stu-id="fad9a-131">NoMasking</span></span>
- <span data-ttu-id="fad9a-132">SMS</span><span class="sxs-lookup"><span data-stu-id="fad9a-132">Text</span></span>
- <span data-ttu-id="fad9a-133">Ilości</span><span class="sxs-lookup"><span data-stu-id="fad9a-133">Number</span></span>
- <span data-ttu-id="fad9a-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="fad9a-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="fad9a-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="fad9a-135">CreditCardNumber</span></span>
- <span data-ttu-id="fad9a-136">Wiadomość e-mail domyślna wartość jest domyślna.</span><span class="sxs-lookup"><span data-stu-id="fad9a-136">Email The default value is Default.</span></span>

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

### <span data-ttu-id="fad9a-137">-Numer</span><span class="sxs-lookup"><span data-stu-id="fad9a-137">-NumberFrom</span></span>
<span data-ttu-id="fad9a-138">Określa dolną liczbę powiązaną interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="fad9a-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="fad9a-139">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="fad9a-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="fad9a-140">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="fad9a-140">The default value is 0.</span></span>

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

### <span data-ttu-id="fad9a-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="fad9a-141">-NumberTo</span></span>
<span data-ttu-id="fad9a-142">Określa górną granicę interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="fad9a-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="fad9a-143">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="fad9a-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="fad9a-144">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="fad9a-144">The default value is 0.</span></span>

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

### <span data-ttu-id="fad9a-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fad9a-145">-PassThru</span></span>
<span data-ttu-id="fad9a-146">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fad9a-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fad9a-147">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fad9a-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fad9a-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="fad9a-148">-PrefixSize</span></span>
<span data-ttu-id="fad9a-149">Określa liczbę znaków na początku tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="fad9a-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="fad9a-150">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="fad9a-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="fad9a-151">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="fad9a-151">The default value is 0.</span></span>

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

### <span data-ttu-id="fad9a-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="fad9a-152">-ReplacementString</span></span>
<span data-ttu-id="fad9a-153">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="fad9a-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="fad9a-154">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="fad9a-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="fad9a-155">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="fad9a-155">The default value is 0.</span></span>

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

### <span data-ttu-id="fad9a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad9a-156">-ResourceGroupName</span></span>
<span data-ttu-id="fad9a-157">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="fad9a-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fad9a-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fad9a-158">-SchemaName</span></span>
<span data-ttu-id="fad9a-159">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="fad9a-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="fad9a-160">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fad9a-160">-ServerName</span></span>
<span data-ttu-id="fad9a-161">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="fad9a-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fad9a-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="fad9a-162">-SuffixSize</span></span>
<span data-ttu-id="fad9a-163">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="fad9a-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="fad9a-164">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="fad9a-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="fad9a-165">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="fad9a-165">The default value is 0.</span></span>

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

### <span data-ttu-id="fad9a-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="fad9a-166">-TableName</span></span>
<span data-ttu-id="fad9a-167">Określa nazwę tabeli bazy danych, która zawiera kolumnę zamaskowane.</span><span class="sxs-lookup"><span data-stu-id="fad9a-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="fad9a-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fad9a-168">-Confirm</span></span>
<span data-ttu-id="fad9a-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fad9a-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fad9a-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fad9a-170">-WhatIf</span></span>
<span data-ttu-id="fad9a-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fad9a-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fad9a-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fad9a-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fad9a-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad9a-173">CommonParameters</span></span>
<span data-ttu-id="fad9a-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad9a-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad9a-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad9a-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad9a-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fad9a-176">INPUTS</span></span>

### <span data-ttu-id="fad9a-177">System. String</span><span class="sxs-lookup"><span data-stu-id="fad9a-177">System.String</span></span>

### <span data-ttu-id="fad9a-178">System. Nullable ' 1 [[System. UInt32; mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fad9a-178">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fad9a-179">System. Nullable "1 [[System. Double, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fad9a-179">System.Nullable\`1[[System.Double, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fad9a-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fad9a-180">OUTPUTS</span></span>

### <span data-ttu-id="fad9a-181">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="fad9a-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="fad9a-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fad9a-182">NOTES</span></span>

## <span data-ttu-id="fad9a-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fad9a-183">RELATED LINKS</span></span>

[<span data-ttu-id="fad9a-184">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fad9a-184">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fad9a-185">Nowe — AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fad9a-185">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fad9a-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fad9a-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fad9a-187">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fad9a-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

