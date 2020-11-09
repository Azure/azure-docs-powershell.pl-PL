---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307039"
---
# <span data-ttu-id="79e23-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="79e23-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="79e23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79e23-102">SYNOPSIS</span></span>
<span data-ttu-id="79e23-103">Tworzy nową bazę danych MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="79e23-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="79e23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79e23-104">SYNTAX</span></span>

### <span data-ttu-id="79e23-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79e23-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e23-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79e23-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79e23-107">Opis</span><span class="sxs-lookup"><span data-stu-id="79e23-107">DESCRIPTION</span></span>
<span data-ttu-id="79e23-108">Tworzy nową bazę danych MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="79e23-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="79e23-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79e23-109">EXAMPLES</span></span>

### <span data-ttu-id="79e23-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79e23-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="79e23-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79e23-111">PARAMETERS</span></span>

### <span data-ttu-id="79e23-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79e23-112">-AccountName</span></span>
<span data-ttu-id="79e23-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="79e23-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79e23-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="79e23-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="79e23-115">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="79e23-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="79e23-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79e23-116">-Confirm</span></span>
<span data-ttu-id="79e23-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79e23-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e23-118">-DefaultProfile</span></span>
<span data-ttu-id="79e23-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79e23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e23-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79e23-120">-Name</span></span>
<span data-ttu-id="79e23-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="79e23-121">Database name.</span></span>

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

### <span data-ttu-id="79e23-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="79e23-122">-ParentObject</span></span>
<span data-ttu-id="79e23-123">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="79e23-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="79e23-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e23-124">-ResourceGroupName</span></span>
<span data-ttu-id="79e23-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79e23-125">Name of resource group.</span></span>

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

### <span data-ttu-id="79e23-126">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="79e23-126">-Throughput</span></span>
<span data-ttu-id="79e23-127">Przepływność bazy danych Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="79e23-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="79e23-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="79e23-128">Default value is 400.</span></span>

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

### <span data-ttu-id="79e23-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e23-129">-WhatIf</span></span>
<span data-ttu-id="79e23-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79e23-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e23-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79e23-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e23-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e23-132">CommonParameters</span></span>
<span data-ttu-id="79e23-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e23-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e23-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79e23-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e23-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79e23-135">INPUTS</span></span>

### <span data-ttu-id="79e23-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="79e23-136">None</span></span>

## <span data-ttu-id="79e23-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79e23-137">OUTPUTS</span></span>

### <span data-ttu-id="79e23-138">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="79e23-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="79e23-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="79e23-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="79e23-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79e23-140">NOTES</span></span>

## <span data-ttu-id="79e23-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79e23-141">RELATED LINKS</span></span>
