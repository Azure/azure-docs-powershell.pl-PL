---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177227"
---
# <span data-ttu-id="34919-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="34919-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="34919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34919-102">SYNOPSIS</span></span>
<span data-ttu-id="34919-103">{{ Fill in the Synopsis }}</span><span class="sxs-lookup"><span data-stu-id="34919-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="34919-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34919-104">SYNTAX</span></span>

### <span data-ttu-id="34919-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="34919-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34919-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34919-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34919-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34919-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34919-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="34919-108">DESCRIPTION</span></span>
<span data-ttu-id="34919-109">{{ Wypełnij opis }}</span><span class="sxs-lookup"><span data-stu-id="34919-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="34919-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34919-110">EXAMPLES</span></span>

### <span data-ttu-id="34919-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34919-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="34919-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="34919-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="34919-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34919-113">PARAMETERS</span></span>

### <span data-ttu-id="34919-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="34919-114">-AsJob</span></span>
<span data-ttu-id="34919-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="34919-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34919-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34919-116">-Confirm</span></span>
<span data-ttu-id="34919-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34919-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34919-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34919-118">-DefaultProfile</span></span>
<span data-ttu-id="34919-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34919-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34919-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="34919-120">-FailoverPolicy</span></span>
<span data-ttu-id="34919-121">Tablica ciągów o nazwach regionów uporządkowanych według priorytetu trybu failover.</span><span class="sxs-lookup"><span data-stu-id="34919-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="34919-122">Np. eastus, westus</span><span class="sxs-lookup"><span data-stu-id="34919-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34919-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34919-123">-InputObject</span></span>
<span data-ttu-id="34919-124">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="34919-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34919-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34919-125">-Name</span></span>
<span data-ttu-id="34919-126">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="34919-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34919-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34919-127">-ResourceGroupName</span></span>
<span data-ttu-id="34919-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34919-128">Name of resource group.</span></span>

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

### <span data-ttu-id="34919-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34919-129">-ResourceId</span></span>
<span data-ttu-id="34919-130">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="34919-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34919-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34919-131">-WhatIf</span></span>
<span data-ttu-id="34919-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34919-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34919-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="34919-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34919-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34919-134">CommonParameters</span></span>
<span data-ttu-id="34919-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34919-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34919-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34919-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34919-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34919-137">INPUTS</span></span>

### <span data-ttu-id="34919-138">Brak</span><span class="sxs-lookup"><span data-stu-id="34919-138">None</span></span>

## <span data-ttu-id="34919-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34919-139">OUTPUTS</span></span>

### <span data-ttu-id="34919-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="34919-140">System.Void</span></span>

## <span data-ttu-id="34919-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34919-141">NOTES</span></span>

## <span data-ttu-id="34919-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34919-142">RELATED LINKS</span></span>
