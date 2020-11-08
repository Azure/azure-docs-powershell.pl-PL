---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: d90df542fd2acc925531f4bf9da7244ea1831a63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051148"
---
# <span data-ttu-id="eaf79-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="eaf79-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="eaf79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaf79-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf79-103">Aktualizuje wartość przepływności w bazie danych CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="eaf79-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="eaf79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaf79-104">SYNTAX</span></span>

### <span data-ttu-id="eaf79-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eaf79-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf79-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaf79-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaf79-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaf79-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaf79-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaf79-108">EXAMPLES</span></span>

### <span data-ttu-id="eaf79-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eaf79-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="eaf79-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaf79-110">PARAMETERS</span></span>

### <span data-ttu-id="eaf79-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eaf79-111">-AccountName</span></span>
<span data-ttu-id="eaf79-112">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="eaf79-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="eaf79-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eaf79-113">-Confirm</span></span>
<span data-ttu-id="eaf79-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaf79-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf79-115">-DefaultProfile</span></span>
<span data-ttu-id="eaf79-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf79-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eaf79-117">-InputObject</span></span>
<span data-ttu-id="eaf79-118">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="eaf79-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="eaf79-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eaf79-119">-Name</span></span>
<span data-ttu-id="eaf79-120">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eaf79-120">Database name.</span></span>

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

### <span data-ttu-id="eaf79-121">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="eaf79-121">-ParentObject</span></span>
<span data-ttu-id="eaf79-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="eaf79-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf79-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf79-123">-ResourceGroupName</span></span>
<span data-ttu-id="eaf79-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eaf79-124">Name of resource group.</span></span>

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

### <span data-ttu-id="eaf79-125">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="eaf79-125">-Throughput</span></span>
<span data-ttu-id="eaf79-126">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="eaf79-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="eaf79-127">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="eaf79-127">Default value is 400.</span></span>

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

### <span data-ttu-id="eaf79-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf79-128">-WhatIf</span></span>
<span data-ttu-id="eaf79-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaf79-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf79-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eaf79-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf79-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf79-131">CommonParameters</span></span>
<span data-ttu-id="eaf79-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf79-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf79-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaf79-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf79-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaf79-134">INPUTS</span></span>

### <span data-ttu-id="eaf79-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eaf79-135">None</span></span>

## <span data-ttu-id="eaf79-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaf79-136">OUTPUTS</span></span>

### <span data-ttu-id="eaf79-137">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="eaf79-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="eaf79-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaf79-138">NOTES</span></span>

## <span data-ttu-id="eaf79-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaf79-139">RELATED LINKS</span></span>
