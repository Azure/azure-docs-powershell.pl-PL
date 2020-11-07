---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: c8cfb1077f418c9d671729cb0ff762141a7b77c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894777"
---
# <span data-ttu-id="1bcaa-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="1bcaa-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="1bcaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="1bcaa-103">Pobiera CosmosDB funkcji zdefiniowanej przez użytkownika SQL.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="1bcaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bcaa-104">SYNTAX</span></span>

### <span data-ttu-id="1bcaa-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcaa-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bcaa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcaa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bcaa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1bcaa-107">DESCRIPTION</span></span>
<span data-ttu-id="1bcaa-108">Polecenie cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** pobiera listę wszystkich istniejących CosmosDB SQL UserDefinedFunctions dla danej ResourceGroupName, AccountName, DatabaseName i ContainerName oraz pobiera jedną CosmosDB SQL UserDefinedFunction dla danego elementu ResourceGroupName, AccountName, DatabaseName, ContainerName i UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="1bcaa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bcaa-109">EXAMPLES</span></span>

### <span data-ttu-id="1bcaa-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1bcaa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="1bcaa-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bcaa-111">PARAMETERS</span></span>

### <span data-ttu-id="1bcaa-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1bcaa-112">-AccountName</span></span>
<span data-ttu-id="1bcaa-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1bcaa-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1bcaa-114">-ContainerName</span></span>
<span data-ttu-id="1bcaa-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-115">Container name.</span></span>

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

### <span data-ttu-id="1bcaa-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1bcaa-116">-DatabaseName</span></span>
<span data-ttu-id="1bcaa-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-117">Database name.</span></span>

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

### <span data-ttu-id="1bcaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bcaa-118">-DefaultProfile</span></span>
<span data-ttu-id="1bcaa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bcaa-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1bcaa-120">-InputObject</span></span>
<span data-ttu-id="1bcaa-121">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-121">Sql Container object.</span></span>

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

### <span data-ttu-id="1bcaa-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1bcaa-122">-Name</span></span>
<span data-ttu-id="1bcaa-123">Nazwa funkcji zdefiniowana przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-123">User Defined Function Name.</span></span>

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

### <span data-ttu-id="1bcaa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bcaa-124">-ResourceGroupName</span></span>
<span data-ttu-id="1bcaa-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1bcaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bcaa-126">CommonParameters</span></span>
<span data-ttu-id="1bcaa-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bcaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bcaa-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bcaa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bcaa-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bcaa-129">INPUTS</span></span>

### <span data-ttu-id="1bcaa-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1bcaa-130">None</span></span>

## <span data-ttu-id="1bcaa-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bcaa-131">OUTPUTS</span></span>

### <span data-ttu-id="1bcaa-132">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="1bcaa-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="1bcaa-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bcaa-133">NOTES</span></span>

## <span data-ttu-id="1bcaa-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bcaa-134">RELATED LINKS</span></span>
