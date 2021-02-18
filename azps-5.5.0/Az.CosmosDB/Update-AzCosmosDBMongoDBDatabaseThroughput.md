---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1948bc5b5488c951861509c9b3c9ee7815eddec9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181243"
---
# <span data-ttu-id="48e38-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="48e38-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="48e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48e38-102">SYNOPSIS</span></span>
<span data-ttu-id="48e38-103">Aktualizuje wartość przepływności bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="48e38-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="48e38-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48e38-104">SYNTAX</span></span>

### <span data-ttu-id="48e38-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="48e38-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e38-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e38-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e38-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e38-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48e38-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="48e38-108">DESCRIPTION</span></span>
<span data-ttu-id="48e38-109">Aktualizuje wartość przepływności bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="48e38-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="48e38-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48e38-110">EXAMPLES</span></span>

### <span data-ttu-id="48e38-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48e38-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="48e38-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48e38-112">PARAMETERS</span></span>

### <span data-ttu-id="48e38-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48e38-113">-AccountName</span></span>
<span data-ttu-id="48e38-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="48e38-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="48e38-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="48e38-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="48e38-116">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="48e38-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="48e38-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48e38-117">-Confirm</span></span>
<span data-ttu-id="48e38-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48e38-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48e38-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e38-119">-DefaultProfile</span></span>
<span data-ttu-id="48e38-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48e38-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48e38-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48e38-121">-InputObject</span></span>
<span data-ttu-id="48e38-122">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="48e38-122">CosmosDB Account object</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48e38-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="48e38-123">-Name</span></span>
<span data-ttu-id="48e38-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="48e38-124">Database name.</span></span>

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

### <span data-ttu-id="48e38-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="48e38-125">-ParentObject</span></span>
<span data-ttu-id="48e38-126">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="48e38-126">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e38-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e38-127">-ResourceGroupName</span></span>
<span data-ttu-id="48e38-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48e38-128">Name of resource group.</span></span>

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

### <span data-ttu-id="48e38-129">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="48e38-129">-Throughput</span></span>
<span data-ttu-id="48e38-130">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="48e38-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="48e38-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="48e38-131">Default value is 400.</span></span>

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

### <span data-ttu-id="48e38-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e38-132">-WhatIf</span></span>
<span data-ttu-id="48e38-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48e38-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e38-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="48e38-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48e38-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e38-135">CommonParameters</span></span>
<span data-ttu-id="48e38-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e38-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e38-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48e38-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e38-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48e38-138">INPUTS</span></span>

### <span data-ttu-id="48e38-139">Brak</span><span class="sxs-lookup"><span data-stu-id="48e38-139">None</span></span>

## <span data-ttu-id="48e38-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48e38-140">OUTPUTS</span></span>

### <span data-ttu-id="48e38-141">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="48e38-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="48e38-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48e38-142">NOTES</span></span>

## <span data-ttu-id="48e38-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48e38-143">RELATED LINKS</span></span>
