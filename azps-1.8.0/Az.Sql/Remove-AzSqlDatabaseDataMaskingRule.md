---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 016b77c7e58a3c95405d6364118a9d0ec7815660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707829"
---
# <span data-ttu-id="2a3b1-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2a3b1-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="2a3b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3b1-103">Usuwa regułę maskowania danych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="2a3b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a3b1-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a3b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a3b1-105">DESCRIPTION</span></span>
<span data-ttu-id="2a3b1-106">Polecenie cmdlet **Remove-AzSqlDatabaseDataMaskingRule** usuwa określoną regułę maskowania danych z bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="2a3b1-107">Regułę maskowania danych można usunąć, korzystając z parametrów *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="2a3b1-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2a3b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a3b1-109">EXAMPLES</span></span>

### <span data-ttu-id="2a3b1-110">Przykład 1: Usuwanie reguły maskowania danych bazy danych</span><span class="sxs-lookup"><span data-stu-id="2a3b1-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="2a3b1-111">To polecenie usuwa nazwę reguły Rule01 zdefiniowaną dla Database01 bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="2a3b1-112">Baza danych znajduje się w witrynie Server01 i jest przypisana do ResourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="2a3b1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a3b1-113">PARAMETERS</span></span>

### <span data-ttu-id="2a3b1-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2a3b1-114">-ColumnName</span></span>
<span data-ttu-id="2a3b1-115">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="2a3b1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a3b1-116">-DatabaseName</span></span>
<span data-ttu-id="2a3b1-117">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2a3b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3b1-118">-DefaultProfile</span></span>
<span data-ttu-id="2a3b1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2a3b1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a3b1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2a3b1-120">-Force</span></span>
<span data-ttu-id="2a3b1-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a3b1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a3b1-122">-PassThru</span></span>
<span data-ttu-id="2a3b1-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a3b1-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a3b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a3b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a3b1-126">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2a3b1-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2a3b1-127">-SchemaName</span></span>
<span data-ttu-id="2a3b1-128">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="2a3b1-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2a3b1-129">-ServerName</span></span>
<span data-ttu-id="2a3b1-130">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2a3b1-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="2a3b1-131">-TableName</span></span>
<span data-ttu-id="2a3b1-132">Określa nazwę tabeli SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="2a3b1-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a3b1-133">-Confirm</span></span>
<span data-ttu-id="2a3b1-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a3b1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a3b1-135">-WhatIf</span></span>
<span data-ttu-id="2a3b1-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a3b1-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a3b1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3b1-138">CommonParameters</span></span>
<span data-ttu-id="2a3b1-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a3b1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3b1-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a3b1-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3b1-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a3b1-141">INPUTS</span></span>

### <span data-ttu-id="2a3b1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2a3b1-142">System.String</span></span>

## <span data-ttu-id="2a3b1-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a3b1-143">OUTPUTS</span></span>

### <span data-ttu-id="2a3b1-144">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="2a3b1-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="2a3b1-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a3b1-145">NOTES</span></span>

## <span data-ttu-id="2a3b1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a3b1-146">RELATED LINKS</span></span>

[<span data-ttu-id="2a3b1-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2a3b1-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2a3b1-148">Nowe — AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2a3b1-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2a3b1-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2a3b1-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2a3b1-150">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2a3b1-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


