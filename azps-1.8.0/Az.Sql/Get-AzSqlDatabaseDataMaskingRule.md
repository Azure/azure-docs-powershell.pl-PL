---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 5c43820c57531ca5a844e1ab429c26d85fecceee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708003"
---
# <span data-ttu-id="3b426-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b426-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="3b426-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b426-102">SYNOPSIS</span></span>
<span data-ttu-id="3b426-103">Pobiera reguły maskowania danych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3b426-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="3b426-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b426-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b426-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b426-105">DESCRIPTION</span></span>
<span data-ttu-id="3b426-106">Polecenie cmdlet **Get-AzSqlDatabaseDataMaskingRule** pobiera określoną regułę maskowania danych lub wszystkie reguły maskowania danych dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3b426-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="3b426-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych, a parametr *RuleID* określający regułę zwracaną przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="3b426-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="3b426-108">Jeśli nie podasz *RuleID* , zostaną zwrócone wszystkie reguły maskowania danych dla tej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3b426-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="3b426-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="3b426-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3b426-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b426-110">EXAMPLES</span></span>

### <span data-ttu-id="3b426-111">Przykład 1: pobieranie wszystkich reguł maskowania danych z bazy danych</span><span class="sxs-lookup"><span data-stu-id="3b426-111">Example 1: Get all data masking rules from a database</span></span>
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

### <span data-ttu-id="3b426-112">Przykład 2: Pobierz regułę maskowania danych zdefiniowaną w schemacie "dbo", tabela "Tabela1" i Column "Kolumna1".</span><span class="sxs-lookup"><span data-stu-id="3b426-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
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

## <span data-ttu-id="3b426-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b426-113">PARAMETERS</span></span>

### <span data-ttu-id="3b426-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3b426-114">-ColumnName</span></span>
<span data-ttu-id="3b426-115">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="3b426-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="3b426-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b426-116">-DatabaseName</span></span>
<span data-ttu-id="3b426-117">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3b426-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3b426-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b426-118">-DefaultProfile</span></span>
<span data-ttu-id="3b426-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3b426-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b426-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b426-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b426-121">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="3b426-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3b426-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3b426-122">-SchemaName</span></span>
<span data-ttu-id="3b426-123">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="3b426-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="3b426-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3b426-124">-ServerName</span></span>
<span data-ttu-id="3b426-125">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="3b426-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3b426-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="3b426-126">-TableName</span></span>
<span data-ttu-id="3b426-127">Określa nazwę tabeli SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3b426-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="3b426-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b426-128">-Confirm</span></span>
<span data-ttu-id="3b426-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b426-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b426-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b426-130">-WhatIf</span></span>
<span data-ttu-id="3b426-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b426-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b426-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b426-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b426-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b426-133">CommonParameters</span></span>
<span data-ttu-id="3b426-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b426-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b426-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b426-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b426-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b426-136">INPUTS</span></span>

### <span data-ttu-id="3b426-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3b426-137">System.String</span></span>

## <span data-ttu-id="3b426-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b426-138">OUTPUTS</span></span>

### <span data-ttu-id="3b426-139">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="3b426-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="3b426-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b426-140">NOTES</span></span>

## <span data-ttu-id="3b426-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b426-141">RELATED LINKS</span></span>

[<span data-ttu-id="3b426-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="3b426-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="3b426-143">Nowe — AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b426-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3b426-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b426-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3b426-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="3b426-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="3b426-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b426-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

