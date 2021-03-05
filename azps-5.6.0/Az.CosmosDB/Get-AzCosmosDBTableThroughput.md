---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7b48190a9ef01d468e762d93d7bc63a96e831de8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986875"
---
# <span data-ttu-id="9d207-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="9d207-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="9d207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d207-102">SYNOPSIS</span></span>
<span data-ttu-id="9d207-103">Pobiera przepływność tabeli AADB.</span><span class="sxs-lookup"><span data-stu-id="9d207-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="9d207-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d207-104">SYNTAX</span></span>

### <span data-ttu-id="9d207-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9d207-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d207-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d207-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d207-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d207-107">DESCRIPTION</span></span>
<span data-ttu-id="9d207-108">Polecenie **cmdlet Get-AzCosmosDBTableThroughput** uzyskuje przepływność tabeli AADB.</span><span class="sxs-lookup"><span data-stu-id="9d207-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="9d207-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d207-109">EXAMPLES</span></span>

### <span data-ttu-id="9d207-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d207-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="9d207-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d207-111">PARAMETERS</span></span>

### <span data-ttu-id="9d207-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9d207-112">-AccountName</span></span>
<span data-ttu-id="9d207-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="9d207-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9d207-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d207-114">-DefaultProfile</span></span>
<span data-ttu-id="9d207-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d207-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d207-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d207-116">-InputObject</span></span>
<span data-ttu-id="9d207-117">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="9d207-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9d207-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d207-118">-Name</span></span>
<span data-ttu-id="9d207-119">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="9d207-119">Name of the Table.</span></span>

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

### <span data-ttu-id="9d207-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d207-120">-ResourceGroupName</span></span>
<span data-ttu-id="9d207-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d207-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9d207-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d207-122">CommonParameters</span></span>
<span data-ttu-id="9d207-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d207-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d207-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d207-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d207-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d207-125">INPUTS</span></span>

### <span data-ttu-id="9d207-126">Brak</span><span class="sxs-lookup"><span data-stu-id="9d207-126">None</span></span>

## <span data-ttu-id="9d207-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d207-127">OUTPUTS</span></span>

### <span data-ttu-id="9d207-128">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9d207-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9d207-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d207-129">NOTES</span></span>

## <span data-ttu-id="9d207-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d207-130">RELATED LINKS</span></span>
