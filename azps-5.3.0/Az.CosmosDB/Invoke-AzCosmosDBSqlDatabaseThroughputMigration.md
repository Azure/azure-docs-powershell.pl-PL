---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 927cdbd6c599b090a66120e95a1ac1a024360271
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503843"
---
# <span data-ttu-id="06dbd-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="06dbd-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="06dbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="06dbd-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="06dbd-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="06dbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06dbd-104">SYNTAX</span></span>

### <span data-ttu-id="06dbd-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06dbd-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06dbd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06dbd-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06dbd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06dbd-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06dbd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="06dbd-108">DESCRIPTION</span></span>
<span data-ttu-id="06dbd-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="06dbd-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="06dbd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06dbd-110">EXAMPLES</span></span>

### <span data-ttu-id="06dbd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06dbd-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="06dbd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06dbd-112">PARAMETERS</span></span>

### <span data-ttu-id="06dbd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06dbd-113">-AccountName</span></span>
<span data-ttu-id="06dbd-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="06dbd-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="06dbd-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06dbd-115">-Confirm</span></span>
<span data-ttu-id="06dbd-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06dbd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06dbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dbd-117">-DefaultProfile</span></span>
<span data-ttu-id="06dbd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06dbd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06dbd-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="06dbd-119">-InputObject</span></span>
<span data-ttu-id="06dbd-120">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="06dbd-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06dbd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06dbd-121">-Name</span></span>
<span data-ttu-id="06dbd-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="06dbd-122">Database name.</span></span>

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

### <span data-ttu-id="06dbd-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="06dbd-123">-ParentObject</span></span>
<span data-ttu-id="06dbd-124">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="06dbd-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="06dbd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06dbd-125">-ResourceGroupName</span></span>
<span data-ttu-id="06dbd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06dbd-126">Name of resource group.</span></span>

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

### <span data-ttu-id="06dbd-127">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="06dbd-127">-ThroughputType</span></span>
<span data-ttu-id="06dbd-128">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="06dbd-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="06dbd-129">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="06dbd-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="06dbd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06dbd-130">-WhatIf</span></span>
<span data-ttu-id="06dbd-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06dbd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06dbd-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06dbd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06dbd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dbd-133">CommonParameters</span></span>
<span data-ttu-id="06dbd-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06dbd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dbd-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06dbd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dbd-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06dbd-136">INPUTS</span></span>

### <span data-ttu-id="06dbd-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="06dbd-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="06dbd-138">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="06dbd-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="06dbd-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06dbd-139">OUTPUTS</span></span>

### <span data-ttu-id="06dbd-140">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="06dbd-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="06dbd-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06dbd-141">NOTES</span></span>

## <span data-ttu-id="06dbd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06dbd-142">RELATED LINKS</span></span>
