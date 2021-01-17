---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372883"
---
# <span data-ttu-id="98d30-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="98d30-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="98d30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98d30-102">SYNOPSIS</span></span>
<span data-ttu-id="98d30-103">Umożliwia zaktualizowanie tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="98d30-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="98d30-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="98d30-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="98d30-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98d30-105">SYNTAX</span></span>

### <span data-ttu-id="98d30-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98d30-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98d30-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98d30-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98d30-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98d30-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98d30-109">Opis</span><span class="sxs-lookup"><span data-stu-id="98d30-109">DESCRIPTION</span></span>
<span data-ttu-id="98d30-110">Umożliwia zaktualizowanie tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="98d30-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="98d30-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="98d30-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="98d30-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98d30-112">EXAMPLES</span></span>

### <span data-ttu-id="98d30-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98d30-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="98d30-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98d30-114">PARAMETERS</span></span>

### <span data-ttu-id="98d30-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98d30-115">-AccountName</span></span>
<span data-ttu-id="98d30-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="98d30-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="98d30-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="98d30-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="98d30-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="98d30-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="98d30-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98d30-119">-Confirm</span></span>
<span data-ttu-id="98d30-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d30-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d30-121">-DefaultProfile</span></span>
<span data-ttu-id="98d30-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98d30-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98d30-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98d30-123">-InputObject</span></span>
<span data-ttu-id="98d30-124">Obiekt Table.</span><span class="sxs-lookup"><span data-stu-id="98d30-124">Table Object.</span></span>

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

### <span data-ttu-id="98d30-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98d30-125">-Name</span></span>
<span data-ttu-id="98d30-126">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="98d30-126">Name of the Table.</span></span>

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

### <span data-ttu-id="98d30-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="98d30-127">-ParentObject</span></span>
<span data-ttu-id="98d30-128">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="98d30-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="98d30-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d30-129">-ResourceGroupName</span></span>
<span data-ttu-id="98d30-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98d30-130">Name of resource group.</span></span>

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

### <span data-ttu-id="98d30-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="98d30-131">-Throughput</span></span>
<span data-ttu-id="98d30-132">Przepływność tabeli (RU/s).</span><span class="sxs-lookup"><span data-stu-id="98d30-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="98d30-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="98d30-133">Default value is 400.</span></span>

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

### <span data-ttu-id="98d30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d30-134">-WhatIf</span></span>
<span data-ttu-id="98d30-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98d30-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98d30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d30-137">CommonParameters</span></span>
<span data-ttu-id="98d30-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d30-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98d30-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d30-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98d30-140">INPUTS</span></span>

### <span data-ttu-id="98d30-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="98d30-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="98d30-142">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="98d30-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="98d30-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98d30-143">OUTPUTS</span></span>

### <span data-ttu-id="98d30-144">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="98d30-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="98d30-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="98d30-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="98d30-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98d30-146">NOTES</span></span>

## <span data-ttu-id="98d30-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98d30-147">RELATED LINKS</span></span>
