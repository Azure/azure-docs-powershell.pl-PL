---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: d2a4dacb929587fb0f06c002ad26df3144f32f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960794"
---
# <span data-ttu-id="e0a37-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="e0a37-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="e0a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a37-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a37-103">Tworzy nową tabelę OSD.</span><span class="sxs-lookup"><span data-stu-id="e0a37-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="e0a37-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0a37-104">SYNTAX</span></span>

### <span data-ttu-id="e0a37-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e0a37-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0a37-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0a37-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0a37-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0a37-107">DESCRIPTION</span></span>
<span data-ttu-id="e0a37-108">Tworzy nową tabelę OSD.</span><span class="sxs-lookup"><span data-stu-id="e0a37-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="e0a37-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0a37-109">EXAMPLES</span></span>

### <span data-ttu-id="e0a37-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0a37-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="e0a37-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0a37-111">PARAMETERS</span></span>

### <span data-ttu-id="e0a37-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0a37-112">-AccountName</span></span>
<span data-ttu-id="e0a37-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="e0a37-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e0a37-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e0a37-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e0a37-115">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="e0a37-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e0a37-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0a37-116">-Confirm</span></span>
<span data-ttu-id="e0a37-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0a37-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0a37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a37-118">-DefaultProfile</span></span>
<span data-ttu-id="e0a37-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0a37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0a37-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0a37-120">-Name</span></span>
<span data-ttu-id="e0a37-121">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="e0a37-121">Name of the Table.</span></span>

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

### <span data-ttu-id="e0a37-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="e0a37-122">-ParentObject</span></span>
<span data-ttu-id="e0a37-123">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="e0a37-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e0a37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a37-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0a37-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0a37-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e0a37-126">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="e0a37-126">-Throughput</span></span>
<span data-ttu-id="e0a37-127">Przepływność tabel (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e0a37-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="e0a37-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="e0a37-128">Default value is 400.</span></span>

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

### <span data-ttu-id="e0a37-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0a37-129">-WhatIf</span></span>
<span data-ttu-id="e0a37-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0a37-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0a37-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0a37-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0a37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a37-132">CommonParameters</span></span>
<span data-ttu-id="e0a37-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0a37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a37-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0a37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a37-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0a37-135">INPUTS</span></span>

### <span data-ttu-id="e0a37-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e0a37-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e0a37-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0a37-137">OUTPUTS</span></span>

### <span data-ttu-id="e0a37-138">Microsoft.Azure.Commands.Dosdb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="e0a37-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="e0a37-139">Microsoft.Azure.Commands.DoceńDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e0a37-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e0a37-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0a37-140">NOTES</span></span>

## <span data-ttu-id="e0a37-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0a37-141">RELATED LINKS</span></span>
