---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503782"
---
# <span data-ttu-id="81678-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="81678-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="81678-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81678-102">SYNOPSIS</span></span>
<span data-ttu-id="81678-103">Aktualizuje bazę danych MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="81678-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="81678-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="81678-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="81678-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81678-105">SYNTAX</span></span>

### <span data-ttu-id="81678-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="81678-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81678-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81678-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81678-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81678-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81678-109">Opis</span><span class="sxs-lookup"><span data-stu-id="81678-109">DESCRIPTION</span></span>
<span data-ttu-id="81678-110">Aktualizuje bazę danych MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="81678-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="81678-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="81678-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="81678-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81678-112">EXAMPLES</span></span>

### <span data-ttu-id="81678-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81678-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="81678-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81678-114">PARAMETERS</span></span>

### <span data-ttu-id="81678-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81678-115">-AccountName</span></span>
<span data-ttu-id="81678-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="81678-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81678-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="81678-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="81678-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="81678-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="81678-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81678-119">-Confirm</span></span>
<span data-ttu-id="81678-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81678-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81678-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81678-121">-DefaultProfile</span></span>
<span data-ttu-id="81678-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81678-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81678-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81678-123">-InputObject</span></span>
<span data-ttu-id="81678-124">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="81678-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="81678-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81678-125">-Name</span></span>
<span data-ttu-id="81678-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="81678-126">Database name.</span></span>

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

### <span data-ttu-id="81678-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="81678-127">-ParentObject</span></span>
<span data-ttu-id="81678-128">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="81678-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="81678-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81678-129">-ResourceGroupName</span></span>
<span data-ttu-id="81678-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81678-130">Name of resource group.</span></span>

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

### <span data-ttu-id="81678-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="81678-131">-Throughput</span></span>
<span data-ttu-id="81678-132">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="81678-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="81678-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="81678-133">Default value is 400.</span></span>

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

### <span data-ttu-id="81678-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81678-134">-WhatIf</span></span>
<span data-ttu-id="81678-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81678-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81678-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81678-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81678-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81678-137">CommonParameters</span></span>
<span data-ttu-id="81678-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81678-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81678-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81678-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81678-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81678-140">INPUTS</span></span>

### <span data-ttu-id="81678-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="81678-141">None</span></span>

## <span data-ttu-id="81678-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81678-142">OUTPUTS</span></span>

### <span data-ttu-id="81678-143">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="81678-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="81678-144">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="81678-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="81678-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81678-145">NOTES</span></span>

## <span data-ttu-id="81678-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81678-146">RELATED LINKS</span></span>
