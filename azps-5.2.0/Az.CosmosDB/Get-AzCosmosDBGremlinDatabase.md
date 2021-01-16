---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343930"
---
# <span data-ttu-id="b83aa-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="b83aa-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="b83aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b83aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b83aa-103">Pobiera bazę danych Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b83aa-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b83aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b83aa-104">SYNTAX</span></span>

### <span data-ttu-id="b83aa-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b83aa-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b83aa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b83aa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b83aa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b83aa-107">DESCRIPTION</span></span>
<span data-ttu-id="b83aa-108">Polecenie cmdlet **Get-AzCosmosDBGremlinDatabase** pobiera bazę danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b83aa-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b83aa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b83aa-109">EXAMPLES</span></span>

### <span data-ttu-id="b83aa-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b83aa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="b83aa-111">Obiekt zasobu zawiera _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="b83aa-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="b83aa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b83aa-112">PARAMETERS</span></span>

### <span data-ttu-id="b83aa-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b83aa-113">-AccountName</span></span>
<span data-ttu-id="b83aa-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b83aa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b83aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83aa-115">-DefaultProfile</span></span>
<span data-ttu-id="b83aa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b83aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b83aa-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b83aa-117">-Name</span></span>
<span data-ttu-id="b83aa-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b83aa-118">Database name.</span></span>

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

### <span data-ttu-id="b83aa-119">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b83aa-119">-ParentObject</span></span>
<span data-ttu-id="b83aa-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b83aa-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b83aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b83aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="b83aa-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b83aa-122">Name of resource group.</span></span>

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

### <span data-ttu-id="b83aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83aa-123">CommonParameters</span></span>
<span data-ttu-id="b83aa-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b83aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83aa-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b83aa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83aa-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b83aa-126">INPUTS</span></span>

### <span data-ttu-id="b83aa-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b83aa-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b83aa-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b83aa-128">OUTPUTS</span></span>

### <span data-ttu-id="b83aa-129">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b83aa-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="b83aa-130">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b83aa-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b83aa-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b83aa-131">NOTES</span></span>

## <span data-ttu-id="b83aa-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b83aa-132">RELATED LINKS</span></span>
