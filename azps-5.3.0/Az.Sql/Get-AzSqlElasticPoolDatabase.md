---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374801"
---
# <span data-ttu-id="11afd-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="11afd-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="11afd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11afd-102">SYNOPSIS</span></span>
<span data-ttu-id="11afd-103">Pobiera elastyczną bazę danych w puli elastycznej i jej wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="11afd-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="11afd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11afd-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11afd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11afd-105">DESCRIPTION</span></span>
<span data-ttu-id="11afd-106">Polecenie cmdlet **Get-AzSqlElasticPoolDatabase** pobiera elastyczną bazę danych w puli elastycznej oraz wartości ich właściwości.</span><span class="sxs-lookup"><span data-stu-id="11afd-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="11afd-107">W usłudze Azure SQL Database można określić nazwę Elastic Database, aby wyświetlić wartości właściwości tylko tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="11afd-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="11afd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11afd-108">EXAMPLES</span></span>

### <span data-ttu-id="11afd-109">Przykład 1: pobieranie wszystkich baz danych w elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="11afd-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="11afd-110">To polecenie pobiera wszystkie bazy danych z puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="11afd-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="11afd-111">Przykład 2: pobieranie wszystkich baz danych w puli elastycznej przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="11afd-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="11afd-112">To polecenie pobiera wszystkie bazy danych z puli elastycznej o nazwie ElasticPool01, która rozpoczyna się od "bazy danych".</span><span class="sxs-lookup"><span data-stu-id="11afd-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="11afd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11afd-113">PARAMETERS</span></span>

### <span data-ttu-id="11afd-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11afd-114">-DatabaseName</span></span>
<span data-ttu-id="11afd-115">Określa nazwę bazy danych SQL, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11afd-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="11afd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11afd-116">-DefaultProfile</span></span>
<span data-ttu-id="11afd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="11afd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11afd-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="11afd-118">-ElasticPoolName</span></span>
<span data-ttu-id="11afd-119">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="11afd-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="11afd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11afd-120">-ResourceGroupName</span></span>
<span data-ttu-id="11afd-121">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="11afd-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="11afd-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="11afd-122">-ServerName</span></span>
<span data-ttu-id="11afd-123">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="11afd-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="11afd-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11afd-124">-Confirm</span></span>
<span data-ttu-id="11afd-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11afd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11afd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11afd-126">-WhatIf</span></span>
<span data-ttu-id="11afd-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11afd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11afd-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11afd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11afd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11afd-129">CommonParameters</span></span>
<span data-ttu-id="11afd-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11afd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11afd-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11afd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11afd-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11afd-132">INPUTS</span></span>

### <span data-ttu-id="11afd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="11afd-133">System.String</span></span>

## <span data-ttu-id="11afd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11afd-134">OUTPUTS</span></span>

### <span data-ttu-id="11afd-135">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="11afd-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="11afd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11afd-136">NOTES</span></span>

## <span data-ttu-id="11afd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11afd-137">RELATED LINKS</span></span>

[<span data-ttu-id="11afd-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11afd-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="11afd-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="11afd-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="11afd-140">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11afd-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="11afd-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11afd-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="11afd-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11afd-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

