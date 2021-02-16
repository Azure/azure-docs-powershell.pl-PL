---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199011"
---
# <span data-ttu-id="c2fab-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c2fab-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="c2fab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fab-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fab-103">Pobiera bazę danych SqlsDB.</span><span class="sxs-lookup"><span data-stu-id="c2fab-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="c2fab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2fab-104">SYNTAX</span></span>

### <span data-ttu-id="c2fab-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c2fab-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2fab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2fab-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2fab-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2fab-107">DESCRIPTION</span></span>
<span data-ttu-id="c2fab-108">Polecenie cmdlet **Get-AzCosmosDBSqlDatabase** pobiera listę wszystkich istniejących baz danych Sql dla organizacji ResourceGroupName, AccountName i otrzymuje pojedynczą bazę danych Sql dla nazwa_grupy zasobów, accountname, nazwa_bazy danych i nazwę ContainerName.</span><span class="sxs-lookup"><span data-stu-id="c2fab-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="c2fab-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2fab-109">EXAMPLES</span></span>

### <span data-ttu-id="c2fab-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2fab-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="c2fab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2fab-111">PARAMETERS</span></span>

### <span data-ttu-id="c2fab-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2fab-112">-AccountName</span></span>
<span data-ttu-id="c2fab-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="c2fab-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2fab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fab-114">-DefaultProfile</span></span>
<span data-ttu-id="c2fab-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2fab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fab-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2fab-116">-Name</span></span>
<span data-ttu-id="c2fab-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c2fab-117">Database name.</span></span>

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

### <span data-ttu-id="c2fab-118">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2fab-118">-ParentObject</span></span>
<span data-ttu-id="c2fab-119">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="c2fab-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2fab-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2fab-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2fab-121">Name of resource group.</span></span>

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

### <span data-ttu-id="c2fab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fab-122">CommonParameters</span></span>
<span data-ttu-id="c2fab-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fab-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2fab-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fab-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2fab-125">INPUTS</span></span>

### <span data-ttu-id="c2fab-126">Brak</span><span class="sxs-lookup"><span data-stu-id="c2fab-126">None</span></span>

## <span data-ttu-id="c2fab-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fab-127">OUTPUTS</span></span>

### <span data-ttu-id="c2fab-128">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2fab-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c2fab-129">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c2fab-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c2fab-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2fab-130">NOTES</span></span>

## <span data-ttu-id="c2fab-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2fab-131">RELATED LINKS</span></span>
