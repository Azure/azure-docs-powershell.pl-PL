---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0d422014d3cf2ca2ffa18b60c10b50b21bf91144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986903"
---
# <span data-ttu-id="c28fe-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="c28fe-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="c28fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c28fe-103">Pobiera funkcję Sql User Defined Function (Czas) języka Sql.</span><span class="sxs-lookup"><span data-stu-id="c28fe-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="c28fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c28fe-104">SYNTAX</span></span>

### <span data-ttu-id="c28fe-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c28fe-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c28fe-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c28fe-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c28fe-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c28fe-107">DESCRIPTION</span></span>
<span data-ttu-id="c28fe-108">Polecenie **cmdlet Get-AzCosmosDBSqlUserDefinedFunction** pobiera listę wszystkich istniejących plików akusdb sql UserDefinedFunctions dla danej nazwy grupy zasobów, nazwa_konta, nazwa_bazy danych i nazwa_kontenera oraz otrzymuje pojedynczą nazwę ADB Sql UserDefinedFunction dla danej właściwości ResourceGroupName, AccountName, DatabaseName, ContainerName i UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="c28fe-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="c28fe-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c28fe-109">EXAMPLES</span></span>

### <span data-ttu-id="c28fe-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c28fe-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="c28fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c28fe-111">PARAMETERS</span></span>

### <span data-ttu-id="c28fe-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c28fe-112">-AccountName</span></span>
<span data-ttu-id="c28fe-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="c28fe-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c28fe-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c28fe-114">-ContainerName</span></span>
<span data-ttu-id="c28fe-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="c28fe-115">Container name.</span></span>

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

### <span data-ttu-id="c28fe-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c28fe-116">-DatabaseName</span></span>
<span data-ttu-id="c28fe-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c28fe-117">Database name.</span></span>

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

### <span data-ttu-id="c28fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28fe-118">-DefaultProfile</span></span>
<span data-ttu-id="c28fe-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c28fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28fe-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c28fe-120">-Name</span></span>
<span data-ttu-id="c28fe-121">Nazwa funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c28fe-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="c28fe-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c28fe-122">-ParentObject</span></span>
<span data-ttu-id="c28fe-123">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="c28fe-123">Sql Container object.</span></span>

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

### <span data-ttu-id="c28fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="c28fe-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c28fe-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c28fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28fe-126">CommonParameters</span></span>
<span data-ttu-id="c28fe-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28fe-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c28fe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28fe-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c28fe-129">INPUTS</span></span>

### <span data-ttu-id="c28fe-130">Brak</span><span class="sxs-lookup"><span data-stu-id="c28fe-130">None</span></span>

## <span data-ttu-id="c28fe-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c28fe-131">OUTPUTS</span></span>

### <span data-ttu-id="c28fe-132">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="c28fe-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="c28fe-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c28fe-133">NOTES</span></span>

## <span data-ttu-id="c28fe-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c28fe-134">RELATED LINKS</span></span>
