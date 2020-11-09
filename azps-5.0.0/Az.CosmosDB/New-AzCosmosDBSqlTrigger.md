---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306967"
---
# <span data-ttu-id="0168f-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="0168f-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="0168f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0168f-102">SYNOPSIS</span></span>
<span data-ttu-id="0168f-103">Tworzy nowy wyzwalacz SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0168f-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="0168f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0168f-104">SYNTAX</span></span>

### <span data-ttu-id="0168f-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0168f-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0168f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0168f-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0168f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0168f-107">DESCRIPTION</span></span>
<span data-ttu-id="0168f-108">Tworzy nowy wyzwalacz SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0168f-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="0168f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0168f-109">EXAMPLES</span></span>

### <span data-ttu-id="0168f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0168f-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="0168f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0168f-111">PARAMETERS</span></span>

### <span data-ttu-id="0168f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0168f-112">-AccountName</span></span>
<span data-ttu-id="0168f-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0168f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0168f-114">-Body</span><span class="sxs-lookup"><span data-stu-id="0168f-114">-Body</span></span>
<span data-ttu-id="0168f-115">Treść wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="0168f-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="0168f-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0168f-116">-Confirm</span></span>
<span data-ttu-id="0168f-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0168f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0168f-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0168f-118">-ContainerName</span></span>
<span data-ttu-id="0168f-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="0168f-119">Container name.</span></span>

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

### <span data-ttu-id="0168f-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0168f-120">-DatabaseName</span></span>
<span data-ttu-id="0168f-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0168f-121">Database name.</span></span>

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

### <span data-ttu-id="0168f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0168f-122">-DefaultProfile</span></span>
<span data-ttu-id="0168f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0168f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0168f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0168f-124">-Name</span></span>
<span data-ttu-id="0168f-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="0168f-125">Trigger name.</span></span>

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

### <span data-ttu-id="0168f-126">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="0168f-126">-ParentObject</span></span>
<span data-ttu-id="0168f-127">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="0168f-127">Sql Container object.</span></span>

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

### <span data-ttu-id="0168f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0168f-128">-ResourceGroupName</span></span>
<span data-ttu-id="0168f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0168f-129">Name of resource group.</span></span>

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

### <span data-ttu-id="0168f-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="0168f-130">-TriggerOperation</span></span>
<span data-ttu-id="0168f-131">Operacja, z którą jest skojarzony wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="0168f-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="0168f-132">Możliwe wartości to: "wszystko", "Utwórz", "Aktualizuj", "Usuń", "Zamień".</span><span class="sxs-lookup"><span data-stu-id="0168f-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="0168f-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="0168f-133">-TriggerType</span></span>
<span data-ttu-id="0168f-134">Typ wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="0168f-134">Type of the Trigger.</span></span>
<span data-ttu-id="0168f-135">Możliwe są następujące wartości: "pre", "post"</span><span class="sxs-lookup"><span data-stu-id="0168f-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="0168f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0168f-136">-WhatIf</span></span>
<span data-ttu-id="0168f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0168f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0168f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0168f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0168f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0168f-139">CommonParameters</span></span>
<span data-ttu-id="0168f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0168f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0168f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0168f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0168f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0168f-142">INPUTS</span></span>

### <span data-ttu-id="0168f-143">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="0168f-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="0168f-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0168f-144">OUTPUTS</span></span>

### <span data-ttu-id="0168f-145">Microsoft. Azure. Commands. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="0168f-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="0168f-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="0168f-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="0168f-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0168f-147">NOTES</span></span>

## <span data-ttu-id="0168f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0168f-148">RELATED LINKS</span></span>
