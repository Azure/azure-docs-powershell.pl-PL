---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223600"
---
# <span data-ttu-id="47390-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="47390-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="47390-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47390-102">SYNOPSIS</span></span>
<span data-ttu-id="47390-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="47390-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="47390-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47390-104">SYNTAX</span></span>

### <span data-ttu-id="47390-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="47390-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47390-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47390-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47390-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47390-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47390-108">Opis</span><span class="sxs-lookup"><span data-stu-id="47390-108">DESCRIPTION</span></span>
<span data-ttu-id="47390-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="47390-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="47390-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47390-110">EXAMPLES</span></span>

### <span data-ttu-id="47390-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47390-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="47390-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47390-112">PARAMETERS</span></span>

### <span data-ttu-id="47390-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="47390-113">-AccountName</span></span>
<span data-ttu-id="47390-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="47390-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="47390-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47390-115">-Confirm</span></span>
<span data-ttu-id="47390-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47390-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47390-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47390-117">-DatabaseName</span></span>
<span data-ttu-id="47390-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="47390-118">Database name.</span></span>

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

### <span data-ttu-id="47390-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47390-119">-DefaultProfile</span></span>
<span data-ttu-id="47390-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47390-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47390-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="47390-121">-InputObject</span></span>
<span data-ttu-id="47390-122">Obiekt kolekcji Mongo.</span><span class="sxs-lookup"><span data-stu-id="47390-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47390-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47390-123">-Name</span></span>
<span data-ttu-id="47390-124">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="47390-124">Collection name.</span></span>

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

### <span data-ttu-id="47390-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="47390-125">-ParentObject</span></span>
<span data-ttu-id="47390-126">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="47390-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47390-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47390-127">-ResourceGroupName</span></span>
<span data-ttu-id="47390-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47390-128">Name of resource group.</span></span>

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

### <span data-ttu-id="47390-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="47390-129">-ThroughputType</span></span>
<span data-ttu-id="47390-130">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="47390-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="47390-131">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="47390-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="47390-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47390-132">-WhatIf</span></span>
<span data-ttu-id="47390-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47390-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47390-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47390-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47390-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47390-135">CommonParameters</span></span>
<span data-ttu-id="47390-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47390-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47390-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47390-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47390-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47390-138">INPUTS</span></span>

### <span data-ttu-id="47390-139">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="47390-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="47390-140">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="47390-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="47390-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47390-141">OUTPUTS</span></span>

### <span data-ttu-id="47390-142">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="47390-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="47390-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47390-143">NOTES</span></span>

## <span data-ttu-id="47390-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47390-144">RELATED LINKS</span></span>
