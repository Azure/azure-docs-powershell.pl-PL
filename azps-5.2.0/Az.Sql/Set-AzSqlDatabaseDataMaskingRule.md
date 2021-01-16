---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344425"
---
# <span data-ttu-id="511d0-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="511d0-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="511d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="511d0-102">SYNOPSIS</span></span>
<span data-ttu-id="511d0-103">Ustawia właściwości reguły maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="511d0-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="511d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="511d0-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="511d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="511d0-105">DESCRIPTION</span></span>
<span data-ttu-id="511d0-106">Polecenie cmdlet **Set-AzSqlDatabaseDataMaskingRule** ustawia regułę maskowania danych dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="511d0-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="511d0-107">Aby użyć polecenia cmdlet, podaj parametry *ResourceGroupName*, *nazwa_serwera*, *DatabaseName* i *RuleID* w celu zidentyfikowania reguły.</span><span class="sxs-lookup"><span data-stu-id="511d0-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="511d0-108">Aby przekierować regułę, możesz podać dowolne parametry *SchemaName*, *TableName* i *ColumnName (ColumnName* ).</span><span class="sxs-lookup"><span data-stu-id="511d0-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="511d0-109">Określ parametr *MaskingFunction* , aby zmodyfikować sposób maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="511d0-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="511d0-110">Jeśli określisz wartość liczbową lub tekst dla *MaskingFunction*, możesz określić parametry *numer* i *NumberTo* na potrzeby maskowania numerów lub parametry *PrefixSize*, *ReplacementString* i *SuffixSize* w celu maskowania tekstu.</span><span class="sxs-lookup"><span data-stu-id="511d0-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="511d0-111">Jeśli wykonanie polecenia powiedzie się, a jeśli określisz parametr *PassThru* , polecenie cmdlet zwróci obiekt opisujący właściwości reguły maskowania danych i identyfikatory reguł.</span><span class="sxs-lookup"><span data-stu-id="511d0-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="511d0-112">Identyfikatory reguł obejmują, ale nie są ograniczone do, **ResourceGroupName**, **nazwa_serwera**, **DatabaseName** i **RuleID**.</span><span class="sxs-lookup"><span data-stu-id="511d0-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="511d0-113">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="511d0-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="511d0-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="511d0-114">EXAMPLES</span></span>

### <span data-ttu-id="511d0-115">Przykład 1: Zmienianie zakresu reguły maskowania danych w bazie danych</span><span class="sxs-lookup"><span data-stu-id="511d0-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="511d0-116">To polecenie modyfikuje regułę maskowania danych o IDENTYFIKATORze Rule17.</span><span class="sxs-lookup"><span data-stu-id="511d0-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="511d0-117">Ta reguła działa w bazie danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="511d0-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="511d0-118">To polecenie zmienia granice interwału, w którym jest generowana liczba losowa jako wartość maskowania.</span><span class="sxs-lookup"><span data-stu-id="511d0-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="511d0-119">Nowy zakres to od 23 do 42.</span><span class="sxs-lookup"><span data-stu-id="511d0-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="511d0-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="511d0-120">Example 2</span></span>

<span data-ttu-id="511d0-121">Ustawia właściwości reguły maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="511d0-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="511d0-122">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="511d0-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="511d0-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="511d0-123">PARAMETERS</span></span>

### <span data-ttu-id="511d0-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="511d0-124">-ColumnName</span></span>
<span data-ttu-id="511d0-125">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="511d0-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="511d0-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="511d0-126">-DatabaseName</span></span>
<span data-ttu-id="511d0-127">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="511d0-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="511d0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511d0-128">-DefaultProfile</span></span>
<span data-ttu-id="511d0-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="511d0-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="511d0-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="511d0-130">-MaskingFunction</span></span>
<span data-ttu-id="511d0-131">Określa funkcja maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="511d0-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="511d0-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="511d0-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="511d0-133">Domyślne</span><span class="sxs-lookup"><span data-stu-id="511d0-133">Default</span></span>
- <span data-ttu-id="511d0-134">Nomaskowanie</span><span class="sxs-lookup"><span data-stu-id="511d0-134">NoMasking</span></span>
- <span data-ttu-id="511d0-135">SMS</span><span class="sxs-lookup"><span data-stu-id="511d0-135">Text</span></span>
- <span data-ttu-id="511d0-136">Ilości</span><span class="sxs-lookup"><span data-stu-id="511d0-136">Number</span></span>
- <span data-ttu-id="511d0-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="511d0-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="511d0-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="511d0-138">CreditCardNumber</span></span>
- <span data-ttu-id="511d0-139">Wiadomość e-mail domyślna wartość jest domyślna.</span><span class="sxs-lookup"><span data-stu-id="511d0-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="511d0-140">-Numer</span><span class="sxs-lookup"><span data-stu-id="511d0-140">-NumberFrom</span></span>
<span data-ttu-id="511d0-141">Określa dolną liczbę powiązaną interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="511d0-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="511d0-142">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="511d0-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="511d0-143">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="511d0-143">The default value is 0.</span></span>

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

