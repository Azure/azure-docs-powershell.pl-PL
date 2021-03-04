---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: f1fb191a235cdf1c98768d3201cab49278f4403c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958849"
---
# <span data-ttu-id="c6ad8-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="c6ad8-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="c6ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ad8-103">Pobiera język Sql StoredProcedure z bazy danych Sql.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="c6ad8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6ad8-104">SYNTAX</span></span>

### <span data-ttu-id="c6ad8-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ad8-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6ad8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ad8-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6ad8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6ad8-107">DESCRIPTION</span></span>
<span data-ttu-id="c6ad8-108">Polecenie cmdlet **Get-AzCosmosDBSqlStoredProcedure** pobiera listę wszystkich istniejących plików WSDB Sql StoredProcedures dla danej nazwy ResourceGroupName, AccountName, DatabaseName i ContainerName, a także otrzymuje pojedynczą bazę danych Sql StoredProcedure dla danej nazwy ResourceGroupName, AccountName, DatabaseName, ContainerName i StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="c6ad8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6ad8-109">EXAMPLES</span></span>

### <span data-ttu-id="c6ad8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6ad8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="c6ad8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6ad8-111">PARAMETERS</span></span>

### <span data-ttu-id="c6ad8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6ad8-112">-AccountName</span></span>
<span data-ttu-id="c6ad8-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c6ad8-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c6ad8-114">-ContainerName</span></span>
<span data-ttu-id="c6ad8-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-115">Container name.</span></span>

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

### <span data-ttu-id="c6ad8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6ad8-116">-DatabaseName</span></span>
<span data-ttu-id="c6ad8-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-117">Database name.</span></span>

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

### <span data-ttu-id="c6ad8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ad8-118">-DefaultProfile</span></span>
<span data-ttu-id="c6ad8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6ad8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c6ad8-120">-Name</span></span>
<span data-ttu-id="c6ad8-121">Przechowywana nazwa Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="c6ad8-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6ad8-122">-ParentObject</span></span>
<span data-ttu-id="c6ad8-123">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-123">Sql Container object.</span></span>

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

### <span data-ttu-id="c6ad8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ad8-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6ad8-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c6ad8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ad8-126">CommonParameters</span></span>
<span data-ttu-id="c6ad8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ad8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ad8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6ad8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ad8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6ad8-129">INPUTS</span></span>

### <span data-ttu-id="c6ad8-130">Brak</span><span class="sxs-lookup"><span data-stu-id="c6ad8-130">None</span></span>

## <span data-ttu-id="c6ad8-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6ad8-131">OUTPUTS</span></span>

### <span data-ttu-id="c6ad8-132">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="c6ad8-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="c6ad8-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6ad8-133">NOTES</span></span>

## <span data-ttu-id="c6ad8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6ad8-134">RELATED LINKS</span></span>
