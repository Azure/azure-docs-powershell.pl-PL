---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894298"
---
# <span data-ttu-id="9d4f2-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="9d4f2-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="9d4f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4f2-103">Tworzy nową lub aktualizuje istniejące CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="9d4f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d4f2-104">SYNTAX</span></span>

### <span data-ttu-id="9d4f2-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d4f2-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d4f2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d4f2-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d4f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d4f2-107">DESCRIPTION</span></span>
<span data-ttu-id="9d4f2-108">Polecenie cmdlet **Set-AzCosmosDBSqlUserDefinedFunction** tworzy nowy lub aktualizuje istniejące CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="9d4f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d4f2-109">EXAMPLES</span></span>

### <span data-ttu-id="9d4f2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d4f2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="9d4f2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d4f2-111">PARAMETERS</span></span>

### <span data-ttu-id="9d4f2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9d4f2-112">-AccountName</span></span>
<span data-ttu-id="9d4f2-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9d4f2-114">-Body</span><span class="sxs-lookup"><span data-stu-id="9d4f2-114">-Body</span></span>
<span data-ttu-id="9d4f2-115">Treść funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-115">The body of the User Defined Function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4f2-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d4f2-116">-Confirm</span></span>
<span data-ttu-id="9d4f2-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4f2-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9d4f2-118">-ContainerName</span></span>
<span data-ttu-id="9d4f2-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-119">Container name.</span></span>

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

### <span data-ttu-id="9d4f2-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9d4f2-120">-DatabaseName</span></span>
<span data-ttu-id="9d4f2-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-121">Database name.</span></span>

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

### <span data-ttu-id="9d4f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4f2-122">-DefaultProfile</span></span>
<span data-ttu-id="9d4f2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d4f2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d4f2-124">-InputObject</span></span>
<span data-ttu-id="9d4f2-125">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-125">Sql Container object.</span></span>

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

### <span data-ttu-id="9d4f2-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d4f2-126">-Name</span></span>
<span data-ttu-id="9d4f2-127">Nazwa funkcji zdefiniowana przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-127">User Defined Function Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4f2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d4f2-128">-ResourceGroupName</span></span>
<span data-ttu-id="9d4f2-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-129">Name of resource group.</span></span>

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

### <span data-ttu-id="9d4f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d4f2-130">-WhatIf</span></span>
<span data-ttu-id="9d4f2-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d4f2-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4f2-133">CommonParameters</span></span>
<span data-ttu-id="9d4f2-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d4f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4f2-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d4f2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4f2-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d4f2-136">INPUTS</span></span>

### <span data-ttu-id="9d4f2-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d4f2-137">None</span></span>

## <span data-ttu-id="9d4f2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d4f2-138">OUTPUTS</span></span>

### <span data-ttu-id="9d4f2-139">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="9d4f2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="9d4f2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d4f2-140">NOTES</span></span>

## <span data-ttu-id="9d4f2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d4f2-141">RELATED LINKS</span></span>
