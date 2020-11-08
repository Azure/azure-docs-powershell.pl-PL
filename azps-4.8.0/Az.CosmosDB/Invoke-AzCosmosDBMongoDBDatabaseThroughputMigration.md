---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223598"
---
# <span data-ttu-id="5b73b-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="5b73b-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="5b73b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b73b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b73b-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="5b73b-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="5b73b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b73b-104">SYNTAX</span></span>

### <span data-ttu-id="5b73b-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5b73b-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b73b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b73b-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b73b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b73b-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b73b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5b73b-108">DESCRIPTION</span></span>
<span data-ttu-id="5b73b-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="5b73b-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="5b73b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b73b-110">EXAMPLES</span></span>

### <span data-ttu-id="5b73b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b73b-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="5b73b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b73b-112">PARAMETERS</span></span>

### <span data-ttu-id="5b73b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b73b-113">-AccountName</span></span>
<span data-ttu-id="5b73b-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5b73b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5b73b-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b73b-115">-Confirm</span></span>
<span data-ttu-id="5b73b-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b73b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b73b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b73b-117">-DefaultProfile</span></span>
<span data-ttu-id="5b73b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b73b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b73b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b73b-119">-InputObject</span></span>
<span data-ttu-id="5b73b-120">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="5b73b-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b73b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b73b-121">-Name</span></span>
<span data-ttu-id="5b73b-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5b73b-122">Database name.</span></span>

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

### <span data-ttu-id="5b73b-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="5b73b-123">-ParentObject</span></span>
<span data-ttu-id="5b73b-124">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5b73b-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5b73b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b73b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b73b-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5b73b-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5b73b-127">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="5b73b-127">-ThroughputType</span></span>
<span data-ttu-id="5b73b-128">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="5b73b-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="5b73b-129">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="5b73b-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="5b73b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b73b-130">-WhatIf</span></span>
<span data-ttu-id="5b73b-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b73b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b73b-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5b73b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b73b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b73b-133">CommonParameters</span></span>
<span data-ttu-id="5b73b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b73b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b73b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b73b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b73b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b73b-136">INPUTS</span></span>

### <span data-ttu-id="5b73b-137">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5b73b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="5b73b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b73b-138">OUTPUTS</span></span>

### <span data-ttu-id="5b73b-139">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5b73b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5b73b-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b73b-140">NOTES</span></span>

## <span data-ttu-id="5b73b-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b73b-141">RELATED LINKS</span></span>
