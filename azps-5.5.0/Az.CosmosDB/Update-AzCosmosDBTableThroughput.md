---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196730"
---
# <span data-ttu-id="a4c71-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="a4c71-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="a4c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4c71-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c71-103">Aktualizuje wartość przepływności tabeli AADB.</span><span class="sxs-lookup"><span data-stu-id="a4c71-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="a4c71-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4c71-104">SYNTAX</span></span>

### <span data-ttu-id="a4c71-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a4c71-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c71-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4c71-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c71-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4c71-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4c71-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4c71-108">DESCRIPTION</span></span>
<span data-ttu-id="a4c71-109">Aktualizuje wartość przepływności tabeli AADB.</span><span class="sxs-lookup"><span data-stu-id="a4c71-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="a4c71-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4c71-110">EXAMPLES</span></span>

### <span data-ttu-id="a4c71-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4c71-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="a4c71-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4c71-112">PARAMETERS</span></span>

### <span data-ttu-id="a4c71-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4c71-113">-AccountName</span></span>
<span data-ttu-id="a4c71-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="a4c71-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a4c71-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a4c71-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a4c71-116">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="a4c71-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a4c71-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4c71-117">-Confirm</span></span>
<span data-ttu-id="a4c71-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4c71-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c71-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c71-119">-DefaultProfile</span></span>
<span data-ttu-id="a4c71-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c71-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4c71-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4c71-121">-InputObject</span></span>
<span data-ttu-id="a4c71-122">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="a4c71-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a4c71-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a4c71-123">-Name</span></span>
<span data-ttu-id="a4c71-124">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="a4c71-124">Name of the Table.</span></span>

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

### <span data-ttu-id="a4c71-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="a4c71-125">-ParentObject</span></span>
<span data-ttu-id="a4c71-126">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="a4c71-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a4c71-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c71-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4c71-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4c71-128">Name of resource group.</span></span>

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

### <span data-ttu-id="a4c71-129">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="a4c71-129">-Throughput</span></span>
<span data-ttu-id="a4c71-130">Przepływność tabel (RU/s).</span><span class="sxs-lookup"><span data-stu-id="a4c71-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="a4c71-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="a4c71-131">Default value is 400.</span></span>

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

### <span data-ttu-id="a4c71-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c71-132">-WhatIf</span></span>
<span data-ttu-id="a4c71-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4c71-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c71-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4c71-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c71-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c71-135">CommonParameters</span></span>
<span data-ttu-id="a4c71-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c71-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c71-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4c71-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c71-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4c71-138">INPUTS</span></span>

### <span data-ttu-id="a4c71-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a4c71-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a4c71-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4c71-140">OUTPUTS</span></span>

### <span data-ttu-id="a4c71-141">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a4c71-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a4c71-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4c71-142">NOTES</span></span>

## <span data-ttu-id="a4c71-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4c71-143">RELATED LINKS</span></span>
