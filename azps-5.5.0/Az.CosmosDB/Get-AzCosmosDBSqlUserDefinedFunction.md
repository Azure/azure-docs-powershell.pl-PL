---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181378"
---
# <span data-ttu-id="81f05-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="81f05-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="81f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f05-102">SYNOPSIS</span></span>
<span data-ttu-id="81f05-103">Pobiera funkcję Sql User Defined Function (Czas) języka Sql.</span><span class="sxs-lookup"><span data-stu-id="81f05-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="81f05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81f05-104">SYNTAX</span></span>

### <span data-ttu-id="81f05-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="81f05-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81f05-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81f05-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81f05-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="81f05-107">DESCRIPTION</span></span>
<span data-ttu-id="81f05-108">Polecenie **cmdlet Get-AzCosmosDBSqlUserDefinedFunction** pobiera listę wszystkich istniejących plików akusdb sql UserDefinedFunctions dla danej nazwy Grupy Zasobów, Nazwa_konta, Nazwa_bazy danych i Nazwa_kontenera oraz otrzymuje pojedynczą nazwę AlejaDb Sql UserDefinedFunction dla danej nazwy ResourceGroupName, AccountName, DatabaseName, ContainerName i UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="81f05-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="81f05-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81f05-109">EXAMPLES</span></span>

### <span data-ttu-id="81f05-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81f05-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="81f05-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81f05-111">PARAMETERS</span></span>

### <span data-ttu-id="81f05-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81f05-112">-AccountName</span></span>
<span data-ttu-id="81f05-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="81f05-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81f05-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="81f05-114">-ContainerName</span></span>
<span data-ttu-id="81f05-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="81f05-115">Container name.</span></span>

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

### <span data-ttu-id="81f05-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81f05-116">-DatabaseName</span></span>
<span data-ttu-id="81f05-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="81f05-117">Database name.</span></span>

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

### <span data-ttu-id="81f05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f05-118">-DefaultProfile</span></span>
<span data-ttu-id="81f05-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="81f05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f05-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="81f05-120">-Name</span></span>
<span data-ttu-id="81f05-121">Nazwa funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="81f05-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="81f05-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="81f05-122">-ParentObject</span></span>
<span data-ttu-id="81f05-123">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="81f05-123">Sql Container object.</span></span>

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

### <span data-ttu-id="81f05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f05-124">-ResourceGroupName</span></span>
<span data-ttu-id="81f05-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81f05-125">Name of resource group.</span></span>

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

### <span data-ttu-id="81f05-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f05-126">CommonParameters</span></span>
<span data-ttu-id="81f05-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f05-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f05-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81f05-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f05-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81f05-129">INPUTS</span></span>

### <span data-ttu-id="81f05-130">Brak</span><span class="sxs-lookup"><span data-stu-id="81f05-130">None</span></span>

## <span data-ttu-id="81f05-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81f05-131">OUTPUTS</span></span>

### <span data-ttu-id="81f05-132">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="81f05-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="81f05-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81f05-133">NOTES</span></span>

## <span data-ttu-id="81f05-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81f05-134">RELATED LINKS</span></span>
