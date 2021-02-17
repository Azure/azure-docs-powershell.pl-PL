---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 7b30582e0a55e65009fa7248c61cd36f32393249
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196851"
---
# <span data-ttu-id="3c0a1-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="3c0a1-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="3c0a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0a1-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="3c0a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c0a1-104">SYNTAX</span></span>

### <span data-ttu-id="3c0a1-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3c0a1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c0a1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0a1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0a1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0a1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c0a1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c0a1-108">DESCRIPTION</span></span>
<span data-ttu-id="3c0a1-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="3c0a1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c0a1-110">EXAMPLES</span></span>

### <span data-ttu-id="3c0a1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c0a1-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="3c0a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c0a1-112">PARAMETERS</span></span>

### <span data-ttu-id="3c0a1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3c0a1-113">-AccountName</span></span>
<span data-ttu-id="3c0a1-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3c0a1-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c0a1-115">-Confirm</span></span>
<span data-ttu-id="3c0a1-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c0a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0a1-117">-DefaultProfile</span></span>
<span data-ttu-id="3c0a1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c0a1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c0a1-119">-InputObject</span></span>
<span data-ttu-id="3c0a1-120">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="3c0a1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3c0a1-121">-Name</span></span>
<span data-ttu-id="3c0a1-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-122">Database name.</span></span>

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

### <span data-ttu-id="3c0a1-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="3c0a1-123">-ParentObject</span></span>
<span data-ttu-id="3c0a1-124">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="3c0a1-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3c0a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c0a1-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-126">Name of resource group.</span></span>

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

### <span data-ttu-id="3c0a1-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="3c0a1-127">-ThroughputType</span></span>
<span data-ttu-id="3c0a1-128">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="3c0a1-129">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="3c0a1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c0a1-130">-WhatIf</span></span>
<span data-ttu-id="3c0a1-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c0a1-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c0a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0a1-133">CommonParameters</span></span>
<span data-ttu-id="3c0a1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0a1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c0a1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0a1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c0a1-136">INPUTS</span></span>

### <span data-ttu-id="3c0a1-137">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3c0a1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3c0a1-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c0a1-138">OUTPUTS</span></span>

### <span data-ttu-id="3c0a1-139">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3c0a1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3c0a1-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c0a1-140">NOTES</span></span>

## <span data-ttu-id="3c0a1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c0a1-141">RELATED LINKS</span></span>
