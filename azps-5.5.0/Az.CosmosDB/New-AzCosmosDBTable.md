---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238500"
---
# <span data-ttu-id="642de-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="642de-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="642de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="642de-102">SYNOPSIS</span></span>
<span data-ttu-id="642de-103">Tworzy nową tabelę OSD.</span><span class="sxs-lookup"><span data-stu-id="642de-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="642de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="642de-104">SYNTAX</span></span>

### <span data-ttu-id="642de-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="642de-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="642de-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="642de-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="642de-107">DESCRIPTION</span></span>
<span data-ttu-id="642de-108">Tworzy nową tabelę OSD.</span><span class="sxs-lookup"><span data-stu-id="642de-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="642de-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="642de-109">EXAMPLES</span></span>

### <span data-ttu-id="642de-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="642de-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="642de-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="642de-111">PARAMETERS</span></span>

### <span data-ttu-id="642de-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="642de-112">-AccountName</span></span>
<span data-ttu-id="642de-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="642de-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="642de-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="642de-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="642de-115">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="642de-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="642de-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="642de-116">-Confirm</span></span>
<span data-ttu-id="642de-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="642de-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642de-118">-DefaultProfile</span></span>
<span data-ttu-id="642de-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="642de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="642de-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="642de-120">-Name</span></span>
<span data-ttu-id="642de-121">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="642de-121">Name of the Table.</span></span>

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

### <span data-ttu-id="642de-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="642de-122">-ParentObject</span></span>
<span data-ttu-id="642de-123">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="642de-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="642de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642de-124">-ResourceGroupName</span></span>
<span data-ttu-id="642de-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="642de-125">Name of resource group.</span></span>

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

### <span data-ttu-id="642de-126">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="642de-126">-Throughput</span></span>
<span data-ttu-id="642de-127">Przepływność tabel (RU/s).</span><span class="sxs-lookup"><span data-stu-id="642de-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="642de-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="642de-128">Default value is 400.</span></span>

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

### <span data-ttu-id="642de-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642de-129">-WhatIf</span></span>
<span data-ttu-id="642de-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="642de-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="642de-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="642de-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642de-132">CommonParameters</span></span>
<span data-ttu-id="642de-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="642de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642de-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="642de-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642de-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="642de-135">INPUTS</span></span>

### <span data-ttu-id="642de-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="642de-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="642de-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="642de-137">OUTPUTS</span></span>

### <span data-ttu-id="642de-138">Microsoft.Azure.Commands.Dosdb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="642de-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="642de-139">Microsoft.Azure.Commands.DoceńDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="642de-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="642de-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="642de-140">NOTES</span></span>

## <span data-ttu-id="642de-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="642de-141">RELATED LINKS</span></span>
