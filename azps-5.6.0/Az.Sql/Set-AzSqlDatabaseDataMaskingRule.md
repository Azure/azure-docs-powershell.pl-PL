---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8ed90e6c3a145298029f1ef4d12b6248ed39526e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994918"
---
# <span data-ttu-id="08376-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08376-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="08376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08376-102">SYNOPSIS</span></span>
<span data-ttu-id="08376-103">Ustawia właściwości reguły maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="08376-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="08376-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="08376-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08376-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="08376-105">DESCRIPTION</span></span>
<span data-ttu-id="08376-106">Polecenie **cmdlet Set-AzSqlDatabaseDataMaskingRule** ustawia regułę maskowania danych dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="08376-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="08376-107">Aby użyć polecenia cmdlet, podaj parametry *ResourceGroupName* *,ServerName,* *DatabaseName* i *RuleId* (Nazwa_bazy danych) w celu zidentyfikowania reguły.</span><span class="sxs-lookup"><span data-stu-id="08376-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="08376-108">Możesz podać dowolny z parametrów *nazwa_schematu,* *nazwa_tabeli* i nazwa_kolumny, aby ponownie określić regułę. </span><span class="sxs-lookup"><span data-stu-id="08376-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="08376-109">Określenie *parametru MaskingFunction* w celu zmodyfikowania sposobu maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="08376-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="08376-110">W przypadku określenia wartości Number (Liczba) lub Text for *MaskingFunction*(Tekst dla funkcji maskowania) można określić parametry NumberFrom (LiczbaZ) i *NumberTo* (NumberFrom) dla maskowania liczb lub parametry *PrefixSize*(Rozmiar *Prefiksu), ReplacementString* i *SuffixSize* (RozmiarSufiksu) dla maskowania tekstu. </span><span class="sxs-lookup"><span data-stu-id="08376-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="08376-111">Jeśli polecenie się powiedzie i określisz parametr *PassThru,* polecenie cmdlet zwróci obiekt opisujący właściwości reguły maskowania danych i identyfikatory reguł.</span><span class="sxs-lookup"><span data-stu-id="08376-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="08376-112">Do identyfikatorów reguł należą między innymi nazwa **ResourceGroupName,** **Nazwa_serwera,** **Nazwa_bazy** danych i **Reguła.**</span><span class="sxs-lookup"><span data-stu-id="08376-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="08376-113">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="08376-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="08376-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="08376-114">EXAMPLES</span></span>

### <span data-ttu-id="08376-115">Przykład 1. Zmienianie zakresu reguły maskowania danych w bazie danych</span><span class="sxs-lookup"><span data-stu-id="08376-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="08376-116">To polecenie modyfikuje regułę maskowania danych, która ma regułę identyfikatorów 17.</span><span class="sxs-lookup"><span data-stu-id="08376-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="08376-117">Ta reguła działa w bazie danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="08376-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="08376-118">To polecenie zmienia granice interwału, w którym liczba losowa jest generowana jako zamaskowana wartość.</span><span class="sxs-lookup"><span data-stu-id="08376-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="08376-119">Nowy zakres to między 23 a 42.</span><span class="sxs-lookup"><span data-stu-id="08376-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="08376-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="08376-120">Example 2</span></span>

<span data-ttu-id="08376-121">Ustawia właściwości reguły maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="08376-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="08376-122">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="08376-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="08376-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08376-123">PARAMETERS</span></span>

### <span data-ttu-id="08376-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="08376-124">-ColumnName</span></span>
<span data-ttu-id="08376-125">Określa nazwę kolumny docelowej przez regułę maskowania.</span><span class="sxs-lookup"><span data-stu-id="08376-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="08376-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08376-126">-DatabaseName</span></span>
<span data-ttu-id="08376-127">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="08376-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="08376-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08376-128">-DefaultProfile</span></span>
<span data-ttu-id="08376-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="08376-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08376-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="08376-130">-MaskingFunction</span></span>
<span data-ttu-id="08376-131">Określa funkcję maskowania używaną przez regułę.</span><span class="sxs-lookup"><span data-stu-id="08376-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="08376-132">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="08376-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08376-133">Domyślne</span><span class="sxs-lookup"><span data-stu-id="08376-133">Default</span></span>
- <span data-ttu-id="08376-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="08376-134">NoMasking</span></span>
- <span data-ttu-id="08376-135">Tekst</span><span class="sxs-lookup"><span data-stu-id="08376-135">Text</span></span>
- <span data-ttu-id="08376-136">Numer</span><span class="sxs-lookup"><span data-stu-id="08376-136">Number</span></span>
- <span data-ttu-id="08376-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="08376-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="08376-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="08376-138">CreditCardNumber</span></span>
- <span data-ttu-id="08376-139">Wiadomość e-mail Wartość domyślna to Domyślna.</span><span class="sxs-lookup"><span data-stu-id="08376-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="08376-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="08376-140">-NumberFrom</span></span>
<span data-ttu-id="08376-141">Określa dolną liczbę powiązaną interwału, z którego jest wybierana losowa wartość.</span><span class="sxs-lookup"><span data-stu-id="08376-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="08376-142">Określ ten parametr tylko w przypadku określenia wartości number dla *parametru MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="08376-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="08376-143">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="08376-143">The default value is 0.</span></span>

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

