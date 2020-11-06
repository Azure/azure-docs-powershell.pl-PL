---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 0c04697f36558c7eb4c296e2837595541381a3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524858"
---
# <span data-ttu-id="75381-101">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75381-101">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="75381-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75381-102">SYNOPSIS</span></span>
<span data-ttu-id="75381-103">Pobiera reguły maskowania danych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="75381-103">Gets the data masking rules from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75381-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75381-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75381-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75381-105">DESCRIPTION</span></span>
<span data-ttu-id="75381-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseDataMaskingRule** pobiera określoną regułę maskowania danych lub wszystkie reguły maskowania danych dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="75381-106">The **Get-AzureRmSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="75381-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych, a parametr *RuleID* określający regułę zwracaną przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="75381-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="75381-108">Jeśli nie podasz *RuleID* , zostaną zwrócone wszystkie reguły maskowania danych dla tej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="75381-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>

<span data-ttu-id="75381-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="75381-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="75381-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75381-110">EXAMPLES</span></span>

### <span data-ttu-id="75381-111">Przykład 1: pobieranie wszystkich reguł maskowania danych z bazy danych</span><span class="sxs-lookup"><span data-stu-id="75381-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

### <span data-ttu-id="75381-112">Przykład 2: Pobierz regułę maskowania danych zdefiniowaną w schemacie "dbo", tabela "Tabela1" i Column "Kolumna1".</span><span class="sxs-lookup"><span data-stu-id="75381-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
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

## <span data-ttu-id="75381-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75381-113">PARAMETERS</span></span>

### <span data-ttu-id="75381-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="75381-114">-ColumnName</span></span>
<span data-ttu-id="75381-115">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="75381-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="75381-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75381-116">-DatabaseName</span></span>
<span data-ttu-id="75381-117">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="75381-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="75381-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75381-118">-DefaultProfile</span></span>
<span data-ttu-id="75381-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75381-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75381-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75381-120">-ResourceGroupName</span></span>
<span data-ttu-id="75381-121">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="75381-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="75381-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="75381-122">-SchemaName</span></span>
<span data-ttu-id="75381-123">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="75381-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="75381-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="75381-124">-ServerName</span></span>
<span data-ttu-id="75381-125">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="75381-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="75381-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="75381-126">-TableName</span></span>
<span data-ttu-id="75381-127">Określa nazwę tabeli SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="75381-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="75381-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75381-128">-Confirm</span></span>
<span data-ttu-id="75381-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75381-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75381-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75381-130">-WhatIf</span></span>
<span data-ttu-id="75381-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75381-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75381-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75381-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75381-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75381-133">CommonParameters</span></span>
<span data-ttu-id="75381-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75381-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75381-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75381-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75381-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75381-136">INPUTS</span></span>

###  
<span data-ttu-id="75381-137">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="75381-137">None.</span></span>

## <span data-ttu-id="75381-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75381-138">OUTPUTS</span></span>

### <span data-ttu-id="75381-139">Microsoft. Azure. Commands. SQL. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="75381-139">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="75381-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75381-140">NOTES</span></span>

## <span data-ttu-id="75381-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75381-141">RELATED LINKS</span></span>

[<span data-ttu-id="75381-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="75381-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="75381-143">Nowe — AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75381-143">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="75381-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75381-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="75381-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="75381-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="75381-146">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75381-146">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


