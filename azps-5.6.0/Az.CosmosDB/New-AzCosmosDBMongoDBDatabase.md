---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: dd0df6dcaf49ab027585773437785d37940dcd9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978721"
---
# <span data-ttu-id="89b29-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="89b29-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="89b29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b29-102">SYNOPSIS</span></span>
<span data-ttu-id="89b29-103">Tworzy nową bazę danych ADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="89b29-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="89b29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="89b29-104">SYNTAX</span></span>

### <span data-ttu-id="89b29-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="89b29-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89b29-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89b29-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89b29-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="89b29-107">DESCRIPTION</span></span>
<span data-ttu-id="89b29-108">Tworzy nową bazę danych ADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="89b29-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="89b29-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="89b29-109">EXAMPLES</span></span>

### <span data-ttu-id="89b29-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89b29-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="89b29-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89b29-111">PARAMETERS</span></span>

### <span data-ttu-id="89b29-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89b29-112">-AccountName</span></span>
<span data-ttu-id="89b29-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="89b29-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="89b29-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="89b29-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="89b29-115">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="89b29-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="89b29-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89b29-116">-Confirm</span></span>
<span data-ttu-id="89b29-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="89b29-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89b29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b29-118">-DefaultProfile</span></span>
<span data-ttu-id="89b29-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="89b29-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89b29-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="89b29-120">-Name</span></span>
<span data-ttu-id="89b29-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="89b29-121">Database name.</span></span>

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

### <span data-ttu-id="89b29-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="89b29-122">-ParentObject</span></span>
<span data-ttu-id="89b29-123">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="89b29-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="89b29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b29-124">-ResourceGroupName</span></span>
<span data-ttu-id="89b29-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89b29-125">Name of resource group.</span></span>

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

### <span data-ttu-id="89b29-126">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="89b29-126">-Throughput</span></span>
<span data-ttu-id="89b29-127">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="89b29-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="89b29-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="89b29-128">Default value is 400.</span></span>

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

### <span data-ttu-id="89b29-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89b29-129">-WhatIf</span></span>
<span data-ttu-id="89b29-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89b29-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89b29-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="89b29-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89b29-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b29-132">CommonParameters</span></span>
<span data-ttu-id="89b29-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b29-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b29-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89b29-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b29-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89b29-135">INPUTS</span></span>

### <span data-ttu-id="89b29-136">Brak</span><span class="sxs-lookup"><span data-stu-id="89b29-136">None</span></span>

## <span data-ttu-id="89b29-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89b29-137">OUTPUTS</span></span>

### <span data-ttu-id="89b29-138">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="89b29-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="89b29-139">Microsoft.Azure.Commands.DoceńDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="89b29-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="89b29-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="89b29-140">NOTES</span></span>

## <span data-ttu-id="89b29-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89b29-141">RELATED LINKS</span></span>
