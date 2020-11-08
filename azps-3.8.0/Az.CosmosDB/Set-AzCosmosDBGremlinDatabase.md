---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053402"
---
# <span data-ttu-id="8ffd2-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="8ffd2-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="8ffd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ffd2-102">SYNOPSIS</span></span>
<span data-ttu-id="8ffd2-103">Ustawia bazę danych Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="8ffd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ffd2-104">SYNTAX</span></span>

### <span data-ttu-id="8ffd2-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ffd2-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ffd2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ffd2-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ffd2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8ffd2-107">DESCRIPTION</span></span>
<span data-ttu-id="8ffd2-108">Polecenie cmdlet **Set-AzCosmosDBGremlinDatabase** ustawia bazę danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="8ffd2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ffd2-109">EXAMPLES</span></span>

### <span data-ttu-id="8ffd2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ffd2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="8ffd2-111">Obiekt zasobu zawiera _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="8ffd2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ffd2-112">PARAMETERS</span></span>

### <span data-ttu-id="8ffd2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ffd2-113">-AccountName</span></span>
<span data-ttu-id="8ffd2-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8ffd2-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ffd2-115">-Confirm</span></span>
<span data-ttu-id="8ffd2-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ffd2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ffd2-117">-DefaultProfile</span></span>
<span data-ttu-id="8ffd2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ffd2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ffd2-119">-InputObject</span></span>
<span data-ttu-id="8ffd2-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8ffd2-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8ffd2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ffd2-121">-Name</span></span>
<span data-ttu-id="8ffd2-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-122">Database name.</span></span>

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

### <span data-ttu-id="8ffd2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ffd2-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ffd2-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-124">Name of resource group.</span></span>

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

### <span data-ttu-id="8ffd2-125">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="8ffd2-125">-Throughput</span></span>
<span data-ttu-id="8ffd2-126">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8ffd2-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="8ffd2-127">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-127">Default value is 400.</span></span>

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

### <span data-ttu-id="8ffd2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ffd2-128">-WhatIf</span></span>
<span data-ttu-id="8ffd2-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ffd2-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ffd2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ffd2-131">CommonParameters</span></span>
<span data-ttu-id="8ffd2-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ffd2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ffd2-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ffd2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ffd2-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ffd2-134">INPUTS</span></span>

### <span data-ttu-id="8ffd2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8ffd2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8ffd2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ffd2-136">OUTPUTS</span></span>

### <span data-ttu-id="8ffd2-137">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8ffd2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="8ffd2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ffd2-138">NOTES</span></span>

## <span data-ttu-id="8ffd2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ffd2-139">RELATED LINKS</span></span>
