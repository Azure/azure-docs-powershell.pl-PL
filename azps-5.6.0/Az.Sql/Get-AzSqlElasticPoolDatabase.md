---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 4a9e128fb8c67c44329dd2b99da8ce4722835323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999530"
---
# <span data-ttu-id="d88d2-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="d88d2-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="d88d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d88d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d88d2-103">Elastyczna baza danych znajduje się w elastycznej puli i wartości ich właściwości.</span><span class="sxs-lookup"><span data-stu-id="d88d2-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="d88d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d88d2-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d88d2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d88d2-105">DESCRIPTION</span></span>
<span data-ttu-id="d88d2-106">Polecenie **cmdlet Get-AzSqlElasticPoolDatabase** pobiera elastyczne bazy danych w elastycznej puli i wartości ich właściwości.</span><span class="sxs-lookup"><span data-stu-id="d88d2-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="d88d2-107">Możesz określić nazwę elastycznej bazy danych w usłudze Azure SQL Database, aby wyświetlić wartości właściwości tylko dla tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d88d2-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="d88d2-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d88d2-108">EXAMPLES</span></span>

### <span data-ttu-id="d88d2-109">Przykład 1. Uzyskiwanie wszystkich baz danych w elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="d88d2-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d88d2-110">To polecenie pobiera wszystkie bazy danych w elastyczną pulę o nazwie Poszybkowane Bufor01.</span><span class="sxs-lookup"><span data-stu-id="d88d2-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="d88d2-111">Przykład 2. Uzyskiwanie wszystkich baz danych w elastycznej puli przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="d88d2-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="d88d2-112">To polecenie pobiera wszystkie bazy danych w elastycznej puli o nazwie Poszybowej01, która zaczyna się od "Bazy danych".</span><span class="sxs-lookup"><span data-stu-id="d88d2-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="d88d2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d88d2-113">PARAMETERS</span></span>

### <span data-ttu-id="d88d2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d88d2-114">-DatabaseName</span></span>
<span data-ttu-id="d88d2-115">Określa nazwę bazy danych SQL, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d88d2-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d88d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88d2-116">-DefaultProfile</span></span>
<span data-ttu-id="d88d2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d88d2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d88d2-118">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="d88d2-118">-ElasticPoolName</span></span>
<span data-ttu-id="d88d2-119">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="d88d2-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="d88d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="d88d2-121">Określa nazwę grupy zasobów, do której przypisano pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="d88d2-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="d88d2-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d88d2-122">-ServerName</span></span>
<span data-ttu-id="d88d2-123">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="d88d2-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="d88d2-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d88d2-124">-Confirm</span></span>
<span data-ttu-id="d88d2-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d88d2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d88d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d88d2-126">-WhatIf</span></span>
<span data-ttu-id="d88d2-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d88d2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88d2-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d88d2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d88d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88d2-129">CommonParameters</span></span>
<span data-ttu-id="d88d2-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d88d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88d2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d88d2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88d2-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d88d2-132">INPUTS</span></span>

### <span data-ttu-id="d88d2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d88d2-133">System.String</span></span>

## <span data-ttu-id="d88d2-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d88d2-134">OUTPUTS</span></span>

### <span data-ttu-id="d88d2-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d88d2-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d88d2-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d88d2-136">NOTES</span></span>

## <span data-ttu-id="d88d2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d88d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="d88d2-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d88d2-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="d88d2-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="d88d2-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="d88d2-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d88d2-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="d88d2-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d88d2-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="d88d2-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d88d2-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

