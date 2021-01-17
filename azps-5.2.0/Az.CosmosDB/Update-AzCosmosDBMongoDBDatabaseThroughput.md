---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1948bc5b5488c951861509c9b3c9ee7815eddec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371730"
---
# <span data-ttu-id="f6e5a-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="f6e5a-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="f6e5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e5a-103">Aktualizuje wartość przepływności w bazie danych CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="f6e5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6e5a-104">SYNTAX</span></span>

### <span data-ttu-id="f6e5a-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f6e5a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6e5a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6e5a-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6e5a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6e5a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6e5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f6e5a-108">DESCRIPTION</span></span>
<span data-ttu-id="f6e5a-109">Aktualizuje wartość przepływności w bazie danych CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="f6e5a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6e5a-110">EXAMPLES</span></span>

### <span data-ttu-id="f6e5a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6e5a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="f6e5a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6e5a-112">PARAMETERS</span></span>

### <span data-ttu-id="f6e5a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f6e5a-113">-AccountName</span></span>
<span data-ttu-id="f6e5a-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f6e5a-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f6e5a-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f6e5a-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f6e5a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6e5a-117">-Confirm</span></span>
<span data-ttu-id="f6e5a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6e5a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e5a-119">-DefaultProfile</span></span>
<span data-ttu-id="f6e5a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e5a-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f6e5a-121">-InputObject</span></span>
<span data-ttu-id="f6e5a-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f6e5a-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f6e5a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6e5a-123">-Name</span></span>
<span data-ttu-id="f6e5a-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-124">Database name.</span></span>

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

### <span data-ttu-id="f6e5a-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="f6e5a-125">-ParentObject</span></span>
<span data-ttu-id="f6e5a-126">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f6e5a-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f6e5a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e5a-127">-ResourceGroupName</span></span>
<span data-ttu-id="f6e5a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="f6e5a-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="f6e5a-129">-Throughput</span></span>
<span data-ttu-id="f6e5a-130">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f6e5a-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="f6e5a-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-131">Default value is 400.</span></span>

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

### <span data-ttu-id="f6e5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6e5a-132">-WhatIf</span></span>
<span data-ttu-id="f6e5a-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6e5a-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6e5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e5a-135">CommonParameters</span></span>
<span data-ttu-id="f6e5a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6e5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e5a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6e5a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e5a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6e5a-138">INPUTS</span></span>

### <span data-ttu-id="f6e5a-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f6e5a-139">None</span></span>

## <span data-ttu-id="f6e5a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6e5a-140">OUTPUTS</span></span>

### <span data-ttu-id="f6e5a-141">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f6e5a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f6e5a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6e5a-142">NOTES</span></span>

## <span data-ttu-id="f6e5a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6e5a-143">RELATED LINKS</span></span>
