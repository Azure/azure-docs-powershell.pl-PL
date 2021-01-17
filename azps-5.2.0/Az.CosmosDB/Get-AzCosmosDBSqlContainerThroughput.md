---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351169"
---
# <span data-ttu-id="aa862-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="aa862-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="aa862-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa862-102">SYNOPSIS</span></span>
<span data-ttu-id="aa862-103">Pobiera ustawienia przepływności odpowiadające kontenerowi SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="aa862-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="aa862-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa862-104">SYNTAX</span></span>

### <span data-ttu-id="aa862-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa862-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa862-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa862-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa862-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aa862-107">DESCRIPTION</span></span>
<span data-ttu-id="aa862-108">Polecenie cmdlet **Get-AzCosmosDBSqlContainerThroughput** pobiera ustawienia przepływności odpowiadające kontenerowi SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="aa862-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="aa862-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa862-109">EXAMPLES</span></span>

### <span data-ttu-id="aa862-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa862-110">Example 1</span></span>
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

## <span data-ttu-id="aa862-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa862-111">PARAMETERS</span></span>

### <span data-ttu-id="aa862-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa862-112">-AccountName</span></span>
<span data-ttu-id="aa862-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="aa862-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aa862-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa862-114">-DatabaseName</span></span>
<span data-ttu-id="aa862-115">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="aa862-115">Database name.</span></span>

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

### <span data-ttu-id="aa862-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa862-116">-DefaultProfile</span></span>
<span data-ttu-id="aa862-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa862-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa862-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa862-118">-InputObject</span></span>
<span data-ttu-id="aa862-119">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="aa862-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa862-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa862-120">-Name</span></span>
<span data-ttu-id="aa862-121">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="aa862-121">Container name.</span></span>

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

### <span data-ttu-id="aa862-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa862-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa862-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa862-123">Name of resource group.</span></span>

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

### <span data-ttu-id="aa862-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa862-124">CommonParameters</span></span>
<span data-ttu-id="aa862-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa862-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa862-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa862-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa862-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa862-127">INPUTS</span></span>

### <span data-ttu-id="aa862-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aa862-128">None</span></span>

## <span data-ttu-id="aa862-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa862-129">OUTPUTS</span></span>

### <span data-ttu-id="aa862-130">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="aa862-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="aa862-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa862-131">NOTES</span></span>

## <span data-ttu-id="aa862-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa862-132">RELATED LINKS</span></span>
