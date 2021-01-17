---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351181"
---
# <span data-ttu-id="d7535-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="d7535-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="d7535-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7535-102">SYNOPSIS</span></span>
<span data-ttu-id="d7535-103">Pobiera kontener SQL programu CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d7535-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="d7535-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7535-104">SYNTAX</span></span>

### <span data-ttu-id="d7535-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7535-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="d7535-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7535-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7535-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7535-107">DESCRIPTION</span></span>
<span data-ttu-id="d7535-108">Polecenie cmdlet **Get-AzCosmosDBSqlContainer** pobiera listę wszystkich istniejących kontenerów SQL CosmosDB dla danego ResourceGroupName, AccountName i DatabaseName, a następnie pobiera jeden kontener CosmosDB SQL dla danego elementu ResourceGroupName, AccountName, DatabaseName i containerName.</span><span class="sxs-lookup"><span data-stu-id="d7535-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="d7535-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7535-109">EXAMPLES</span></span>

### <span data-ttu-id="d7535-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7535-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="d7535-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7535-111">PARAMETERS</span></span>

### <span data-ttu-id="d7535-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7535-112">-AccountName</span></span>
<span data-ttu-id="d7535-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="d7535-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d7535-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7535-114">-DatabaseName</span></span>
<span data-ttu-id="d7535-115">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d7535-115">Database name.</span></span>

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

### <span data-ttu-id="d7535-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7535-116">-DefaultProfile</span></span>
<span data-ttu-id="d7535-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7535-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7535-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7535-118">-Name</span></span>
<span data-ttu-id="d7535-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7535-119">Container name.</span></span>

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

### <span data-ttu-id="d7535-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="d7535-120">-ParentObject</span></span>
<span data-ttu-id="d7535-121">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d7535-121">Sql Database object.</span></span>

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

### <span data-ttu-id="d7535-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7535-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7535-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7535-123">Name of resource group.</span></span>

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

### <span data-ttu-id="d7535-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7535-124">CommonParameters</span></span>
<span data-ttu-id="d7535-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7535-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7535-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7535-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7535-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7535-127">INPUTS</span></span>

### <span data-ttu-id="d7535-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d7535-128">None</span></span>

## <span data-ttu-id="d7535-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7535-129">OUTPUTS</span></span>

### <span data-ttu-id="d7535-130">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d7535-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="d7535-131">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d7535-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d7535-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7535-132">NOTES</span></span>

## <span data-ttu-id="d7535-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7535-133">RELATED LINKS</span></span>
