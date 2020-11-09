---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306817"
---
# <span data-ttu-id="86eb6-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="86eb6-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="86eb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="86eb6-103">Aktualizuje bazę danych Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="86eb6-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="86eb6-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="86eb6-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="86eb6-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86eb6-105">SYNTAX</span></span>

### <span data-ttu-id="86eb6-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="86eb6-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86eb6-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86eb6-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86eb6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86eb6-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86eb6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="86eb6-109">DESCRIPTION</span></span>
<span data-ttu-id="86eb6-110">Aktualizuje bazę danych Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="86eb6-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="86eb6-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="86eb6-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="86eb6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86eb6-112">EXAMPLES</span></span>

### <span data-ttu-id="86eb6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86eb6-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="86eb6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86eb6-114">PARAMETERS</span></span>

### <span data-ttu-id="86eb6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86eb6-115">-AccountName</span></span>
<span data-ttu-id="86eb6-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="86eb6-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="86eb6-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="86eb6-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="86eb6-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="86eb6-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="86eb6-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86eb6-119">-Confirm</span></span>
<span data-ttu-id="86eb6-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86eb6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86eb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86eb6-121">-DefaultProfile</span></span>
<span data-ttu-id="86eb6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86eb6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86eb6-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="86eb6-123">-InputObject</span></span>
<span data-ttu-id="86eb6-124">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="86eb6-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86eb6-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86eb6-125">-Name</span></span>
<span data-ttu-id="86eb6-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="86eb6-126">Database name.</span></span>

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

### <span data-ttu-id="86eb6-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="86eb6-127">-ParentObject</span></span>
<span data-ttu-id="86eb6-128">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="86eb6-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="86eb6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86eb6-129">-ResourceGroupName</span></span>
<span data-ttu-id="86eb6-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86eb6-130">Name of resource group.</span></span>

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

### <span data-ttu-id="86eb6-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="86eb6-131">-Throughput</span></span>
<span data-ttu-id="86eb6-132">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="86eb6-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="86eb6-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="86eb6-133">Default value is 400.</span></span>

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

### <span data-ttu-id="86eb6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86eb6-134">-WhatIf</span></span>
<span data-ttu-id="86eb6-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86eb6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86eb6-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86eb6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86eb6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86eb6-137">CommonParameters</span></span>
<span data-ttu-id="86eb6-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86eb6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86eb6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86eb6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86eb6-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86eb6-140">INPUTS</span></span>

### <span data-ttu-id="86eb6-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="86eb6-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="86eb6-142">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="86eb6-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="86eb6-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86eb6-143">OUTPUTS</span></span>

### <span data-ttu-id="86eb6-144">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="86eb6-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="86eb6-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="86eb6-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="86eb6-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86eb6-146">NOTES</span></span>

## <span data-ttu-id="86eb6-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86eb6-147">RELATED LINKS</span></span>
