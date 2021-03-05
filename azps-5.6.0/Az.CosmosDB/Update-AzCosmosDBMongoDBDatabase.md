---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: dbffec52b5c1b30f6b00febbc2e6c952beda669e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977290"
---
# <span data-ttu-id="26f42-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="26f42-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="26f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f42-102">SYNOPSIS</span></span>
<span data-ttu-id="26f42-103">Aktualizuje bazę danych DosDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="26f42-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="26f42-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="26f42-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="26f42-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26f42-105">SYNTAX</span></span>

### <span data-ttu-id="26f42-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="26f42-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f42-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f42-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26f42-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f42-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26f42-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="26f42-109">DESCRIPTION</span></span>
<span data-ttu-id="26f42-110">Aktualizuje bazę danych DosDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="26f42-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="26f42-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="26f42-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="26f42-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26f42-112">EXAMPLES</span></span>

### <span data-ttu-id="26f42-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26f42-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="26f42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26f42-114">PARAMETERS</span></span>

### <span data-ttu-id="26f42-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26f42-115">-AccountName</span></span>
<span data-ttu-id="26f42-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="26f42-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26f42-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="26f42-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="26f42-118">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="26f42-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="26f42-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26f42-119">-Confirm</span></span>
<span data-ttu-id="26f42-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26f42-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f42-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f42-121">-DefaultProfile</span></span>
<span data-ttu-id="26f42-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26f42-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f42-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26f42-123">-InputObject</span></span>
<span data-ttu-id="26f42-124">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="26f42-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f42-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="26f42-125">-Name</span></span>
<span data-ttu-id="26f42-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="26f42-126">Database name.</span></span>

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

### <span data-ttu-id="26f42-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="26f42-127">-ParentObject</span></span>
<span data-ttu-id="26f42-128">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="26f42-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="26f42-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f42-129">-ResourceGroupName</span></span>
<span data-ttu-id="26f42-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26f42-130">Name of resource group.</span></span>

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

### <span data-ttu-id="26f42-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="26f42-131">-Throughput</span></span>
<span data-ttu-id="26f42-132">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="26f42-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="26f42-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="26f42-133">Default value is 400.</span></span>

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

### <span data-ttu-id="26f42-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f42-134">-WhatIf</span></span>
<span data-ttu-id="26f42-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26f42-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f42-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26f42-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f42-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f42-137">CommonParameters</span></span>
<span data-ttu-id="26f42-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f42-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f42-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26f42-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f42-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26f42-140">INPUTS</span></span>

### <span data-ttu-id="26f42-141">Brak</span><span class="sxs-lookup"><span data-stu-id="26f42-141">None</span></span>

## <span data-ttu-id="26f42-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26f42-142">OUTPUTS</span></span>

### <span data-ttu-id="26f42-143">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="26f42-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="26f42-144">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="26f42-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="26f42-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26f42-145">NOTES</span></span>

## <span data-ttu-id="26f42-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26f42-146">RELATED LINKS</span></span>
