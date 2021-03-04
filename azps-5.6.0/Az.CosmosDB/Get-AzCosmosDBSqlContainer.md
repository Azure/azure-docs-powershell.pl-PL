---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 5c7c26faa6171babd60f9d5fb406d3b3c08ef81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952778"
---
# <span data-ttu-id="412ad-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="412ad-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="412ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="412ad-102">SYNOPSIS</span></span>
<span data-ttu-id="412ad-103">Pobiera kontener sql DossDB.</span><span class="sxs-lookup"><span data-stu-id="412ad-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="412ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="412ad-104">SYNTAX</span></span>

### <span data-ttu-id="412ad-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="412ad-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="412ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="412ad-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="412ad-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="412ad-107">DESCRIPTION</span></span>
<span data-ttu-id="412ad-108">Polecenie cmdlet **Get-AzCosmosDBSqlContainer** pobiera listę wszystkich istniejących kontenerów sql Dla organizacji ResourceGroupName, AccountName i DatabaseName oraz otrzymuje jeden kontener sql dla nazwa_grupy zasobów, nazwa_konta i nazwa_bazy danych.</span><span class="sxs-lookup"><span data-stu-id="412ad-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="412ad-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="412ad-109">EXAMPLES</span></span>

### <span data-ttu-id="412ad-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="412ad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="412ad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="412ad-111">PARAMETERS</span></span>

### <span data-ttu-id="412ad-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="412ad-112">-AccountName</span></span>
<span data-ttu-id="412ad-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="412ad-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ad-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="412ad-114">-DatabaseName</span></span>
<span data-ttu-id="412ad-115">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="412ad-115">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412ad-116">-DefaultProfile</span></span>
<span data-ttu-id="412ad-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="412ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ad-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="412ad-118">-Name</span></span>
<span data-ttu-id="412ad-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="412ad-119">Container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ad-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="412ad-120">-ParentObject</span></span>
<span data-ttu-id="412ad-121">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="412ad-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="412ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="412ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="412ad-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="412ad-123">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412ad-124">CommonParameters</span></span>
<span data-ttu-id="412ad-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412ad-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="412ad-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412ad-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="412ad-127">INPUTS</span></span>

### <span data-ttu-id="412ad-128">Brak</span><span class="sxs-lookup"><span data-stu-id="412ad-128">None</span></span>

## <span data-ttu-id="412ad-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="412ad-129">OUTPUTS</span></span>

### <span data-ttu-id="412ad-130">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="412ad-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="412ad-131">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="412ad-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="412ad-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="412ad-132">NOTES</span></span>

## <span data-ttu-id="412ad-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="412ad-133">RELATED LINKS</span></span>
