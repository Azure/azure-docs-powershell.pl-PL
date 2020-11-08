---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049517"
---
# <span data-ttu-id="4a0e9-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="4a0e9-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="4a0e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0e9-103">Tworzy nową lub aktualizuje istniejące CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="4a0e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a0e9-104">SYNTAX</span></span>

### <span data-ttu-id="4a0e9-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a0e9-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a0e9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a0e9-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a0e9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4a0e9-107">DESCRIPTION</span></span>
<span data-ttu-id="4a0e9-108">Polecenie cmdlet **Set-AzCosmosDBSqlStoredProcedure** tworzy nowy lub aktualizuje istniejące CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="4a0e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a0e9-109">EXAMPLES</span></span>

### <span data-ttu-id="4a0e9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a0e9-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="4a0e9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a0e9-111">PARAMETERS</span></span>

### <span data-ttu-id="4a0e9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a0e9-112">-AccountName</span></span>
<span data-ttu-id="4a0e9-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4a0e9-114">-Body</span><span class="sxs-lookup"><span data-stu-id="4a0e9-114">-Body</span></span>
<span data-ttu-id="4a0e9-115">Treść procedury składowanej.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="4a0e9-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a0e9-116">-Confirm</span></span>
<span data-ttu-id="4a0e9-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a0e9-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4a0e9-118">-ContainerName</span></span>
<span data-ttu-id="4a0e9-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-119">Container name.</span></span>

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

### <span data-ttu-id="4a0e9-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a0e9-120">-DatabaseName</span></span>
<span data-ttu-id="4a0e9-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-121">Database name.</span></span>

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

### <span data-ttu-id="4a0e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0e9-122">-DefaultProfile</span></span>
<span data-ttu-id="4a0e9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a0e9-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a0e9-124">-InputObject</span></span>
<span data-ttu-id="4a0e9-125">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-125">Sql Container object.</span></span>

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

### <span data-ttu-id="4a0e9-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a0e9-126">-Name</span></span>
<span data-ttu-id="4a0e9-127">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="4a0e9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a0e9-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a0e9-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-129">Name of resource group.</span></span>

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

### <span data-ttu-id="4a0e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a0e9-130">-WhatIf</span></span>
<span data-ttu-id="4a0e9-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a0e9-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a0e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0e9-133">CommonParameters</span></span>
<span data-ttu-id="4a0e9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0e9-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a0e9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0e9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a0e9-136">INPUTS</span></span>

### <span data-ttu-id="4a0e9-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4a0e9-137">None</span></span>

## <span data-ttu-id="4a0e9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a0e9-138">OUTPUTS</span></span>

### <span data-ttu-id="4a0e9-139">Microsoft. Azure. Commands. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="4a0e9-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="4a0e9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a0e9-140">NOTES</span></span>

## <span data-ttu-id="4a0e9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a0e9-141">RELATED LINKS</span></span>
