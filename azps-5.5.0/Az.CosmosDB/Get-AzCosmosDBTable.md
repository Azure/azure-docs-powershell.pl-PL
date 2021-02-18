---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181371"
---
# <span data-ttu-id="9f1d3-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="9f1d3-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="9f1d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1d3-103">Pobiera tabelę DosyćDB.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="9f1d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9f1d3-104">SYNTAX</span></span>

### <span data-ttu-id="9f1d3-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9f1d3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f1d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f1d3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f1d3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9f1d3-107">DESCRIPTION</span></span>
<span data-ttu-id="9f1d3-108">Polecenie **cmdlet Get-AzCosmosDBTable** pobiera istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="9f1d3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9f1d3-109">EXAMPLES</span></span>

### <span data-ttu-id="9f1d3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9f1d3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="9f1d3-111">Obiekt zasobu _rid właściwości _ts, _ts_ tagu etag tabeli.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="9f1d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f1d3-112">PARAMETERS</span></span>

### <span data-ttu-id="9f1d3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9f1d3-113">-AccountName</span></span>
<span data-ttu-id="9f1d3-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f1d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1d3-115">-DefaultProfile</span></span>
<span data-ttu-id="9f1d3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f1d3-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9f1d3-117">-Name</span></span>
<span data-ttu-id="9f1d3-118">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-118">Name of the Table.</span></span>

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

### <span data-ttu-id="9f1d3-119">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="9f1d3-119">-ParentObject</span></span>
<span data-ttu-id="9f1d3-120">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="9f1d3-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9f1d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1d3-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f1d3-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-122">Name of resource group.</span></span>

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

### <span data-ttu-id="9f1d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1d3-123">CommonParameters</span></span>
<span data-ttu-id="9f1d3-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1d3-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f1d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1d3-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f1d3-126">INPUTS</span></span>

### <span data-ttu-id="9f1d3-127">Brak</span><span class="sxs-lookup"><span data-stu-id="9f1d3-127">None</span></span>

## <span data-ttu-id="9f1d3-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f1d3-128">OUTPUTS</span></span>

### <span data-ttu-id="9f1d3-129">Microsoft.Azure.Commands.Dosdb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="9f1d3-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="9f1d3-130">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9f1d3-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9f1d3-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9f1d3-131">NOTES</span></span>

## <span data-ttu-id="9f1d3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f1d3-132">RELATED LINKS</span></span>
