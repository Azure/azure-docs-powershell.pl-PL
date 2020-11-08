---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 61acd388dabcfe71c83d282d032e9d4bb688d88b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053075"
---
# <span data-ttu-id="4efb5-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="4efb5-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="4efb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4efb5-102">SYNOPSIS</span></span>
<span data-ttu-id="4efb5-103">Pobiera ustawienia przepływności odpowiadające kontenerowi SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4efb5-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="4efb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4efb5-104">SYNTAX</span></span>

### <span data-ttu-id="4efb5-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4efb5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4efb5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4efb5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4efb5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4efb5-107">DESCRIPTION</span></span>
<span data-ttu-id="4efb5-108">Polecenie cmdlet **Get-AzCosmosDBSqlContainerThroughput** pobiera ustawienia przepływności odpowiadające kontenerowi SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4efb5-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="4efb5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4efb5-109">EXAMPLES</span></span>

### <span data-ttu-id="4efb5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4efb5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="4efb5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4efb5-111">PARAMETERS</span></span>

### <span data-ttu-id="4efb5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4efb5-112">-AccountName</span></span>
<span data-ttu-id="4efb5-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4efb5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4efb5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4efb5-114">-DatabaseName</span></span>
<span data-ttu-id="4efb5-115">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4efb5-115">Database name.</span></span>

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

### <span data-ttu-id="4efb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efb5-116">-DefaultProfile</span></span>
<span data-ttu-id="4efb5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4efb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4efb5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4efb5-118">-InputObject</span></span>
<span data-ttu-id="4efb5-119">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="4efb5-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4efb5-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4efb5-120">-Name</span></span>
<span data-ttu-id="4efb5-121">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="4efb5-121">Container name.</span></span>

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

### <span data-ttu-id="4efb5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4efb5-122">-ResourceGroupName</span></span>
<span data-ttu-id="4efb5-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4efb5-123">Name of resource group.</span></span>

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

### <span data-ttu-id="4efb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efb5-124">CommonParameters</span></span>
<span data-ttu-id="4efb5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4efb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efb5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4efb5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efb5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4efb5-127">INPUTS</span></span>

### <span data-ttu-id="4efb5-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4efb5-128">None</span></span>

## <span data-ttu-id="4efb5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4efb5-129">OUTPUTS</span></span>

### <span data-ttu-id="4efb5-130">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4efb5-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4efb5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4efb5-131">NOTES</span></span>

## <span data-ttu-id="4efb5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4efb5-132">RELATED LINKS</span></span>
