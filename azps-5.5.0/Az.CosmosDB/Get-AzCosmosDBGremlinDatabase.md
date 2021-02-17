---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199042"
---
# <span data-ttu-id="14733-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="14733-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="14733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14733-102">SYNOPSIS</span></span>
<span data-ttu-id="14733-103">Pobiera bazę danych GrysDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="14733-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="14733-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14733-104">SYNTAX</span></span>

### <span data-ttu-id="14733-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="14733-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14733-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14733-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14733-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="14733-107">DESCRIPTION</span></span>
<span data-ttu-id="14733-108">Polecenie **cmdlet Get-AzCosmosDBGremlinDatabase** pobiera bazę danych GrysDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="14733-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="14733-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14733-109">EXAMPLES</span></span>

### <span data-ttu-id="14733-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14733-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="14733-111">Obiekt zasobu _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="14733-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="14733-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14733-112">PARAMETERS</span></span>

### <span data-ttu-id="14733-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="14733-113">-AccountName</span></span>
<span data-ttu-id="14733-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="14733-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="14733-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14733-115">-DefaultProfile</span></span>
<span data-ttu-id="14733-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14733-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14733-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14733-117">-Name</span></span>
<span data-ttu-id="14733-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="14733-118">Database name.</span></span>

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

### <span data-ttu-id="14733-119">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="14733-119">-ParentObject</span></span>
<span data-ttu-id="14733-120">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="14733-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="14733-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14733-121">-ResourceGroupName</span></span>
<span data-ttu-id="14733-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14733-122">Name of resource group.</span></span>

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

### <span data-ttu-id="14733-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14733-123">CommonParameters</span></span>
<span data-ttu-id="14733-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14733-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14733-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14733-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14733-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14733-126">INPUTS</span></span>

### <span data-ttu-id="14733-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="14733-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="14733-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14733-128">OUTPUTS</span></span>

### <span data-ttu-id="14733-129">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="14733-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="14733-130">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="14733-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="14733-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14733-131">NOTES</span></span>

## <span data-ttu-id="14733-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14733-132">RELATED LINKS</span></span>
