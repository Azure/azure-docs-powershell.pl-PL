---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 879cf737553ea082c99a2cdf8d6bff8e8734e595
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177306"
---
# <span data-ttu-id="f12ca-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="f12ca-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="f12ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f12ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f12ca-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="f12ca-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="f12ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f12ca-104">SYNTAX</span></span>

### <span data-ttu-id="f12ca-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f12ca-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f12ca-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f12ca-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f12ca-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f12ca-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f12ca-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f12ca-108">DESCRIPTION</span></span>
<span data-ttu-id="f12ca-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="f12ca-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="f12ca-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f12ca-110">EXAMPLES</span></span>

### <span data-ttu-id="f12ca-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f12ca-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="f12ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f12ca-112">PARAMETERS</span></span>

### <span data-ttu-id="f12ca-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f12ca-113">-AccountName</span></span>
<span data-ttu-id="f12ca-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="f12ca-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f12ca-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f12ca-115">-Confirm</span></span>
<span data-ttu-id="f12ca-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f12ca-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f12ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12ca-117">-DefaultProfile</span></span>
<span data-ttu-id="f12ca-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f12ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f12ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f12ca-119">-InputObject</span></span>
<span data-ttu-id="f12ca-120">Obiekt Table.</span><span class="sxs-lookup"><span data-stu-id="f12ca-120">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f12ca-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f12ca-121">-Name</span></span>
<span data-ttu-id="f12ca-122">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="f12ca-122">Name of the Table.</span></span>

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

### <span data-ttu-id="f12ca-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="f12ca-123">-ParentObject</span></span>
<span data-ttu-id="f12ca-124">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="f12ca-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f12ca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f12ca-125">-ResourceGroupName</span></span>
<span data-ttu-id="f12ca-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f12ca-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f12ca-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="f12ca-127">-ThroughputType</span></span>
<span data-ttu-id="f12ca-128">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="f12ca-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="f12ca-129">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="f12ca-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="f12ca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f12ca-130">-WhatIf</span></span>
<span data-ttu-id="f12ca-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12ca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f12ca-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f12ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f12ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12ca-133">CommonParameters</span></span>
<span data-ttu-id="f12ca-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f12ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12ca-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f12ca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12ca-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f12ca-136">INPUTS</span></span>

### <span data-ttu-id="f12ca-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="f12ca-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="f12ca-138">Microsoft.Azure.Commands.Dosdb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f12ca-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="f12ca-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f12ca-139">OUTPUTS</span></span>

### <span data-ttu-id="f12ca-140">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f12ca-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f12ca-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f12ca-141">NOTES</span></span>

## <span data-ttu-id="f12ca-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f12ca-142">RELATED LINKS</span></span>
