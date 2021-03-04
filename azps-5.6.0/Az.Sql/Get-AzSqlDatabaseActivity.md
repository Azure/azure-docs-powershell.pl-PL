---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 12b44d2045574b1d787dd0b2bdb70ec44b616ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993238"
---
# <span data-ttu-id="3984f-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="3984f-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="3984f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3984f-102">SYNOPSIS</span></span>
<span data-ttu-id="3984f-103">Pobiera stan operacji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3984f-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="3984f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3984f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3984f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3984f-105">DESCRIPTION</span></span>
<span data-ttu-id="3984f-106">Polecenie **cmdlet Get-AzSqlDatabaseActivity** pobiera stan operacji bazy danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3984f-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="3984f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3984f-107">EXAMPLES</span></span>

### <span data-ttu-id="3984f-108">Przykład 1. Uzyskiwanie stanu dla wszystkich wystąpień bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3984f-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="3984f-109">To polecenie zwraca stan operacji wszystkich wystąpień bazy danych SQL w puli elastycznej o nazwie 10000000000000000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="3984f-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="3984f-110">Przykład 2. Uzyskiwanie stanu dla wszystkich operacji w bazie danych SQL</span><span class="sxs-lookup"><span data-stu-id="3984f-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="3984f-111">To polecenie zwraca stan wszystkich operacji bazy danych SQL w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="3984f-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="3984f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3984f-112">PARAMETERS</span></span>

### <span data-ttu-id="3984f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3984f-113">-DatabaseName</span></span>
<span data-ttu-id="3984f-114">Określa nazwę bazy danych, dla której to polecenie cmdlet ma stan.</span><span class="sxs-lookup"><span data-stu-id="3984f-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="3984f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3984f-115">-DefaultProfile</span></span>
<span data-ttu-id="3984f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3984f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3984f-117">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="3984f-117">-ElasticPoolName</span></span>
<span data-ttu-id="3984f-118">Określa nazwę elastycznej puli bazy danych, dla której to polecenie cmdlet ma stan.</span><span class="sxs-lookup"><span data-stu-id="3984f-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="3984f-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3984f-119">-OperationId</span></span>
<span data-ttu-id="3984f-120">Określa identyfikator operacji, która będzie owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3984f-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3984f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3984f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3984f-122">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="3984f-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3984f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3984f-123">-ServerName</span></span>
<span data-ttu-id="3984f-124">Określa nazwę pliku, Microsoft SQL Server hostuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="3984f-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="3984f-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3984f-125">-Confirm</span></span>
<span data-ttu-id="3984f-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3984f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3984f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3984f-127">-WhatIf</span></span>
<span data-ttu-id="3984f-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3984f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3984f-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3984f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3984f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3984f-130">CommonParameters</span></span>
<span data-ttu-id="3984f-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3984f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3984f-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3984f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3984f-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3984f-133">INPUTS</span></span>

### <span data-ttu-id="3984f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3984f-134">System.String</span></span>

### <span data-ttu-id="3984f-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3984f-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3984f-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3984f-136">OUTPUTS</span></span>

### <span data-ttu-id="3984f-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="3984f-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="3984f-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3984f-138">NOTES</span></span>

## <span data-ttu-id="3984f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3984f-139">RELATED LINKS</span></span>
