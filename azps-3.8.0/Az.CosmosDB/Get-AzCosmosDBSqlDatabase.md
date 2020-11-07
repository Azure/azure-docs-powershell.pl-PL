---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896490"
---
# <span data-ttu-id="ad357-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ad357-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="ad357-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad357-102">SYNOPSIS</span></span>
<span data-ttu-id="ad357-103">Pobiera bazę danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ad357-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ad357-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad357-104">SYNTAX</span></span>

### <span data-ttu-id="ad357-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ad357-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad357-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad357-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad357-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad357-107">DESCRIPTION</span></span>
<span data-ttu-id="ad357-108">Polecenie cmdlet **Get-AzCosmosDBSqlDatabase** pobiera listę wszystkich istniejących CosmosDB baz danych SQL dla danego ResourceGroupName, AccountName i pobiera jedną CosmosDB bazę danych SQL dla danego elementu ResourceGroupName, AccountName, DatabaseName i containerName.</span><span class="sxs-lookup"><span data-stu-id="ad357-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="ad357-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad357-109">EXAMPLES</span></span>

### <span data-ttu-id="ad357-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad357-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="ad357-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad357-111">PARAMETERS</span></span>

### <span data-ttu-id="ad357-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad357-112">-AccountName</span></span>
<span data-ttu-id="ad357-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ad357-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ad357-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad357-114">-DefaultProfile</span></span>
<span data-ttu-id="ad357-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad357-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad357-116">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ad357-116">-Detailed</span></span>
<span data-ttu-id="ad357-117">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci kontener z wartością przepływności.</span><span class="sxs-lookup"><span data-stu-id="ad357-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="ad357-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ad357-118">-InputObject</span></span>
<span data-ttu-id="ad357-119">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ad357-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad357-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad357-120">-Name</span></span>
<span data-ttu-id="ad357-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ad357-121">Database name.</span></span>

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

### <span data-ttu-id="ad357-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad357-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad357-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad357-123">Name of resource group.</span></span>

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

### <span data-ttu-id="ad357-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad357-124">CommonParameters</span></span>
<span data-ttu-id="ad357-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad357-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad357-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad357-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad357-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad357-127">INPUTS</span></span>

### <span data-ttu-id="ad357-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ad357-128">None</span></span>

## <span data-ttu-id="ad357-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad357-129">OUTPUTS</span></span>

### <span data-ttu-id="ad357-130">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ad357-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ad357-131">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ad357-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ad357-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad357-132">NOTES</span></span>

## <span data-ttu-id="ad357-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad357-133">RELATED LINKS</span></span>
