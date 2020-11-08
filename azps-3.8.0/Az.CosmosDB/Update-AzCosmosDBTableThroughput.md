---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 56c99a1e3cf21f38544e97ee84ba10efb51bc983
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051141"
---
# <span data-ttu-id="8f742-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="8f742-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="8f742-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f742-102">SYNOPSIS</span></span>
<span data-ttu-id="8f742-103">Umożliwia zaktualizowanie wartości przepływności tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8f742-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="8f742-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f742-104">SYNTAX</span></span>

### <span data-ttu-id="8f742-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8f742-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f742-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f742-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -ParentObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f742-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f742-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -InputObject <PSTableGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f742-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f742-108">EXAMPLES</span></span>

### <span data-ttu-id="8f742-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f742-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="8f742-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f742-110">PARAMETERS</span></span>

### <span data-ttu-id="8f742-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8f742-111">-AccountName</span></span>
<span data-ttu-id="8f742-112">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="8f742-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8f742-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f742-113">-Confirm</span></span>
<span data-ttu-id="8f742-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f742-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f742-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f742-115">-DefaultProfile</span></span>
<span data-ttu-id="8f742-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f742-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f742-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8f742-117">-InputObject</span></span>
<span data-ttu-id="8f742-118">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8f742-118">CosmosDB Account object</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f742-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f742-119">-Name</span></span>
<span data-ttu-id="8f742-120">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="8f742-120">Name of the Table.</span></span>

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

### <span data-ttu-id="8f742-121">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="8f742-121">-ParentObject</span></span>
<span data-ttu-id="8f742-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8f742-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f742-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f742-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f742-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f742-124">Name of resource group.</span></span>

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

### <span data-ttu-id="8f742-125">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="8f742-125">-Throughput</span></span>
<span data-ttu-id="8f742-126">Przepływność tabeli (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8f742-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="8f742-127">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="8f742-127">Default value is 400.</span></span>

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

### <span data-ttu-id="8f742-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f742-128">-WhatIf</span></span>
<span data-ttu-id="8f742-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f742-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f742-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8f742-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f742-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f742-131">CommonParameters</span></span>
<span data-ttu-id="8f742-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f742-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f742-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f742-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f742-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f742-134">INPUTS</span></span>

### <span data-ttu-id="8f742-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8f742-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8f742-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f742-136">OUTPUTS</span></span>

### <span data-ttu-id="8f742-137">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8f742-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8f742-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f742-138">NOTES</span></span>

## <span data-ttu-id="8f742-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f742-139">RELATED LINKS</span></span>
