---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051159"
---
# <span data-ttu-id="acc8f-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="acc8f-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="acc8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="acc8f-102">SYNOPSIS</span></span>
<span data-ttu-id="acc8f-103">Umożliwia ustawienie tabeli CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="acc8f-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="acc8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="acc8f-104">SYNTAX</span></span>

### <span data-ttu-id="acc8f-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="acc8f-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc8f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc8f-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acc8f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="acc8f-107">DESCRIPTION</span></span>
<span data-ttu-id="acc8f-108">Polecenie cmdlet **Set-AzCosmosDBTable** tworzy nową tabelę lub aktualizuje istniejącą tabelę, zastępując istniejącą tabelę całkowicie.</span><span class="sxs-lookup"><span data-stu-id="acc8f-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="acc8f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="acc8f-109">EXAMPLES</span></span>

### <span data-ttu-id="acc8f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="acc8f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="acc8f-111">Obiekt zasobu zawiera właściwości _rid, _ts, ETag tabeli.</span><span class="sxs-lookup"><span data-stu-id="acc8f-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="acc8f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="acc8f-112">PARAMETERS</span></span>

### <span data-ttu-id="acc8f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="acc8f-113">-AccountName</span></span>
<span data-ttu-id="acc8f-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="acc8f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="acc8f-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="acc8f-115">-Confirm</span></span>
<span data-ttu-id="acc8f-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acc8f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc8f-117">-DefaultProfile</span></span>
<span data-ttu-id="acc8f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="acc8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc8f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="acc8f-119">-InputObject</span></span>
<span data-ttu-id="acc8f-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="acc8f-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="acc8f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="acc8f-121">-Name</span></span>
<span data-ttu-id="acc8f-122">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="acc8f-122">Name of the Table.</span></span>

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

### <span data-ttu-id="acc8f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc8f-123">-ResourceGroupName</span></span>
<span data-ttu-id="acc8f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="acc8f-124">Name of resource group.</span></span>

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

### <span data-ttu-id="acc8f-125">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="acc8f-125">-Throughput</span></span>
<span data-ttu-id="acc8f-126">Przepływność tabeli (RU/s).</span><span class="sxs-lookup"><span data-stu-id="acc8f-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="acc8f-127">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="acc8f-127">Default value is 400.</span></span>

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

### <span data-ttu-id="acc8f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc8f-128">-WhatIf</span></span>
<span data-ttu-id="acc8f-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acc8f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acc8f-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="acc8f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc8f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc8f-131">CommonParameters</span></span>
<span data-ttu-id="acc8f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc8f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc8f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acc8f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc8f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acc8f-134">INPUTS</span></span>

### <span data-ttu-id="acc8f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="acc8f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="acc8f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="acc8f-136">OUTPUTS</span></span>

### <span data-ttu-id="acc8f-137">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="acc8f-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="acc8f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="acc8f-138">NOTES</span></span>

## <span data-ttu-id="acc8f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acc8f-139">RELATED LINKS</span></span>
