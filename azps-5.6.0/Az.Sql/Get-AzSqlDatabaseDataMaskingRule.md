---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: ab6bdaac71e13cfe62c054c5dbc01686760505ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967473"
---
# <span data-ttu-id="5a5fc-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5a5fc-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="5a5fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5fc-103">Pobiera reguły maskowania danych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="5a5fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a5fc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a5fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="5a5fc-106">Polecenie **cmdlet Get-AzSqlDatabaseDataMaskingRule** pobiera określoną regułę maskowania danych lub wszystkie reguły maskowania danych dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="5a5fc-107">Aby użyć polecenia cmdlet, określ bazę danych za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName,* a parametr *RuleId* określ regułę zwracaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="5a5fc-108">Jeśli nie powrócisz do *reguły RuleId,* zostaną zwrócone wszystkie reguły maskowania danych dla tej bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-108">If you do not provide *RuleId*, all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="5a5fc-109">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5a5fc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a5fc-110">EXAMPLES</span></span>

### <span data-ttu-id="5a5fc-111">Przykład 1. Uzyskiwanie wszystkich reguł maskowania danych z bazy danych</span><span class="sxs-lookup"><span data-stu-id="5a5fc-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="5a5fc-112">Przykład 2. Pobierz regułę maskowania danych zdefiniowaną w schemacie "dbo", tabeli "tabela1" i kolumnie "kolumna1".</span><span class="sxs-lookup"><span data-stu-id="5a5fc-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="5a5fc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a5fc-113">PARAMETERS</span></span>

### <span data-ttu-id="5a5fc-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5a5fc-114">-ColumnName</span></span>
<span data-ttu-id="5a5fc-115">Określa nazwę kolumny docelowej przez regułę maskowania.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="5a5fc-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a5fc-116">-DatabaseName</span></span>
<span data-ttu-id="5a5fc-117">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5a5fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5fc-118">-DefaultProfile</span></span>
<span data-ttu-id="5a5fc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5a5fc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a5fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a5fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a5fc-121">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5a5fc-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5a5fc-122">-SchemaName</span></span>
<span data-ttu-id="5a5fc-123">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="5a5fc-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a5fc-124">-ServerName</span></span>
<span data-ttu-id="5a5fc-125">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5a5fc-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="5a5fc-126">-TableName</span></span>
<span data-ttu-id="5a5fc-127">Określa nazwę tabeli Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="5a5fc-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a5fc-128">-Confirm</span></span>
<span data-ttu-id="5a5fc-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a5fc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a5fc-130">-WhatIf</span></span>
<span data-ttu-id="5a5fc-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a5fc-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a5fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5fc-133">CommonParameters</span></span>
<span data-ttu-id="5a5fc-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a5fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5fc-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a5fc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5fc-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a5fc-136">INPUTS</span></span>

### <span data-ttu-id="5a5fc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5a5fc-137">System.String</span></span>

## <span data-ttu-id="5a5fc-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a5fc-138">OUTPUTS</span></span>

### <span data-ttu-id="5a5fc-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="5a5fc-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="5a5fc-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a5fc-140">NOTES</span></span>

## <span data-ttu-id="5a5fc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a5fc-141">RELATED LINKS</span></span>

[<span data-ttu-id="5a5fc-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="5a5fc-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="5a5fc-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5a5fc-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5a5fc-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5a5fc-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5a5fc-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="5a5fc-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="5a5fc-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5a5fc-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


