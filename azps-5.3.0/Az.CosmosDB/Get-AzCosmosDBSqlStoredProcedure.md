---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503859"
---
# <span data-ttu-id="bbf08-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="bbf08-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="bbf08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbf08-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf08-103">Pobiera CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="bbf08-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="bbf08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbf08-104">SYNTAX</span></span>

### <span data-ttu-id="bbf08-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf08-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbf08-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf08-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbf08-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bbf08-107">DESCRIPTION</span></span>
<span data-ttu-id="bbf08-108">Polecenie cmdlet **Get-AzCosmosDBSqlStoredProcedure** pobiera listę wszystkich istniejących CosmosDB SQL StoredProcedures dla danej ResourceGroupName, AccountName, DatabaseName i ContainerName oraz pobiera jedną CosmosDB SQL StoredProcedure dla danego elementu ResourceGroupName, AccountName, DatabaseName, ContainerName i StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="bbf08-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="bbf08-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbf08-109">EXAMPLES</span></span>

### <span data-ttu-id="bbf08-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bbf08-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="bbf08-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbf08-111">PARAMETERS</span></span>

### <span data-ttu-id="bbf08-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bbf08-112">-AccountName</span></span>
<span data-ttu-id="bbf08-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="bbf08-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bbf08-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bbf08-114">-ContainerName</span></span>
<span data-ttu-id="bbf08-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="bbf08-115">Container name.</span></span>

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

### <span data-ttu-id="bbf08-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bbf08-116">-DatabaseName</span></span>
<span data-ttu-id="bbf08-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bbf08-117">Database name.</span></span>

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

### <span data-ttu-id="bbf08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf08-118">-DefaultProfile</span></span>
<span data-ttu-id="bbf08-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf08-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbf08-120">-Name</span></span>
<span data-ttu-id="bbf08-121">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="bbf08-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="bbf08-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="bbf08-122">-ParentObject</span></span>
<span data-ttu-id="bbf08-123">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="bbf08-123">Sql Container object.</span></span>

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

### <span data-ttu-id="bbf08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf08-124">-ResourceGroupName</span></span>
<span data-ttu-id="bbf08-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bbf08-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bbf08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf08-126">CommonParameters</span></span>
<span data-ttu-id="bbf08-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf08-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbf08-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf08-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbf08-129">INPUTS</span></span>

### <span data-ttu-id="bbf08-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bbf08-130">None</span></span>

## <span data-ttu-id="bbf08-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbf08-131">OUTPUTS</span></span>

### <span data-ttu-id="bbf08-132">Microsoft. Azure. Commands. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="bbf08-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="bbf08-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbf08-133">NOTES</span></span>

## <span data-ttu-id="bbf08-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbf08-134">RELATED LINKS</span></span>
