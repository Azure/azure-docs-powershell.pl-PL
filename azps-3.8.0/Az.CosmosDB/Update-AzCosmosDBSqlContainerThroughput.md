---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051151"
---
# <span data-ttu-id="286c8-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="286c8-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="286c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="286c8-102">SYNOPSIS</span></span>
<span data-ttu-id="286c8-103">Aktualizuje wartość przepływności w kontenerze SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="286c8-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="286c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="286c8-104">SYNTAX</span></span>

### <span data-ttu-id="286c8-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="286c8-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286c8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="286c8-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="286c8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="286c8-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="286c8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="286c8-108">EXAMPLES</span></span>

### <span data-ttu-id="286c8-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="286c8-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="286c8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="286c8-110">PARAMETERS</span></span>

### <span data-ttu-id="286c8-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="286c8-111">-AccountName</span></span>
<span data-ttu-id="286c8-112">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="286c8-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="286c8-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="286c8-113">-Confirm</span></span>
<span data-ttu-id="286c8-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286c8-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286c8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="286c8-115">-DatabaseName</span></span>
<span data-ttu-id="286c8-116">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="286c8-116">Database name.</span></span>

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

### <span data-ttu-id="286c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286c8-117">-DefaultProfile</span></span>
<span data-ttu-id="286c8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="286c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286c8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="286c8-119">-InputObject</span></span>
<span data-ttu-id="286c8-120">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="286c8-120">Sql Database object.</span></span>

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

### <span data-ttu-id="286c8-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="286c8-121">-Name</span></span>
<span data-ttu-id="286c8-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="286c8-122">Container name.</span></span>

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

### <span data-ttu-id="286c8-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="286c8-123">-ParentObject</span></span>
<span data-ttu-id="286c8-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="286c8-124">Sql Database object.</span></span>

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

### <span data-ttu-id="286c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="286c8-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="286c8-126">Name of resource group.</span></span>

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

### <span data-ttu-id="286c8-127">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="286c8-127">-Throughput</span></span>
<span data-ttu-id="286c8-128">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="286c8-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="286c8-129">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="286c8-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286c8-130">-WhatIf</span></span>
<span data-ttu-id="286c8-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286c8-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="286c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286c8-133">CommonParameters</span></span>
<span data-ttu-id="286c8-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286c8-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="286c8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286c8-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="286c8-136">INPUTS</span></span>

### <span data-ttu-id="286c8-137">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="286c8-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="286c8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="286c8-138">OUTPUTS</span></span>

### <span data-ttu-id="286c8-139">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="286c8-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="286c8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="286c8-140">NOTES</span></span>

## <span data-ttu-id="286c8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="286c8-141">RELATED LINKS</span></span>
