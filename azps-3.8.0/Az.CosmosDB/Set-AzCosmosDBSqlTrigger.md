---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049516"
---
# <span data-ttu-id="5e8c0-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5e8c0-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5e8c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8c0-103">Umożliwia utworzenie nowego lub zaktualizowanie istniejącego wyzwalacza SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5e8c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e8c0-104">SYNTAX</span></span>

### <span data-ttu-id="5e8c0-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e8c0-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e8c0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e8c0-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e8c0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5e8c0-107">DESCRIPTION</span></span>
<span data-ttu-id="5e8c0-108">Polecenie cmdlet **Set-AzCosmosDBSqlTrigger** umożliwia utworzenie nowego lub zaktualizowanie istniejącego wyzwalacza SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5e8c0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e8c0-109">EXAMPLES</span></span>

### <span data-ttu-id="5e8c0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e8c0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="5e8c0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e8c0-111">PARAMETERS</span></span>

### <span data-ttu-id="5e8c0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e8c0-112">-AccountName</span></span>
<span data-ttu-id="5e8c0-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e8c0-114">-Body</span><span class="sxs-lookup"><span data-stu-id="5e8c0-114">-Body</span></span>
<span data-ttu-id="5e8c0-115">Treść wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="5e8c0-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e8c0-116">-Confirm</span></span>
<span data-ttu-id="5e8c0-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e8c0-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5e8c0-118">-ContainerName</span></span>
<span data-ttu-id="5e8c0-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-119">Container name.</span></span>

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

### <span data-ttu-id="5e8c0-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e8c0-120">-DatabaseName</span></span>
<span data-ttu-id="5e8c0-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-121">Database name.</span></span>

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

### <span data-ttu-id="5e8c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8c0-122">-DefaultProfile</span></span>
<span data-ttu-id="5e8c0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e8c0-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e8c0-124">-InputObject</span></span>
<span data-ttu-id="5e8c0-125">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e8c0-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e8c0-126">-Name</span></span>
<span data-ttu-id="5e8c0-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-127">Trigger name.</span></span>

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

### <span data-ttu-id="5e8c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e8c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e8c0-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-129">Name of resource group.</span></span>

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

### <span data-ttu-id="5e8c0-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="5e8c0-130">-TriggerOperation</span></span>
<span data-ttu-id="5e8c0-131">Operacja, z którą jest skojarzony wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="5e8c0-132">Możliwe wartości to: "wszystko", "Utwórz", "Aktualizuj", "Usuń", "Zamień".</span><span class="sxs-lookup"><span data-stu-id="5e8c0-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="5e8c0-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="5e8c0-133">-TriggerType</span></span>
<span data-ttu-id="5e8c0-134">Typ wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-134">Type of the Trigger.</span></span>
<span data-ttu-id="5e8c0-135">Możliwe są następujące wartości: "pre", "post"</span><span class="sxs-lookup"><span data-stu-id="5e8c0-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="5e8c0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e8c0-136">-WhatIf</span></span>
<span data-ttu-id="5e8c0-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e8c0-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e8c0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8c0-139">CommonParameters</span></span>
<span data-ttu-id="5e8c0-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8c0-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e8c0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8c0-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e8c0-142">INPUTS</span></span>

### <span data-ttu-id="5e8c0-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5e8c0-143">None</span></span>

## <span data-ttu-id="5e8c0-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e8c0-144">OUTPUTS</span></span>

### <span data-ttu-id="5e8c0-145">Microsoft. Azure. Commands. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="5e8c0-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="5e8c0-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e8c0-146">NOTES</span></span>

## <span data-ttu-id="5e8c0-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e8c0-147">RELATED LINKS</span></span>
