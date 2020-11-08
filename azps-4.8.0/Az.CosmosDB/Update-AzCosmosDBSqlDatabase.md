---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221818"
---
# <span data-ttu-id="b3221-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b3221-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="b3221-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3221-102">SYNOPSIS</span></span>
<span data-ttu-id="b3221-103">Aktualizuje bazę danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b3221-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="b3221-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b3221-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b3221-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3221-105">SYNTAX</span></span>

### <span data-ttu-id="b3221-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3221-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3221-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3221-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3221-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3221-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3221-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b3221-109">DESCRIPTION</span></span>
<span data-ttu-id="b3221-110">Aktualizuje bazę danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b3221-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="b3221-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b3221-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b3221-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3221-112">EXAMPLES</span></span>

### <span data-ttu-id="b3221-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3221-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="b3221-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3221-114">PARAMETERS</span></span>

### <span data-ttu-id="b3221-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3221-115">-AccountName</span></span>
<span data-ttu-id="b3221-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b3221-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b3221-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b3221-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b3221-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="b3221-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b3221-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3221-119">-Confirm</span></span>
<span data-ttu-id="b3221-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3221-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3221-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3221-121">-DefaultProfile</span></span>
<span data-ttu-id="b3221-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3221-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3221-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3221-123">-InputObject</span></span>
<span data-ttu-id="b3221-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b3221-124">Sql Database object.</span></span>

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

### <span data-ttu-id="b3221-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3221-125">-Name</span></span>
<span data-ttu-id="b3221-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b3221-126">Database name.</span></span>

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

### <span data-ttu-id="b3221-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b3221-127">-ParentObject</span></span>
<span data-ttu-id="b3221-128">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b3221-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b3221-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3221-129">-ResourceGroupName</span></span>
<span data-ttu-id="b3221-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3221-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b3221-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="b3221-131">-Throughput</span></span>
<span data-ttu-id="b3221-132">Przepływność bazy danych SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b3221-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="b3221-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="b3221-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b3221-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3221-134">-WhatIf</span></span>
<span data-ttu-id="b3221-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3221-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3221-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3221-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3221-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3221-137">CommonParameters</span></span>
<span data-ttu-id="b3221-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3221-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3221-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3221-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3221-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3221-140">INPUTS</span></span>

### <span data-ttu-id="b3221-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b3221-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="b3221-142">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b3221-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="b3221-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3221-143">OUTPUTS</span></span>

### <span data-ttu-id="b3221-144">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b3221-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="b3221-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b3221-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b3221-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3221-146">NOTES</span></span>

## <span data-ttu-id="b3221-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3221-147">RELATED LINKS</span></span>
