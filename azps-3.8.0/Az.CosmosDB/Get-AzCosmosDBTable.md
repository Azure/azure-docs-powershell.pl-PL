---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053848"
---
# <span data-ttu-id="54dc5-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="54dc5-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="54dc5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="54dc5-103">Pobiera tabelę CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="54dc5-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="54dc5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54dc5-104">SYNTAX</span></span>

### <span data-ttu-id="54dc5-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="54dc5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54dc5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54dc5-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54dc5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="54dc5-107">DESCRIPTION</span></span>
<span data-ttu-id="54dc5-108">Polecenie cmdlet **Get-AzCosmosDBTable** pobiera istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="54dc5-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="54dc5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54dc5-109">EXAMPLES</span></span>

### <span data-ttu-id="54dc5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54dc5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="54dc5-111">Obiekt zasobu zawiera właściwości _rid, _ts, ETag tabeli.</span><span class="sxs-lookup"><span data-stu-id="54dc5-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="54dc5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54dc5-112">PARAMETERS</span></span>

### <span data-ttu-id="54dc5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54dc5-113">-AccountName</span></span>
<span data-ttu-id="54dc5-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="54dc5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="54dc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54dc5-115">-DefaultProfile</span></span>
<span data-ttu-id="54dc5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54dc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54dc5-117">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="54dc5-117">-Detailed</span></span>
<span data-ttu-id="54dc5-118">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci tabelę z odpowiednią wartością przepustowości.</span><span class="sxs-lookup"><span data-stu-id="54dc5-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="54dc5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54dc5-119">-InputObject</span></span>
<span data-ttu-id="54dc5-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="54dc5-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54dc5-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54dc5-121">-Name</span></span>
<span data-ttu-id="54dc5-122">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="54dc5-122">Name of the Table.</span></span>

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

### <span data-ttu-id="54dc5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54dc5-123">-ResourceGroupName</span></span>
<span data-ttu-id="54dc5-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54dc5-124">Name of resource group.</span></span>

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

### <span data-ttu-id="54dc5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54dc5-125">CommonParameters</span></span>
<span data-ttu-id="54dc5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54dc5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54dc5-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54dc5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54dc5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54dc5-128">INPUTS</span></span>

### <span data-ttu-id="54dc5-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="54dc5-129">None</span></span>

## <span data-ttu-id="54dc5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54dc5-130">OUTPUTS</span></span>

### <span data-ttu-id="54dc5-131">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="54dc5-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="54dc5-132">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="54dc5-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="54dc5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54dc5-133">NOTES</span></span>

## <span data-ttu-id="54dc5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54dc5-134">RELATED LINKS</span></span>
