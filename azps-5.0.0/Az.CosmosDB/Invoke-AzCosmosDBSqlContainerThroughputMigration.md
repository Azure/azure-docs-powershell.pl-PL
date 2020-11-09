---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307177"
---
# <span data-ttu-id="23857-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="23857-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="23857-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23857-102">SYNOPSIS</span></span>
<span data-ttu-id="23857-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="23857-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="23857-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23857-104">SYNTAX</span></span>

### <span data-ttu-id="23857-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23857-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23857-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23857-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23857-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23857-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23857-108">Opis</span><span class="sxs-lookup"><span data-stu-id="23857-108">DESCRIPTION</span></span>
<span data-ttu-id="23857-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="23857-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="23857-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23857-110">EXAMPLES</span></span>

### <span data-ttu-id="23857-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23857-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="23857-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23857-112">PARAMETERS</span></span>

### <span data-ttu-id="23857-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23857-113">-AccountName</span></span>
<span data-ttu-id="23857-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="23857-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="23857-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23857-115">-Confirm</span></span>
<span data-ttu-id="23857-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23857-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23857-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23857-117">-DatabaseName</span></span>
<span data-ttu-id="23857-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="23857-118">Database name.</span></span>

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

### <span data-ttu-id="23857-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23857-119">-DefaultProfile</span></span>
<span data-ttu-id="23857-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23857-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23857-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23857-121">-InputObject</span></span>
<span data-ttu-id="23857-122">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="23857-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23857-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23857-123">-Name</span></span>
<span data-ttu-id="23857-124">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="23857-124">Container name.</span></span>

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

### <span data-ttu-id="23857-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="23857-125">-ParentObject</span></span>
<span data-ttu-id="23857-126">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="23857-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23857-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23857-127">-ResourceGroupName</span></span>
<span data-ttu-id="23857-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23857-128">Name of resource group.</span></span>

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

### <span data-ttu-id="23857-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="23857-129">-ThroughputType</span></span>
<span data-ttu-id="23857-130">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="23857-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="23857-131">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="23857-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="23857-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23857-132">-WhatIf</span></span>
<span data-ttu-id="23857-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23857-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23857-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23857-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23857-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23857-135">CommonParameters</span></span>
<span data-ttu-id="23857-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23857-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23857-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23857-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23857-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23857-138">INPUTS</span></span>

### <span data-ttu-id="23857-139">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="23857-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="23857-140">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="23857-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="23857-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23857-141">OUTPUTS</span></span>

### <span data-ttu-id="23857-142">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="23857-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="23857-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23857-143">NOTES</span></span>

## <span data-ttu-id="23857-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23857-144">RELATED LINKS</span></span>
