---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 684572dd9b43f68eab0497d2603fea30c747415a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053071"
---
# <span data-ttu-id="e8cd1-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="e8cd1-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="e8cd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cd1-103">Pobiera przepływność tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e8cd1-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="e8cd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8cd1-104">SYNTAX</span></span>

### <span data-ttu-id="e8cd1-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8cd1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cd1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8cd1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8cd1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8cd1-107">DESCRIPTION</span></span>
<span data-ttu-id="e8cd1-108">Polecenie cmdlet **Get-AzCosmosDBTableThroughput** pobiera przepływność tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e8cd1-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="e8cd1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8cd1-109">EXAMPLES</span></span>

### <span data-ttu-id="e8cd1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8cd1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="e8cd1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8cd1-111">PARAMETERS</span></span>

### <span data-ttu-id="e8cd1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8cd1-112">-AccountName</span></span>
<span data-ttu-id="e8cd1-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8cd1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e8cd1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cd1-114">-DefaultProfile</span></span>
<span data-ttu-id="e8cd1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8cd1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8cd1-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8cd1-116">-InputObject</span></span>
<span data-ttu-id="e8cd1-117">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e8cd1-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8cd1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8cd1-118">-Name</span></span>
<span data-ttu-id="e8cd1-119">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="e8cd1-119">Name of the Table.</span></span>

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

### <span data-ttu-id="e8cd1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cd1-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8cd1-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8cd1-121">Name of resource group.</span></span>

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

### <span data-ttu-id="e8cd1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cd1-122">CommonParameters</span></span>
<span data-ttu-id="e8cd1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8cd1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cd1-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8cd1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cd1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8cd1-125">INPUTS</span></span>

### <span data-ttu-id="e8cd1-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e8cd1-126">None</span></span>

## <span data-ttu-id="e8cd1-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8cd1-127">OUTPUTS</span></span>

### <span data-ttu-id="e8cd1-128">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e8cd1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e8cd1-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8cd1-129">NOTES</span></span>

## <span data-ttu-id="e8cd1-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8cd1-130">RELATED LINKS</span></span>
