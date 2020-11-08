---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062846"
---
# <span data-ttu-id="85957-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="85957-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="85957-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85957-102">SYNOPSIS</span></span>
<span data-ttu-id="85957-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="85957-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="85957-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85957-104">SYNTAX</span></span>

### <span data-ttu-id="85957-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85957-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85957-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85957-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85957-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85957-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85957-108">Opis</span><span class="sxs-lookup"><span data-stu-id="85957-108">DESCRIPTION</span></span>
<span data-ttu-id="85957-109">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="85957-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="85957-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85957-110">EXAMPLES</span></span>

### <span data-ttu-id="85957-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85957-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="85957-112">FailoverPolicies zaktualizowany przy użyciu Region1 jako FailoverPriority 1, region2 jako FailoverPriority 2 i region3 jako FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="85957-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="85957-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85957-113">PARAMETERS</span></span>

### <span data-ttu-id="85957-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85957-114">-AsJob</span></span>
<span data-ttu-id="85957-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="85957-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85957-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85957-116">-Confirm</span></span>
<span data-ttu-id="85957-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85957-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85957-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85957-118">-DefaultProfile</span></span>
<span data-ttu-id="85957-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85957-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85957-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="85957-120">-FailoverPolicy</span></span>
<span data-ttu-id="85957-121">Tablica ciągów o nazwach regionów uporządkowanych według priorytetu pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="85957-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="85957-122">Na przykład wschód, zachód</span><span class="sxs-lookup"><span data-stu-id="85957-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="85957-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85957-123">-InputObject</span></span>
<span data-ttu-id="85957-124">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="85957-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="85957-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85957-125">-Name</span></span>
<span data-ttu-id="85957-126">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="85957-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="85957-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85957-127">-ResourceGroupName</span></span>
<span data-ttu-id="85957-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85957-128">Name of resource group.</span></span>

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

### <span data-ttu-id="85957-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85957-129">-ResourceId</span></span>
<span data-ttu-id="85957-130">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="85957-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="85957-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85957-131">-WhatIf</span></span>
<span data-ttu-id="85957-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85957-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85957-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85957-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85957-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85957-134">CommonParameters</span></span>
<span data-ttu-id="85957-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85957-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85957-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85957-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85957-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85957-137">INPUTS</span></span>

### <span data-ttu-id="85957-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85957-138">None</span></span>

## <span data-ttu-id="85957-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85957-139">OUTPUTS</span></span>

### <span data-ttu-id="85957-140">System. void</span><span class="sxs-lookup"><span data-stu-id="85957-140">System.Void</span></span>

## <span data-ttu-id="85957-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85957-141">NOTES</span></span>

## <span data-ttu-id="85957-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85957-142">RELATED LINKS</span></span>
