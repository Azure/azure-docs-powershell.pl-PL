---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053074"
---
# <span data-ttu-id="0848e-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="0848e-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="0848e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0848e-102">SYNOPSIS</span></span>
<span data-ttu-id="0848e-103">Pobiera kontener SQL programu CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0848e-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0848e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0848e-104">SYNTAX</span></span>

### <span data-ttu-id="0848e-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0848e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="0848e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0848e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0848e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0848e-107">DESCRIPTION</span></span>
<span data-ttu-id="0848e-108">Polecenie cmdlet **Get-AzCosmosDBSqlContainer** pobiera listę wszystkich istniejących kontenerów SQL CosmosDB dla danego ResourceGroupName, AccountName i DatabaseName, a następnie pobiera jeden kontener CosmosDB SQL dla danego elementu ResourceGroupName, AccountName, DatabaseName i containerName.</span><span class="sxs-lookup"><span data-stu-id="0848e-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="0848e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0848e-109">EXAMPLES</span></span>

### <span data-ttu-id="0848e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0848e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="0848e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0848e-111">PARAMETERS</span></span>

### <span data-ttu-id="0848e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0848e-112">-AccountName</span></span>
<span data-ttu-id="0848e-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0848e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0848e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0848e-114">-DatabaseName</span></span>
<span data-ttu-id="0848e-115">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0848e-115">Database name.</span></span>

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

### <span data-ttu-id="0848e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0848e-116">-DefaultProfile</span></span>
<span data-ttu-id="0848e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0848e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0848e-118">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0848e-118">-Detailed</span></span>
<span data-ttu-id="0848e-119">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci kontener z wartością przepływności.</span><span class="sxs-lookup"><span data-stu-id="0848e-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="0848e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0848e-120">-InputObject</span></span>
<span data-ttu-id="0848e-121">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0848e-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0848e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0848e-122">-Name</span></span>
<span data-ttu-id="0848e-123">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="0848e-123">Container name.</span></span>

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

### <span data-ttu-id="0848e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0848e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0848e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0848e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0848e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0848e-126">CommonParameters</span></span>
<span data-ttu-id="0848e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0848e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0848e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0848e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0848e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0848e-129">INPUTS</span></span>

### <span data-ttu-id="0848e-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0848e-130">None</span></span>

## <span data-ttu-id="0848e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0848e-131">OUTPUTS</span></span>

### <span data-ttu-id="0848e-132">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="0848e-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="0848e-133">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0848e-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0848e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0848e-134">NOTES</span></span>

## <span data-ttu-id="0848e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0848e-135">RELATED LINKS</span></span>
