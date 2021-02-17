---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177314"
---
# <span data-ttu-id="c0f23-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="c0f23-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="c0f23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0f23-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f23-103">Pobiera język Sql StoredProcedure z bazy danych Sql.</span><span class="sxs-lookup"><span data-stu-id="c0f23-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="c0f23-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0f23-104">SYNTAX</span></span>

### <span data-ttu-id="c0f23-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0f23-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0f23-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0f23-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f23-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0f23-107">DESCRIPTION</span></span>
<span data-ttu-id="c0f23-108">Polecenie cmdlet **Get-AzCosmosDBSqlStoredProcedure** pobiera listę wszystkich istniejących plików WSDB Sql StoredProcedures dla danej nazwy ResourceGroupName, AccountName, DatabaseName i ContainerName, a także otrzymuje pojedynczą bazę danych Sql StoredProcedure dla danej nazwy ResourceGroupName, AccountName, DatabaseName, ContainerName i StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="c0f23-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="c0f23-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0f23-109">EXAMPLES</span></span>

### <span data-ttu-id="c0f23-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0f23-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="c0f23-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0f23-111">PARAMETERS</span></span>

### <span data-ttu-id="c0f23-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0f23-112">-AccountName</span></span>
<span data-ttu-id="c0f23-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="c0f23-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c0f23-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c0f23-114">-ContainerName</span></span>
<span data-ttu-id="c0f23-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="c0f23-115">Container name.</span></span>

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

### <span data-ttu-id="c0f23-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0f23-116">-DatabaseName</span></span>
<span data-ttu-id="c0f23-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c0f23-117">Database name.</span></span>

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

### <span data-ttu-id="c0f23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f23-118">-DefaultProfile</span></span>
<span data-ttu-id="c0f23-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0f23-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0f23-120">-Name</span></span>
<span data-ttu-id="c0f23-121">Przechowywana nazwa Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="c0f23-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="c0f23-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c0f23-122">-ParentObject</span></span>
<span data-ttu-id="c0f23-123">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="c0f23-123">Sql Container object.</span></span>

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

### <span data-ttu-id="c0f23-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f23-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0f23-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0f23-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c0f23-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f23-126">CommonParameters</span></span>
<span data-ttu-id="c0f23-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f23-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f23-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0f23-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f23-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0f23-129">INPUTS</span></span>

### <span data-ttu-id="c0f23-130">Brak</span><span class="sxs-lookup"><span data-stu-id="c0f23-130">None</span></span>

## <span data-ttu-id="c0f23-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0f23-131">OUTPUTS</span></span>

### <span data-ttu-id="c0f23-132">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="c0f23-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="c0f23-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0f23-133">NOTES</span></span>

## <span data-ttu-id="c0f23-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0f23-134">RELATED LINKS</span></span>
