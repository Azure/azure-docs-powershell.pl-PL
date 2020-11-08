---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1d470870d27001a07302240dba1abd7e56153d0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053073"
---
# <span data-ttu-id="23cfa-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="23cfa-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="23cfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="23cfa-103">Pobiera właściwości przepływności CosmosDB bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="23cfa-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="23cfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23cfa-104">SYNTAX</span></span>

### <span data-ttu-id="23cfa-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23cfa-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23cfa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23cfa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23cfa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23cfa-107">DESCRIPTION</span></span>
<span data-ttu-id="23cfa-108">Polecenie cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** pobiera właściwości przepływności bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="23cfa-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="23cfa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23cfa-109">EXAMPLES</span></span>

### <span data-ttu-id="23cfa-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23cfa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="23cfa-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23cfa-111">PARAMETERS</span></span>

### <span data-ttu-id="23cfa-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23cfa-112">-AccountName</span></span>
<span data-ttu-id="23cfa-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="23cfa-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="23cfa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cfa-114">-DefaultProfile</span></span>
<span data-ttu-id="23cfa-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23cfa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cfa-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23cfa-116">-InputObject</span></span>
<span data-ttu-id="23cfa-117">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="23cfa-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="23cfa-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23cfa-118">-Name</span></span>
<span data-ttu-id="23cfa-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="23cfa-119">Database name.</span></span>

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

### <span data-ttu-id="23cfa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cfa-120">-ResourceGroupName</span></span>
<span data-ttu-id="23cfa-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23cfa-121">Name of resource group.</span></span>

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

### <span data-ttu-id="23cfa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cfa-122">CommonParameters</span></span>
<span data-ttu-id="23cfa-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cfa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cfa-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23cfa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cfa-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cfa-125">INPUTS</span></span>

### <span data-ttu-id="23cfa-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="23cfa-126">None</span></span>

## <span data-ttu-id="23cfa-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23cfa-127">OUTPUTS</span></span>

### <span data-ttu-id="23cfa-128">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="23cfa-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="23cfa-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23cfa-129">NOTES</span></span>

## <span data-ttu-id="23cfa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cfa-130">RELATED LINKS</span></span>
