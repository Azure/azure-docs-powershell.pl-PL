---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049527"
---
# <span data-ttu-id="09144-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="09144-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="09144-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09144-102">SYNOPSIS</span></span>
<span data-ttu-id="09144-103">Pobiera CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="09144-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="09144-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09144-104">SYNTAX</span></span>

### <span data-ttu-id="09144-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09144-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09144-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09144-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09144-107">Opis</span><span class="sxs-lookup"><span data-stu-id="09144-107">DESCRIPTION</span></span>
<span data-ttu-id="09144-108">Polecenie cmdlet **Get-AzCosmosDBSqlStoredProcedure** pobiera listę wszystkich istniejących CosmosDB SQL StoredProcedures dla danej ResourceGroupName, AccountName, DatabaseName i ContainerName oraz pobiera jedną CosmosDB SQL StoredProcedure dla danego elementu ResourceGroupName, AccountName, DatabaseName, ContainerName i StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="09144-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="09144-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09144-109">EXAMPLES</span></span>

### <span data-ttu-id="09144-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09144-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="09144-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09144-111">PARAMETERS</span></span>

### <span data-ttu-id="09144-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09144-112">-AccountName</span></span>
<span data-ttu-id="09144-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="09144-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09144-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="09144-114">-ContainerName</span></span>
<span data-ttu-id="09144-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="09144-115">Container name.</span></span>

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

### <span data-ttu-id="09144-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09144-116">-DatabaseName</span></span>
<span data-ttu-id="09144-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="09144-117">Database name.</span></span>

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

### <span data-ttu-id="09144-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09144-118">-DefaultProfile</span></span>
<span data-ttu-id="09144-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09144-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09144-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09144-120">-InputObject</span></span>
<span data-ttu-id="09144-121">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="09144-121">Sql Container object.</span></span>

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

### <span data-ttu-id="09144-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09144-122">-Name</span></span>
<span data-ttu-id="09144-123">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="09144-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="09144-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09144-124">-ResourceGroupName</span></span>
<span data-ttu-id="09144-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09144-125">Name of resource group.</span></span>

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

### <span data-ttu-id="09144-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09144-126">CommonParameters</span></span>
<span data-ttu-id="09144-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09144-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09144-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09144-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09144-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09144-129">INPUTS</span></span>

### <span data-ttu-id="09144-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="09144-130">None</span></span>

## <span data-ttu-id="09144-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09144-131">OUTPUTS</span></span>

### <span data-ttu-id="09144-132">Microsoft. Azure. Commands. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="09144-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="09144-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09144-133">NOTES</span></span>

## <span data-ttu-id="09144-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09144-134">RELATED LINKS</span></span>
