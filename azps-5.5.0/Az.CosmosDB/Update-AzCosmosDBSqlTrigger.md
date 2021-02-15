---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196739"
---
# <span data-ttu-id="9107a-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="9107a-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="9107a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9107a-102">SYNOPSIS</span></span>
<span data-ttu-id="9107a-103">Aktualizacja wyzwalacza sql dla firmy JavasDB.</span><span class="sxs-lookup"><span data-stu-id="9107a-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="9107a-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejący wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="9107a-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="9107a-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9107a-105">SYNTAX</span></span>

### <span data-ttu-id="9107a-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9107a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9107a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9107a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9107a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9107a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9107a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9107a-109">DESCRIPTION</span></span>
<span data-ttu-id="9107a-110">Aktualizacja wyzwalacza sql dla firmy JavasDB.</span><span class="sxs-lookup"><span data-stu-id="9107a-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="9107a-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejący wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="9107a-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="9107a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9107a-112">EXAMPLES</span></span>

### <span data-ttu-id="9107a-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9107a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="9107a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9107a-114">PARAMETERS</span></span>

### <span data-ttu-id="9107a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9107a-115">-AccountName</span></span>
<span data-ttu-id="9107a-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="9107a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9107a-117">— Treść</span><span class="sxs-lookup"><span data-stu-id="9107a-117">-Body</span></span>
<span data-ttu-id="9107a-118">Treść wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="9107a-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="9107a-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9107a-119">-Confirm</span></span>
<span data-ttu-id="9107a-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9107a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9107a-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9107a-121">-ContainerName</span></span>
<span data-ttu-id="9107a-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="9107a-122">Container name.</span></span>

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

### <span data-ttu-id="9107a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9107a-123">-DatabaseName</span></span>
<span data-ttu-id="9107a-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9107a-124">Database name.</span></span>

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

### <span data-ttu-id="9107a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9107a-125">-DefaultProfile</span></span>
<span data-ttu-id="9107a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9107a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9107a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9107a-127">-InputObject</span></span>
<span data-ttu-id="9107a-128">Obiekt wyzwalacza języka Sql</span><span class="sxs-lookup"><span data-stu-id="9107a-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9107a-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9107a-129">-Name</span></span>
<span data-ttu-id="9107a-130">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="9107a-130">Trigger name.</span></span>

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

### <span data-ttu-id="9107a-131">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="9107a-131">-ParentObject</span></span>
<span data-ttu-id="9107a-132">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="9107a-132">Sql Container object.</span></span>

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

### <span data-ttu-id="9107a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9107a-133">-ResourceGroupName</span></span>
<span data-ttu-id="9107a-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9107a-134">Name of resource group.</span></span>

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

### <span data-ttu-id="9107a-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="9107a-135">-TriggerOperation</span></span>
<span data-ttu-id="9107a-136">Operacja, z pomocą która jest skojarzona z wyzwalaczem.</span><span class="sxs-lookup"><span data-stu-id="9107a-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="9107a-137">Możliwe wartości: "Wszystko", "Utwórz", "Aktualizacja", "Usuń", "Zamień"</span><span class="sxs-lookup"><span data-stu-id="9107a-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="9107a-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="9107a-138">-TriggerType</span></span>
<span data-ttu-id="9107a-139">Typ wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="9107a-139">Type of the Trigger.</span></span>
<span data-ttu-id="9107a-140">Możliwe wartości: "Przed", "Opublikuj"</span><span class="sxs-lookup"><span data-stu-id="9107a-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="9107a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9107a-141">-WhatIf</span></span>
<span data-ttu-id="9107a-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9107a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9107a-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9107a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9107a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9107a-144">CommonParameters</span></span>
<span data-ttu-id="9107a-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9107a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9107a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9107a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9107a-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9107a-147">INPUTS</span></span>

### <span data-ttu-id="9107a-148">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="9107a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="9107a-149">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="9107a-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="9107a-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9107a-150">OUTPUTS</span></span>

### <span data-ttu-id="9107a-151">Microsoft.Azure.Commands.Dosdb.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="9107a-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="9107a-152">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="9107a-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="9107a-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9107a-153">NOTES</span></span>

## <span data-ttu-id="9107a-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9107a-154">RELATED LINKS</span></span>
