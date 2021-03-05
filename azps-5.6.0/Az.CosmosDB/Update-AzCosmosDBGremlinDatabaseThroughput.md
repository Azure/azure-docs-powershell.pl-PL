---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 21dd30bd60e9b26fc306ed99b31cd3c52d9fdf8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977345"
---
# <span data-ttu-id="09599-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="09599-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="09599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09599-102">SYNOPSIS</span></span>
<span data-ttu-id="09599-103">Aktualizuje wartość przepływności dla bazy danych GremlinDb.</span><span class="sxs-lookup"><span data-stu-id="09599-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="09599-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09599-104">SYNTAX</span></span>

### <span data-ttu-id="09599-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="09599-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09599-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09599-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09599-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09599-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09599-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="09599-108">DESCRIPTION</span></span>
<span data-ttu-id="09599-109">Aktualizuje wartość przepływności dla bazy danych GremlinDb.</span><span class="sxs-lookup"><span data-stu-id="09599-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="09599-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09599-110">EXAMPLES</span></span>

### <span data-ttu-id="09599-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09599-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="09599-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09599-112">PARAMETERS</span></span>

### <span data-ttu-id="09599-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09599-113">-AccountName</span></span>
<span data-ttu-id="09599-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="09599-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09599-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="09599-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="09599-116">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="09599-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09599-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09599-117">-Confirm</span></span>
<span data-ttu-id="09599-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09599-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09599-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09599-119">-DefaultProfile</span></span>
<span data-ttu-id="09599-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09599-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09599-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09599-121">-InputObject</span></span>
<span data-ttu-id="09599-122">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="09599-122">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09599-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09599-123">-Name</span></span>
<span data-ttu-id="09599-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="09599-124">Database name.</span></span>

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

### <span data-ttu-id="09599-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="09599-125">-ParentObject</span></span>
<span data-ttu-id="09599-126">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="09599-126">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09599-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09599-127">-ResourceGroupName</span></span>
<span data-ttu-id="09599-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09599-128">Name of resource group.</span></span>

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

### <span data-ttu-id="09599-129">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="09599-129">-Throughput</span></span>
<span data-ttu-id="09599-130">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="09599-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="09599-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="09599-131">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09599-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09599-132">-WhatIf</span></span>
<span data-ttu-id="09599-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09599-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09599-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="09599-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09599-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09599-135">CommonParameters</span></span>
<span data-ttu-id="09599-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09599-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09599-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09599-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09599-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09599-138">INPUTS</span></span>

### <span data-ttu-id="09599-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="09599-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="09599-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09599-140">OUTPUTS</span></span>

### <span data-ttu-id="09599-141">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="09599-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="09599-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09599-142">NOTES</span></span>

## <span data-ttu-id="09599-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09599-143">RELATED LINKS</span></span>
