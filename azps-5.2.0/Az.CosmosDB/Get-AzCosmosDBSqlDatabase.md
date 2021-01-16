---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333733"
---
# <span data-ttu-id="71af1-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71af1-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="71af1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71af1-102">SYNOPSIS</span></span>
<span data-ttu-id="71af1-103">Pobiera bazę danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="71af1-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="71af1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71af1-104">SYNTAX</span></span>

### <span data-ttu-id="71af1-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="71af1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71af1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71af1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71af1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="71af1-107">DESCRIPTION</span></span>
<span data-ttu-id="71af1-108">Polecenie cmdlet **Get-AzCosmosDBSqlDatabase** pobiera listę wszystkich istniejących CosmosDB baz danych SQL dla danego ResourceGroupName, AccountName i pobiera jedną CosmosDB bazę danych SQL dla danego elementu ResourceGroupName, AccountName, DatabaseName i containerName.</span><span class="sxs-lookup"><span data-stu-id="71af1-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="71af1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71af1-109">EXAMPLES</span></span>

### <span data-ttu-id="71af1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71af1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="71af1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71af1-111">PARAMETERS</span></span>

### <span data-ttu-id="71af1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71af1-112">-AccountName</span></span>
<span data-ttu-id="71af1-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="71af1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="71af1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71af1-114">-DefaultProfile</span></span>
<span data-ttu-id="71af1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71af1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71af1-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71af1-116">-Name</span></span>
<span data-ttu-id="71af1-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="71af1-117">Database name.</span></span>

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

### <span data-ttu-id="71af1-118">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="71af1-118">-ParentObject</span></span>
<span data-ttu-id="71af1-119">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="71af1-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71af1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71af1-120">-ResourceGroupName</span></span>
<span data-ttu-id="71af1-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71af1-121">Name of resource group.</span></span>

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

### <span data-ttu-id="71af1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71af1-122">CommonParameters</span></span>
<span data-ttu-id="71af1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71af1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71af1-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71af1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71af1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71af1-125">INPUTS</span></span>

### <span data-ttu-id="71af1-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="71af1-126">None</span></span>

## <span data-ttu-id="71af1-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71af1-127">OUTPUTS</span></span>

### <span data-ttu-id="71af1-128">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="71af1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="71af1-129">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="71af1-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="71af1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71af1-130">NOTES</span></span>

## <span data-ttu-id="71af1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71af1-131">RELATED LINKS</span></span>
