---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196723"
---
# <span data-ttu-id="49b50-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="49b50-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="49b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b50-102">SYNOPSIS</span></span>
<span data-ttu-id="49b50-103">Aktualizuje tabelę GrysDB.</span><span class="sxs-lookup"><span data-stu-id="49b50-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="49b50-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="49b50-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="49b50-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49b50-105">SYNTAX</span></span>

### <span data-ttu-id="49b50-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="49b50-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49b50-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b50-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49b50-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b50-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49b50-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="49b50-109">DESCRIPTION</span></span>
<span data-ttu-id="49b50-110">Aktualizuje tabelę GrysDB.</span><span class="sxs-lookup"><span data-stu-id="49b50-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="49b50-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="49b50-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="49b50-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49b50-112">EXAMPLES</span></span>

### <span data-ttu-id="49b50-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49b50-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="49b50-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b50-114">PARAMETERS</span></span>

### <span data-ttu-id="49b50-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49b50-115">-AccountName</span></span>
<span data-ttu-id="49b50-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="49b50-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="49b50-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="49b50-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="49b50-118">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="49b50-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="49b50-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49b50-119">-Confirm</span></span>
<span data-ttu-id="49b50-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49b50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b50-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b50-121">-DefaultProfile</span></span>
<span data-ttu-id="49b50-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49b50-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b50-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49b50-123">-InputObject</span></span>
<span data-ttu-id="49b50-124">Obiekt Table.</span><span class="sxs-lookup"><span data-stu-id="49b50-124">Table Object.</span></span>

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

### <span data-ttu-id="49b50-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49b50-125">-Name</span></span>
<span data-ttu-id="49b50-126">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="49b50-126">Name of the Table.</span></span>

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

### <span data-ttu-id="49b50-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="49b50-127">-ParentObject</span></span>
<span data-ttu-id="49b50-128">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="49b50-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="49b50-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b50-129">-ResourceGroupName</span></span>
<span data-ttu-id="49b50-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49b50-130">Name of resource group.</span></span>

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

### <span data-ttu-id="49b50-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="49b50-131">-Throughput</span></span>
<span data-ttu-id="49b50-132">Przepływność tabel (RU/s).</span><span class="sxs-lookup"><span data-stu-id="49b50-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="49b50-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="49b50-133">Default value is 400.</span></span>

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

### <span data-ttu-id="49b50-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b50-134">-WhatIf</span></span>
<span data-ttu-id="49b50-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b50-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b50-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49b50-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b50-137">CommonParameters</span></span>
<span data-ttu-id="49b50-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b50-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49b50-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b50-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49b50-140">INPUTS</span></span>

### <span data-ttu-id="49b50-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="49b50-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="49b50-142">Microsoft.Azure.Commands.Dosdb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="49b50-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="49b50-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49b50-143">OUTPUTS</span></span>

### <span data-ttu-id="49b50-144">Microsoft.Azure.Commands.Dosdb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="49b50-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="49b50-145">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="49b50-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="49b50-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49b50-146">NOTES</span></span>

## <span data-ttu-id="49b50-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49b50-147">RELATED LINKS</span></span>
