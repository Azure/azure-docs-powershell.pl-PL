---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062852"
---
# <span data-ttu-id="c33f0-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="c33f0-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="c33f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c33f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c33f0-103">Pobiera CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="c33f0-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="c33f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c33f0-104">SYNTAX</span></span>

### <span data-ttu-id="c33f0-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c33f0-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c33f0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c33f0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c33f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c33f0-107">DESCRIPTION</span></span>
<span data-ttu-id="c33f0-108">Polecenie cmdlet **Get-AzCosmosDBSqlStoredProcedure** pobiera listę wszystkich istniejących CosmosDB SQL StoredProcedures dla danej ResourceGroupName, AccountName, DatabaseName i ContainerName oraz pobiera jedną CosmosDB SQL StoredProcedure dla danego elementu ResourceGroupName, AccountName, DatabaseName, ContainerName i StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="c33f0-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="c33f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c33f0-109">EXAMPLES</span></span>

### <span data-ttu-id="c33f0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c33f0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="c33f0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c33f0-111">PARAMETERS</span></span>

### <span data-ttu-id="c33f0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c33f0-112">-AccountName</span></span>
<span data-ttu-id="c33f0-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c33f0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c33f0-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c33f0-114">-ContainerName</span></span>
<span data-ttu-id="c33f0-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="c33f0-115">Container name.</span></span>

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

### <span data-ttu-id="c33f0-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c33f0-116">-DatabaseName</span></span>
<span data-ttu-id="c33f0-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c33f0-117">Database name.</span></span>

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

### <span data-ttu-id="c33f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33f0-118">-DefaultProfile</span></span>
<span data-ttu-id="c33f0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c33f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c33f0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c33f0-120">-Name</span></span>
<span data-ttu-id="c33f0-121">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="c33f0-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="c33f0-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="c33f0-122">-ParentObject</span></span>
<span data-ttu-id="c33f0-123">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="c33f0-123">Sql Container object.</span></span>

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

### <span data-ttu-id="c33f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c33f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="c33f0-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c33f0-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c33f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33f0-126">CommonParameters</span></span>
<span data-ttu-id="c33f0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33f0-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c33f0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33f0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c33f0-129">INPUTS</span></span>

### <span data-ttu-id="c33f0-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c33f0-130">None</span></span>

## <span data-ttu-id="c33f0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c33f0-131">OUTPUTS</span></span>

### <span data-ttu-id="c33f0-132">Microsoft. Azure. Commands. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="c33f0-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="c33f0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c33f0-133">NOTES</span></span>

## <span data-ttu-id="c33f0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c33f0-134">RELATED LINKS</span></span>
