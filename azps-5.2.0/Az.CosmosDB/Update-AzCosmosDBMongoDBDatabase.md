---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363153"
---
# <span data-ttu-id="3747d-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="3747d-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="3747d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3747d-102">SYNOPSIS</span></span>
<span data-ttu-id="3747d-103">Aktualizuje bazę danych MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3747d-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="3747d-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="3747d-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="3747d-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3747d-105">SYNTAX</span></span>

### <span data-ttu-id="3747d-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3747d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3747d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3747d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3747d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3747d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3747d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3747d-109">DESCRIPTION</span></span>
<span data-ttu-id="3747d-110">Aktualizuje bazę danych MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3747d-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="3747d-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="3747d-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="3747d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3747d-112">EXAMPLES</span></span>

### <span data-ttu-id="3747d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3747d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="3747d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3747d-114">PARAMETERS</span></span>

### <span data-ttu-id="3747d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3747d-115">-AccountName</span></span>
<span data-ttu-id="3747d-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3747d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3747d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3747d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3747d-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="3747d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3747d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3747d-119">-Confirm</span></span>
<span data-ttu-id="3747d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3747d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3747d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3747d-121">-DefaultProfile</span></span>
<span data-ttu-id="3747d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3747d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3747d-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3747d-123">-InputObject</span></span>
<span data-ttu-id="3747d-124">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="3747d-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3747d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3747d-125">-Name</span></span>
<span data-ttu-id="3747d-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3747d-126">Database name.</span></span>

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

### <span data-ttu-id="3747d-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3747d-127">-ParentObject</span></span>
<span data-ttu-id="3747d-128">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="3747d-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3747d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3747d-129">-ResourceGroupName</span></span>
<span data-ttu-id="3747d-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3747d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="3747d-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="3747d-131">-Throughput</span></span>
<span data-ttu-id="3747d-132">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="3747d-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="3747d-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="3747d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="3747d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3747d-134">-WhatIf</span></span>
<span data-ttu-id="3747d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3747d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3747d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3747d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3747d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3747d-137">CommonParameters</span></span>
<span data-ttu-id="3747d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3747d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3747d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3747d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3747d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3747d-140">INPUTS</span></span>

### <span data-ttu-id="3747d-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3747d-141">None</span></span>

## <span data-ttu-id="3747d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3747d-142">OUTPUTS</span></span>

### <span data-ttu-id="3747d-143">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3747d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="3747d-144">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="3747d-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="3747d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3747d-145">NOTES</span></span>

## <span data-ttu-id="3747d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3747d-146">RELATED LINKS</span></span>
