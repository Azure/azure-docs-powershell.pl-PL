---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221362"
---
# <span data-ttu-id="96d35-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="96d35-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="96d35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96d35-102">SYNOPSIS</span></span>
<span data-ttu-id="96d35-103">Pobiera przepływność tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="96d35-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="96d35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96d35-104">SYNTAX</span></span>

### <span data-ttu-id="96d35-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96d35-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96d35-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96d35-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96d35-107">Opis</span><span class="sxs-lookup"><span data-stu-id="96d35-107">DESCRIPTION</span></span>
<span data-ttu-id="96d35-108">Polecenie cmdlet **Get-AzCosmosDBTableThroughput** pobiera przepływność tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="96d35-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="96d35-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96d35-109">EXAMPLES</span></span>

### <span data-ttu-id="96d35-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96d35-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="96d35-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96d35-111">PARAMETERS</span></span>

### <span data-ttu-id="96d35-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96d35-112">-AccountName</span></span>
<span data-ttu-id="96d35-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="96d35-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="96d35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d35-114">-DefaultProfile</span></span>
<span data-ttu-id="96d35-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96d35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96d35-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96d35-116">-InputObject</span></span>
<span data-ttu-id="96d35-117">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="96d35-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="96d35-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96d35-118">-Name</span></span>
<span data-ttu-id="96d35-119">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="96d35-119">Name of the Table.</span></span>

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

### <span data-ttu-id="96d35-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d35-120">-ResourceGroupName</span></span>
<span data-ttu-id="96d35-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96d35-121">Name of resource group.</span></span>

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

### <span data-ttu-id="96d35-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d35-122">CommonParameters</span></span>
<span data-ttu-id="96d35-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d35-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d35-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96d35-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d35-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96d35-125">INPUTS</span></span>

### <span data-ttu-id="96d35-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="96d35-126">None</span></span>

## <span data-ttu-id="96d35-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96d35-127">OUTPUTS</span></span>

### <span data-ttu-id="96d35-128">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="96d35-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="96d35-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96d35-129">NOTES</span></span>

## <span data-ttu-id="96d35-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96d35-130">RELATED LINKS</span></span>
