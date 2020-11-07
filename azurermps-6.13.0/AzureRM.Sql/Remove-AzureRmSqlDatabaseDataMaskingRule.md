---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 15341932acd8764deb9a1b8b0417b25a5a5cacd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718264"
---
# <span data-ttu-id="92e62-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92e62-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="92e62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92e62-102">SYNOPSIS</span></span>
<span data-ttu-id="92e62-103">Usuwa regułę maskowania danych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="92e62-103">Removes a data masking rule from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92e62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92e62-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92e62-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92e62-105">DESCRIPTION</span></span>
<span data-ttu-id="92e62-106">Polecenie cmdlet **Remove-AzureRmSqlDatabaseDataMaskingRule** usuwa określoną regułę maskowania danych z bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="92e62-106">The **Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="92e62-107">Regułę maskowania danych można usunąć, korzystając z parametrów *ResourceGroupName* , *nazwa_serwera* , *DatabaseName* i *RuleID* w celu zidentyfikowania reguły, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="92e62-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="92e62-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="92e62-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="92e62-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92e62-109">EXAMPLES</span></span>

### <span data-ttu-id="92e62-110">Przykład 1: Usuwanie reguły maskowania danych bazy danych</span><span class="sxs-lookup"><span data-stu-id="92e62-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="92e62-111">To polecenie usuwa nazwę reguły Rule01 zdefiniowaną dla Database01 bazy danych.</span><span class="sxs-lookup"><span data-stu-id="92e62-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="92e62-112">Baza danych znajduje się w witrynie Server01 i jest przypisana do ResourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92e62-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="92e62-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92e62-113">PARAMETERS</span></span>

### <span data-ttu-id="92e62-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="92e62-114">-ColumnName</span></span>
<span data-ttu-id="92e62-115">Określa nazwę kolumny docelowej reguły maskowania.</span><span class="sxs-lookup"><span data-stu-id="92e62-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="92e62-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="92e62-116">-DatabaseName</span></span>
<span data-ttu-id="92e62-117">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="92e62-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="92e62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e62-118">-DefaultProfile</span></span>
<span data-ttu-id="92e62-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="92e62-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e62-120">-Force</span><span class="sxs-lookup"><span data-stu-id="92e62-120">-Force</span></span>
<span data-ttu-id="92e62-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92e62-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92e62-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92e62-122">-PassThru</span></span>
<span data-ttu-id="92e62-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="92e62-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92e62-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="92e62-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="92e62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e62-125">-ResourceGroupName</span></span>
<span data-ttu-id="92e62-126">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="92e62-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="92e62-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="92e62-127">-SchemaName</span></span>
<span data-ttu-id="92e62-128">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="92e62-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="92e62-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="92e62-129">-ServerName</span></span>
<span data-ttu-id="92e62-130">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="92e62-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="92e62-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="92e62-131">-TableName</span></span>
<span data-ttu-id="92e62-132">Określa nazwę tabeli SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="92e62-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="92e62-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92e62-133">-Confirm</span></span>
<span data-ttu-id="92e62-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e62-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e62-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e62-135">-WhatIf</span></span>
<span data-ttu-id="92e62-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e62-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e62-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92e62-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e62-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e62-138">CommonParameters</span></span>
<span data-ttu-id="92e62-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e62-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e62-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e62-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e62-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92e62-141">INPUTS</span></span>

### <span data-ttu-id="92e62-142">System. String</span><span class="sxs-lookup"><span data-stu-id="92e62-142">System.String</span></span>

## <span data-ttu-id="92e62-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92e62-143">OUTPUTS</span></span>

### <span data-ttu-id="92e62-144">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="92e62-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="92e62-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92e62-145">NOTES</span></span>

## <span data-ttu-id="92e62-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92e62-146">RELATED LINKS</span></span>

[<span data-ttu-id="92e62-147">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92e62-147">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="92e62-148">Nowe — AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92e62-148">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="92e62-149">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92e62-149">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="92e62-150">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="92e62-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


