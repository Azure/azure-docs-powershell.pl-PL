---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501766"
---
# <span data-ttu-id="e7ebf-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="e7ebf-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="e7ebf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ebf-103">Pobiera właściwości przepływności CosmosDB bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="e7ebf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7ebf-104">SYNTAX</span></span>

### <span data-ttu-id="e7ebf-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7ebf-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7ebf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7ebf-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7ebf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7ebf-107">DESCRIPTION</span></span>
<span data-ttu-id="e7ebf-108">Polecenie cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** pobiera właściwości przepływności bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="e7ebf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7ebf-109">EXAMPLES</span></span>

### <span data-ttu-id="e7ebf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7ebf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="e7ebf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7ebf-111">PARAMETERS</span></span>

### <span data-ttu-id="e7ebf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7ebf-112">-AccountName</span></span>
<span data-ttu-id="e7ebf-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e7ebf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ebf-114">-DefaultProfile</span></span>
<span data-ttu-id="e7ebf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7ebf-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e7ebf-116">-InputObject</span></span>
<span data-ttu-id="e7ebf-117">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e7ebf-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e7ebf-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7ebf-118">-Name</span></span>
<span data-ttu-id="e7ebf-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-119">Database name.</span></span>

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

### <span data-ttu-id="e7ebf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ebf-120">-ResourceGroupName</span></span>
<span data-ttu-id="e7ebf-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-121">Name of resource group.</span></span>

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

### <span data-ttu-id="e7ebf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ebf-122">CommonParameters</span></span>
<span data-ttu-id="e7ebf-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ebf-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7ebf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ebf-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7ebf-125">INPUTS</span></span>

### <span data-ttu-id="e7ebf-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e7ebf-126">None</span></span>

## <span data-ttu-id="e7ebf-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7ebf-127">OUTPUTS</span></span>

### <span data-ttu-id="e7ebf-128">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e7ebf-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e7ebf-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7ebf-129">NOTES</span></span>

## <span data-ttu-id="e7ebf-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7ebf-130">RELATED LINKS</span></span>
