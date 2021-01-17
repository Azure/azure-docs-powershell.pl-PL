---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361207"
---
# <span data-ttu-id="88e7d-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="88e7d-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="88e7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="88e7d-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="88e7d-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="88e7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88e7d-104">SYNTAX</span></span>

### <span data-ttu-id="88e7d-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="88e7d-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e7d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88e7d-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e7d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88e7d-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e7d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="88e7d-108">DESCRIPTION</span></span>
<span data-ttu-id="88e7d-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="88e7d-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="88e7d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88e7d-110">EXAMPLES</span></span>

### <span data-ttu-id="88e7d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88e7d-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="88e7d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88e7d-112">PARAMETERS</span></span>

### <span data-ttu-id="88e7d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88e7d-113">-AccountName</span></span>
<span data-ttu-id="88e7d-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="88e7d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="88e7d-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88e7d-115">-Confirm</span></span>
<span data-ttu-id="88e7d-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e7d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e7d-117">-DefaultProfile</span></span>
<span data-ttu-id="88e7d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88e7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e7d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="88e7d-119">-InputObject</span></span>
<span data-ttu-id="88e7d-120">Obiekt Table.</span><span class="sxs-lookup"><span data-stu-id="88e7d-120">Table Object.</span></span>

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

### <span data-ttu-id="88e7d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88e7d-121">-Name</span></span>
<span data-ttu-id="88e7d-122">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="88e7d-122">Name of the Table.</span></span>

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

### <span data-ttu-id="88e7d-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="88e7d-123">-ParentObject</span></span>
<span data-ttu-id="88e7d-124">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="88e7d-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="88e7d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e7d-125">-ResourceGroupName</span></span>
<span data-ttu-id="88e7d-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88e7d-126">Name of resource group.</span></span>

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

### <span data-ttu-id="88e7d-127">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="88e7d-127">-ThroughputType</span></span>
<span data-ttu-id="88e7d-128">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="88e7d-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="88e7d-129">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="88e7d-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="88e7d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e7d-130">-WhatIf</span></span>
<span data-ttu-id="88e7d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e7d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e7d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88e7d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e7d-133">CommonParameters</span></span>
<span data-ttu-id="88e7d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e7d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88e7d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e7d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88e7d-136">INPUTS</span></span>

### <span data-ttu-id="88e7d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="88e7d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="88e7d-138">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="88e7d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="88e7d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88e7d-139">OUTPUTS</span></span>

### <span data-ttu-id="88e7d-140">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="88e7d-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="88e7d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88e7d-141">NOTES</span></span>

## <span data-ttu-id="88e7d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88e7d-142">RELATED LINKS</span></span>
