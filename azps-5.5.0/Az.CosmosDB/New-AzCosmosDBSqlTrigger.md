---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177242"
---
# <span data-ttu-id="ea1cb-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="ea1cb-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="ea1cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1cb-103">Tworzy nowy wyzwalacz sql dla firmy ADB.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="ea1cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea1cb-104">SYNTAX</span></span>

### <span data-ttu-id="ea1cb-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea1cb-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1cb-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea1cb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea1cb-107">DESCRIPTION</span></span>
<span data-ttu-id="ea1cb-108">Tworzy nowy wyzwalacz sql dla firmy ADB.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="ea1cb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea1cb-109">EXAMPLES</span></span>

### <span data-ttu-id="ea1cb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea1cb-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="ea1cb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea1cb-111">PARAMETERS</span></span>

### <span data-ttu-id="ea1cb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea1cb-112">-AccountName</span></span>
<span data-ttu-id="ea1cb-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ea1cb-114">— Treść</span><span class="sxs-lookup"><span data-stu-id="ea1cb-114">-Body</span></span>
<span data-ttu-id="ea1cb-115">Treść wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="ea1cb-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea1cb-116">-Confirm</span></span>
<span data-ttu-id="ea1cb-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1cb-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ea1cb-118">-ContainerName</span></span>
<span data-ttu-id="ea1cb-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-119">Container name.</span></span>

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

### <span data-ttu-id="ea1cb-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea1cb-120">-DatabaseName</span></span>
<span data-ttu-id="ea1cb-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-121">Database name.</span></span>

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

### <span data-ttu-id="ea1cb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1cb-122">-DefaultProfile</span></span>
<span data-ttu-id="ea1cb-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea1cb-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ea1cb-124">-Name</span></span>
<span data-ttu-id="ea1cb-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-125">Trigger name.</span></span>

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

### <span data-ttu-id="ea1cb-126">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="ea1cb-126">-ParentObject</span></span>
<span data-ttu-id="ea1cb-127">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-127">Sql Container object.</span></span>

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

### <span data-ttu-id="ea1cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea1cb-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-129">Name of resource group.</span></span>

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

### <span data-ttu-id="ea1cb-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="ea1cb-130">-TriggerOperation</span></span>
<span data-ttu-id="ea1cb-131">Operacja, z pomocą która jest skojarzona z wyzwalaczem.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="ea1cb-132">Możliwe wartości: "Wszystko", "Utwórz", "Aktualizacja", "Usuń", "Zamień"</span><span class="sxs-lookup"><span data-stu-id="ea1cb-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="ea1cb-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="ea1cb-133">-TriggerType</span></span>
<span data-ttu-id="ea1cb-134">Typ wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-134">Type of the Trigger.</span></span>
<span data-ttu-id="ea1cb-135">Możliwe wartości: "Przed", "Opublikuj"</span><span class="sxs-lookup"><span data-stu-id="ea1cb-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="ea1cb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1cb-136">-WhatIf</span></span>
<span data-ttu-id="ea1cb-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1cb-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1cb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1cb-139">CommonParameters</span></span>
<span data-ttu-id="ea1cb-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1cb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1cb-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea1cb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1cb-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea1cb-142">INPUTS</span></span>

### <span data-ttu-id="ea1cb-143">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="ea1cb-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="ea1cb-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea1cb-144">OUTPUTS</span></span>

### <span data-ttu-id="ea1cb-145">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="ea1cb-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="ea1cb-146">Microsoft.Azure.Commands.DoceńDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ea1cb-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ea1cb-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea1cb-147">NOTES</span></span>

## <span data-ttu-id="ea1cb-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea1cb-148">RELATED LINKS</span></span>
