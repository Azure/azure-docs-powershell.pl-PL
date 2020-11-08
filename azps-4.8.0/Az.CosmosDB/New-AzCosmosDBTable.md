---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221529"
---
# <span data-ttu-id="50724-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="50724-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="50724-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50724-102">SYNOPSIS</span></span>
<span data-ttu-id="50724-103">Tworzy nową tabelę CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="50724-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="50724-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50724-104">SYNTAX</span></span>

### <span data-ttu-id="50724-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="50724-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50724-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50724-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50724-107">Opis</span><span class="sxs-lookup"><span data-stu-id="50724-107">DESCRIPTION</span></span>
<span data-ttu-id="50724-108">Tworzy nową tabelę CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="50724-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="50724-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50724-109">EXAMPLES</span></span>

### <span data-ttu-id="50724-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50724-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="50724-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50724-111">PARAMETERS</span></span>

### <span data-ttu-id="50724-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50724-112">-AccountName</span></span>
<span data-ttu-id="50724-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="50724-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="50724-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="50724-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="50724-115">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="50724-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="50724-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50724-116">-Confirm</span></span>
<span data-ttu-id="50724-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50724-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50724-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50724-118">-DefaultProfile</span></span>
<span data-ttu-id="50724-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50724-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50724-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50724-120">-Name</span></span>
<span data-ttu-id="50724-121">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="50724-121">Name of the Table.</span></span>

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

### <span data-ttu-id="50724-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="50724-122">-ParentObject</span></span>
<span data-ttu-id="50724-123">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="50724-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="50724-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50724-124">-ResourceGroupName</span></span>
<span data-ttu-id="50724-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50724-125">Name of resource group.</span></span>

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

### <span data-ttu-id="50724-126">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="50724-126">-Throughput</span></span>
<span data-ttu-id="50724-127">Przepływność tabeli (RU/s).</span><span class="sxs-lookup"><span data-stu-id="50724-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="50724-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="50724-128">Default value is 400.</span></span>

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

### <span data-ttu-id="50724-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50724-129">-WhatIf</span></span>
<span data-ttu-id="50724-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50724-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50724-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50724-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50724-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50724-132">CommonParameters</span></span>
<span data-ttu-id="50724-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50724-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50724-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50724-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50724-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50724-135">INPUTS</span></span>

### <span data-ttu-id="50724-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="50724-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="50724-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50724-137">OUTPUTS</span></span>

### <span data-ttu-id="50724-138">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="50724-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="50724-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="50724-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="50724-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50724-140">NOTES</span></span>

## <span data-ttu-id="50724-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50724-141">RELATED LINKS</span></span>
