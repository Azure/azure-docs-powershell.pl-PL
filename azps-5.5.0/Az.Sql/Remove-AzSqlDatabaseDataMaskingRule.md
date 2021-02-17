---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196059"
---
# <span data-ttu-id="05ef3-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="05ef3-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="05ef3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="05ef3-103">Usuwa regułę maskowania danych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="05ef3-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="05ef3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05ef3-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ef3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="05ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="05ef3-106">Polecenie **cmdlet Remove-AzSqlDatabaseDataMaskingRule** usuwa określoną regułę maskowania danych z bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="05ef3-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="05ef3-107">Regułę maskowania danych można usunąć, używając parametrów *ResourceGroupName,* *ServerName,* *DatabaseName* i *RuleId* w celu zidentyfikowania reguły usunięcia tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ef3-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="05ef3-108">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="05ef3-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="05ef3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05ef3-109">EXAMPLES</span></span>

### <span data-ttu-id="05ef3-110">Przykład 1. Usuwanie reguły maskowania danych bazy danych</span><span class="sxs-lookup"><span data-stu-id="05ef3-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="05ef3-111">To polecenie usuwa nazwę reguły Rule01 zdefiniowaną dla bazy danych Database01.</span><span class="sxs-lookup"><span data-stu-id="05ef3-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="05ef3-112">Baza danych znajduje się na serwerze Server01 i jest przypisana do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="05ef3-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="05ef3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05ef3-113">PARAMETERS</span></span>

### <span data-ttu-id="05ef3-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="05ef3-114">-ColumnName</span></span>
<span data-ttu-id="05ef3-115">Określa nazwę kolumny docelowej przez regułę maskowania.</span><span class="sxs-lookup"><span data-stu-id="05ef3-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="05ef3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05ef3-116">-DatabaseName</span></span>
<span data-ttu-id="05ef3-117">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="05ef3-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="05ef3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ef3-118">-DefaultProfile</span></span>
<span data-ttu-id="05ef3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="05ef3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05ef3-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="05ef3-120">-Force</span></span>
<span data-ttu-id="05ef3-121">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="05ef3-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05ef3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05ef3-122">-PassThru</span></span>
<span data-ttu-id="05ef3-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="05ef3-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="05ef3-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="05ef3-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="05ef3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ef3-125">-ResourceGroupName</span></span>
<span data-ttu-id="05ef3-126">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="05ef3-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="05ef3-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="05ef3-127">-SchemaName</span></span>
<span data-ttu-id="05ef3-128">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="05ef3-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="05ef3-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05ef3-129">-ServerName</span></span>
<span data-ttu-id="05ef3-130">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="05ef3-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="05ef3-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="05ef3-131">-TableName</span></span>
<span data-ttu-id="05ef3-132">Określa nazwę tabeli Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="05ef3-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="05ef3-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05ef3-133">-Confirm</span></span>
<span data-ttu-id="05ef3-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="05ef3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ef3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ef3-135">-WhatIf</span></span>
<span data-ttu-id="05ef3-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ef3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ef3-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="05ef3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ef3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ef3-138">CommonParameters</span></span>
<span data-ttu-id="05ef3-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ef3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ef3-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05ef3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ef3-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05ef3-141">INPUTS</span></span>

### <span data-ttu-id="05ef3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="05ef3-142">System.String</span></span>

## <span data-ttu-id="05ef3-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05ef3-143">OUTPUTS</span></span>

### <span data-ttu-id="05ef3-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="05ef3-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="05ef3-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05ef3-145">NOTES</span></span>

## <span data-ttu-id="05ef3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05ef3-146">RELATED LINKS</span></span>

[<span data-ttu-id="05ef3-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="05ef3-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="05ef3-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="05ef3-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="05ef3-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="05ef3-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="05ef3-150">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="05ef3-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