### <span data-ttu-id="08376-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="08376-144">-NumberTo</span></span>
<span data-ttu-id="08376-145">Określa górną liczbę powiązaną interwału, z którego jest wybierana wartość losowa.</span><span class="sxs-lookup"><span data-stu-id="08376-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="08376-146">Określ ten parametr tylko w przypadku określenia wartości number dla *parametru MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="08376-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="08376-147">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="08376-147">The default value is 0.</span></span>

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

### <span data-ttu-id="08376-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08376-148">-PassThru</span></span>
<span data-ttu-id="08376-149">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="08376-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="08376-150">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="08376-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08376-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="08376-151">-PrefixSize</span></span>
<span data-ttu-id="08376-152">Określa liczbę znaków na początku tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="08376-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="08376-153">Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.</span><span class="sxs-lookup"><span data-stu-id="08376-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="08376-154">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="08376-154">The default value is 0.</span></span>

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

### <span data-ttu-id="08376-155">- ReplacementString</span><span class="sxs-lookup"><span data-stu-id="08376-155">-ReplacementString</span></span>
<span data-ttu-id="08376-156">Określa liczbę znaków na końcu tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="08376-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="08376-157">Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.</span><span class="sxs-lookup"><span data-stu-id="08376-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="08376-158">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="08376-158">The default value is 0.</span></span>

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

### <span data-ttu-id="08376-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08376-159">-ResourceGroupName</span></span>
<span data-ttu-id="08376-160">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="08376-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="08376-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="08376-161">-SchemaName</span></span>
<span data-ttu-id="08376-162">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="08376-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="08376-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08376-163">-ServerName</span></span>
<span data-ttu-id="08376-164">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="08376-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="08376-165">-SufiksSize</span><span class="sxs-lookup"><span data-stu-id="08376-165">-SuffixSize</span></span>
<span data-ttu-id="08376-166">Określa liczbę znaków na końcu tekstu, które nie są maskowane.</span><span class="sxs-lookup"><span data-stu-id="08376-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="08376-167">Określ ten parametr tylko wtedy, gdy dla parametru *MaskingFunction* określisz wartość Tekst.</span><span class="sxs-lookup"><span data-stu-id="08376-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="08376-168">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="08376-168">The default value is 0.</span></span>

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

### <span data-ttu-id="08376-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="08376-169">-TableName</span></span>
<span data-ttu-id="08376-170">Określa nazwę tabeli bazy danych zawierającej zamaskowana kolumnę.</span><span class="sxs-lookup"><span data-stu-id="08376-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="08376-171">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08376-171">-Confirm</span></span>
<span data-ttu-id="08376-172">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="08376-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08376-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08376-173">-WhatIf</span></span>
<span data-ttu-id="08376-174">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08376-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08376-175">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="08376-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08376-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08376-176">CommonParameters</span></span>
<span data-ttu-id="08376-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08376-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08376-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08376-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08376-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08376-179">INPUTS</span></span>

### <span data-ttu-id="08376-180">System.String</span><span class="sxs-lookup"><span data-stu-id="08376-180">System.String</span></span>

### <span data-ttu-id="08376-181">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08376-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08376-182">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08376-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="08376-183">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08376-183">OUTPUTS</span></span>

### <span data-ttu-id="08376-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="08376-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="08376-185">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="08376-185">NOTES</span></span>

## <span data-ttu-id="08376-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08376-186">RELATED LINKS</span></span>

[<span data-ttu-id="08376-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08376-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="08376-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08376-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="08376-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08376-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="08376-190">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="08376-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


