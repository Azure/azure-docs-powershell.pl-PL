---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053091"
---
# <span data-ttu-id="84bd3-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="84bd3-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="84bd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="84bd3-103">Pobiera bazę danych Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="84bd3-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="84bd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84bd3-104">SYNTAX</span></span>

### <span data-ttu-id="84bd3-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84bd3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84bd3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84bd3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84bd3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="84bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="84bd3-108">Polecenie cmdlet **Get-AzCosmosDBGremlinDatabase** pobiera bazę danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="84bd3-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="84bd3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="84bd3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84bd3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="84bd3-111">Obiekt zasobu zawiera _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="84bd3-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="84bd3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84bd3-112">PARAMETERS</span></span>

### <span data-ttu-id="84bd3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="84bd3-113">-AccountName</span></span>
<span data-ttu-id="84bd3-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="84bd3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="84bd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bd3-115">-DefaultProfile</span></span>
<span data-ttu-id="84bd3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84bd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84bd3-117">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="84bd3-117">-Detailed</span></span>
<span data-ttu-id="84bd3-118">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci bazę danych z odpowiednią wartością przepustowości.</span><span class="sxs-lookup"><span data-stu-id="84bd3-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84bd3-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84bd3-119">-InputObject</span></span>
<span data-ttu-id="84bd3-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="84bd3-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84bd3-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84bd3-121">-Name</span></span>
<span data-ttu-id="84bd3-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="84bd3-122">Database name.</span></span>

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

### <span data-ttu-id="84bd3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bd3-123">-ResourceGroupName</span></span>
<span data-ttu-id="84bd3-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84bd3-124">Name of resource group.</span></span>

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

### <span data-ttu-id="84bd3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bd3-125">CommonParameters</span></span>
<span data-ttu-id="84bd3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84bd3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bd3-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84bd3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bd3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84bd3-128">INPUTS</span></span>

### <span data-ttu-id="84bd3-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="84bd3-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="84bd3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84bd3-130">OUTPUTS</span></span>

### <span data-ttu-id="84bd3-131">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="84bd3-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="84bd3-132">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="84bd3-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="84bd3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84bd3-133">NOTES</span></span>

## <span data-ttu-id="84bd3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84bd3-134">RELATED LINKS</span></span>
