---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 4dbfea5106b46bd8d0f1efc1926841dd964b0299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983642"
---
# <span data-ttu-id="6d2ce-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="6d2ce-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="6d2ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2ce-103">Pobiera przepływność bazy danych GremlinDb firmy A0.</span><span class="sxs-lookup"><span data-stu-id="6d2ce-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="6d2ce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6d2ce-104">SYNTAX</span></span>

### <span data-ttu-id="6d2ce-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6d2ce-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d2ce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d2ce-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d2ce-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6d2ce-107">DESCRIPTION</span></span>
<span data-ttu-id="6d2ce-108">Polecenie **cmdlet Get-AzCosmosDBGremlinDatabaseThroughput** pobiera przepływność bazy danych GremlinDb.</span><span class="sxs-lookup"><span data-stu-id="6d2ce-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="6d2ce-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6d2ce-109">EXAMPLES</span></span>

### <span data-ttu-id="6d2ce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d2ce-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="6d2ce-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d2ce-111">PARAMETERS</span></span>

### <span data-ttu-id="6d2ce-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d2ce-112">-AccountName</span></span>
<span data-ttu-id="6d2ce-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="6d2ce-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6d2ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2ce-114">-DefaultProfile</span></span>
<span data-ttu-id="6d2ce-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d2ce-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d2ce-116">-InputObject</span></span>
<span data-ttu-id="6d2ce-117">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="6d2ce-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d2ce-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6d2ce-118">-Name</span></span>
<span data-ttu-id="6d2ce-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6d2ce-119">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d2ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d2ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="6d2ce-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d2ce-121">Name of resource group.</span></span>

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

### <span data-ttu-id="6d2ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2ce-122">CommonParameters</span></span>
<span data-ttu-id="6d2ce-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d2ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2ce-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d2ce-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2ce-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d2ce-125">INPUTS</span></span>

### <span data-ttu-id="6d2ce-126">Brak</span><span class="sxs-lookup"><span data-stu-id="6d2ce-126">None</span></span>

## <span data-ttu-id="6d2ce-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d2ce-127">OUTPUTS</span></span>

### <span data-ttu-id="6d2ce-128">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6d2ce-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6d2ce-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6d2ce-129">NOTES</span></span>

## <span data-ttu-id="6d2ce-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d2ce-130">RELATED LINKS</span></span>