### <span data-ttu-id="511d0-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="511d0-144">-NumberTo</span></span>
<span data-ttu-id="511d0-145">Określa górną granicę interwału, od którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="511d0-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="511d0-146">Ten parametr należy określić tylko w przypadku określenia wartości liczbowej parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="511d0-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="511d0-147">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="511d0-147">The default value is 0.</span></span>

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

### <span data-ttu-id="511d0-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="511d0-148">-PassThru</span></span>
<span data-ttu-id="511d0-149">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="511d0-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="511d0-150">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="511d0-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="511d0-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="511d0-151">-PrefixSize</span></span>
<span data-ttu-id="511d0-152">Określa liczbę znaków na początku tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="511d0-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="511d0-153">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="511d0-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="511d0-154">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="511d0-154">The default value is 0.</span></span>

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

### <span data-ttu-id="511d0-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="511d0-155">-ReplacementString</span></span>
<span data-ttu-id="511d0-156">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="511d0-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="511d0-157">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="511d0-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="511d0-158">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="511d0-158">The default value is 0.</span></span>

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

### <span data-ttu-id="511d0-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511d0-159">-ResourceGroupName</span></span>
<span data-ttu-id="511d0-160">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="511d0-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="511d0-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="511d0-161">-SchemaName</span></span>
<span data-ttu-id="511d0-162">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="511d0-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="511d0-163">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="511d0-163">-ServerName</span></span>
<span data-ttu-id="511d0-164">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="511d0-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="511d0-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="511d0-165">-SuffixSize</span></span>
<span data-ttu-id="511d0-166">Określa liczbę znaków na końcu tekstu, który nie jest maskowany.</span><span class="sxs-lookup"><span data-stu-id="511d0-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="511d0-167">Ten parametr należy określić tylko w przypadku określenia wartości tekstowej dla parametru *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="511d0-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="511d0-168">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="511d0-168">The default value is 0.</span></span>

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

### <span data-ttu-id="511d0-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="511d0-169">-TableName</span></span>
<span data-ttu-id="511d0-170">Określa nazwę tabeli bazy danych, która zawiera kolumnę zamaskowane.</span><span class="sxs-lookup"><span data-stu-id="511d0-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="511d0-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="511d0-171">-Confirm</span></span>
<span data-ttu-id="511d0-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511d0-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511d0-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511d0-173">-WhatIf</span></span>
<span data-ttu-id="511d0-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511d0-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="511d0-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="511d0-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511d0-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511d0-176">CommonParameters</span></span>
<span data-ttu-id="511d0-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511d0-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511d0-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="511d0-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511d0-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="511d0-179">INPUTS</span></span>

### <span data-ttu-id="511d0-180">System. String</span><span class="sxs-lookup"><span data-stu-id="511d0-180">System.String</span></span>

### <span data-ttu-id="511d0-181">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="511d0-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="511d0-182">System. Nullable "1 [[System. Double, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="511d0-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="511d0-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="511d0-183">OUTPUTS</span></span>

### <span data-ttu-id="511d0-184">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="511d0-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="511d0-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="511d0-185">NOTES</span></span>

## <span data-ttu-id="511d0-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="511d0-186">RELATED LINKS</span></span>

[<span data-ttu-id="511d0-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="511d0-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="511d0-188">Nowe — AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="511d0-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="511d0-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="511d0-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="511d0-190">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="511d0-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


