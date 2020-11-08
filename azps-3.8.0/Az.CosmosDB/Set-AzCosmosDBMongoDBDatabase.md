---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053401"
---
# <span data-ttu-id="f2697-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="f2697-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="f2697-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2697-102">SYNOPSIS</span></span>
<span data-ttu-id="f2697-103">Ustawia bazę danych programu CosmosDB MongoDB</span><span class="sxs-lookup"><span data-stu-id="f2697-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="f2697-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2697-104">SYNTAX</span></span>

### <span data-ttu-id="f2697-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2697-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2697-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2697-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2697-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f2697-107">DESCRIPTION</span></span>
<span data-ttu-id="f2697-108">Polecenie cmdlet **Set-AzCosmosDBMongoDBDatabase** pobiera bazę danych CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f2697-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="f2697-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2697-109">EXAMPLES</span></span>

### <span data-ttu-id="f2697-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2697-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="f2697-111">Obiekt zasobu zawiera _rid, _ts, właściwości _etag.</span><span class="sxs-lookup"><span data-stu-id="f2697-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="f2697-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2697-112">PARAMETERS</span></span>

### <span data-ttu-id="f2697-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2697-113">-AccountName</span></span>
<span data-ttu-id="f2697-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f2697-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f2697-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2697-115">-Confirm</span></span>
<span data-ttu-id="f2697-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2697-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2697-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2697-117">-DefaultProfile</span></span>
<span data-ttu-id="f2697-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2697-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2697-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f2697-119">-InputObject</span></span>
<span data-ttu-id="f2697-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f2697-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f2697-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2697-121">-Name</span></span>
<span data-ttu-id="f2697-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f2697-122">Database name.</span></span>

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

### <span data-ttu-id="f2697-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2697-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2697-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2697-124">Name of resource group.</span></span>

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

### <span data-ttu-id="f2697-125">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="f2697-125">-Throughput</span></span>
<span data-ttu-id="f2697-126">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f2697-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="f2697-127">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="f2697-127">Default value is 400.</span></span>

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

### <span data-ttu-id="f2697-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2697-128">-WhatIf</span></span>
<span data-ttu-id="f2697-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2697-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2697-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2697-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2697-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2697-131">CommonParameters</span></span>
<span data-ttu-id="f2697-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2697-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2697-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2697-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2697-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2697-134">INPUTS</span></span>

### <span data-ttu-id="f2697-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f2697-135">None</span></span>

## <span data-ttu-id="f2697-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2697-136">OUTPUTS</span></span>

### <span data-ttu-id="f2697-137">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f2697-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="f2697-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2697-138">NOTES</span></span>

## <span data-ttu-id="f2697-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2697-139">RELATED LINKS</span></span>
