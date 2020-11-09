---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 324350329b166ab3a41f7e2bd8b59af1b9efdcb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306745"
---
# <span data-ttu-id="ea879-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ea879-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="ea879-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea879-102">SYNOPSIS</span></span>
<span data-ttu-id="ea879-103">Aktualizuje wartość przepływności bazy danych usługi SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ea879-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ea879-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea879-104">SYNTAX</span></span>

### <span data-ttu-id="ea879-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea879-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea879-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea879-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea879-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea879-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea879-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea879-108">DESCRIPTION</span></span>
<span data-ttu-id="ea879-109">Aktualizuje wartość przepływności bazy danych usługi SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ea879-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ea879-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea879-110">EXAMPLES</span></span>

### <span data-ttu-id="ea879-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea879-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ea879-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea879-112">PARAMETERS</span></span>

### <span data-ttu-id="ea879-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea879-113">-AccountName</span></span>
<span data-ttu-id="ea879-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ea879-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ea879-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ea879-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ea879-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="ea879-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ea879-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea879-117">-Confirm</span></span>
<span data-ttu-id="ea879-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea879-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea879-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea879-119">-DefaultProfile</span></span>
<span data-ttu-id="ea879-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea879-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea879-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea879-121">-InputObject</span></span>
<span data-ttu-id="ea879-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ea879-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ea879-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea879-123">-Name</span></span>
<span data-ttu-id="ea879-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ea879-124">Database name.</span></span>

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

### <span data-ttu-id="ea879-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="ea879-125">-ParentObject</span></span>
<span data-ttu-id="ea879-126">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ea879-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ea879-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea879-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea879-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea879-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ea879-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="ea879-129">-Throughput</span></span>
<span data-ttu-id="ea879-130">Przepływność bazy danych SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ea879-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="ea879-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="ea879-131">Default value is 400.</span></span>

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

### <span data-ttu-id="ea879-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea879-132">-WhatIf</span></span>
<span data-ttu-id="ea879-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea879-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea879-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea879-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea879-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea879-135">CommonParameters</span></span>
<span data-ttu-id="ea879-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea879-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea879-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea879-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea879-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea879-138">INPUTS</span></span>

### <span data-ttu-id="ea879-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ea879-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ea879-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea879-140">OUTPUTS</span></span>

### <span data-ttu-id="ea879-141">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ea879-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ea879-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea879-142">NOTES</span></span>

## <span data-ttu-id="ea879-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea879-143">RELATED LINKS</span></span>
