---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221356"
---
# <span data-ttu-id="3adaa-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="3adaa-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="3adaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3adaa-102">SYNOPSIS</span></span>
<span data-ttu-id="3adaa-103">Pobiera tabelę CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3adaa-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="3adaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3adaa-104">SYNTAX</span></span>

### <span data-ttu-id="3adaa-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3adaa-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3adaa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3adaa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3adaa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3adaa-107">DESCRIPTION</span></span>
<span data-ttu-id="3adaa-108">Polecenie cmdlet **Get-AzCosmosDBTable** pobiera istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="3adaa-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="3adaa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3adaa-109">EXAMPLES</span></span>

### <span data-ttu-id="3adaa-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3adaa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="3adaa-111">Obiekt zasobu zawiera właściwości _rid, _ts, ETag tabeli.</span><span class="sxs-lookup"><span data-stu-id="3adaa-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="3adaa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3adaa-112">PARAMETERS</span></span>

### <span data-ttu-id="3adaa-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3adaa-113">-AccountName</span></span>
<span data-ttu-id="3adaa-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3adaa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3adaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3adaa-115">-DefaultProfile</span></span>
<span data-ttu-id="3adaa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3adaa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3adaa-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3adaa-117">-Name</span></span>
<span data-ttu-id="3adaa-118">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="3adaa-118">Name of the Table.</span></span>

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

### <span data-ttu-id="3adaa-119">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3adaa-119">-ParentObject</span></span>
<span data-ttu-id="3adaa-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="3adaa-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3adaa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3adaa-121">-ResourceGroupName</span></span>
<span data-ttu-id="3adaa-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3adaa-122">Name of resource group.</span></span>

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

### <span data-ttu-id="3adaa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3adaa-123">CommonParameters</span></span>
<span data-ttu-id="3adaa-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3adaa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3adaa-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3adaa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3adaa-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3adaa-126">INPUTS</span></span>

### <span data-ttu-id="3adaa-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3adaa-127">None</span></span>

## <span data-ttu-id="3adaa-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3adaa-128">OUTPUTS</span></span>

### <span data-ttu-id="3adaa-129">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="3adaa-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="3adaa-130">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3adaa-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3adaa-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3adaa-131">NOTES</span></span>

## <span data-ttu-id="3adaa-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3adaa-132">RELATED LINKS</span></span>
