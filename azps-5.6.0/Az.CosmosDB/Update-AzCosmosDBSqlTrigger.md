---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: bebf801316d18b29f6444b0b369833ae547e78d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009729"
---
# <span data-ttu-id="29dee-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="29dee-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="29dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29dee-102">SYNOPSIS</span></span>
<span data-ttu-id="29dee-103">Aktualizacja wyzwalacza sql dla firmy JavasDB.</span><span class="sxs-lookup"><span data-stu-id="29dee-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="29dee-104">Wykonuje operację poprawki po stronie klienta, czytając istniejący wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="29dee-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="29dee-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29dee-105">SYNTAX</span></span>

### <span data-ttu-id="29dee-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="29dee-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29dee-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29dee-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29dee-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29dee-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29dee-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="29dee-109">DESCRIPTION</span></span>
<span data-ttu-id="29dee-110">Aktualizacja wyzwalacza sql dla firmy JavasDB.</span><span class="sxs-lookup"><span data-stu-id="29dee-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="29dee-111">Wykonuje operację poprawki po stronie klienta, czytając istniejący wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="29dee-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="29dee-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29dee-112">EXAMPLES</span></span>

### <span data-ttu-id="29dee-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29dee-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="29dee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29dee-114">PARAMETERS</span></span>

### <span data-ttu-id="29dee-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="29dee-115">-AccountName</span></span>
<span data-ttu-id="29dee-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="29dee-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="29dee-117">— Treść</span><span class="sxs-lookup"><span data-stu-id="29dee-117">-Body</span></span>
<span data-ttu-id="29dee-118">Treść wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="29dee-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="29dee-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29dee-119">-Confirm</span></span>
<span data-ttu-id="29dee-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29dee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29dee-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="29dee-121">-ContainerName</span></span>
<span data-ttu-id="29dee-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="29dee-122">Container name.</span></span>

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

### <span data-ttu-id="29dee-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29dee-123">-DatabaseName</span></span>
<span data-ttu-id="29dee-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="29dee-124">Database name.</span></span>

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

### <span data-ttu-id="29dee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dee-125">-DefaultProfile</span></span>
<span data-ttu-id="29dee-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29dee-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29dee-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29dee-127">-InputObject</span></span>
<span data-ttu-id="29dee-128">Obiekt wyzwalacza języka Sql</span><span class="sxs-lookup"><span data-stu-id="29dee-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="29dee-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29dee-129">-Name</span></span>
<span data-ttu-id="29dee-130">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="29dee-130">Trigger name.</span></span>

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

### <span data-ttu-id="29dee-131">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="29dee-131">-ParentObject</span></span>
<span data-ttu-id="29dee-132">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="29dee-132">Sql Container object.</span></span>

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

### <span data-ttu-id="29dee-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dee-133">-ResourceGroupName</span></span>
<span data-ttu-id="29dee-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29dee-134">Name of resource group.</span></span>

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

### <span data-ttu-id="29dee-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="29dee-135">-TriggerOperation</span></span>
<span data-ttu-id="29dee-136">Operacja, z pomocą która jest skojarzona z wyzwalaczem.</span><span class="sxs-lookup"><span data-stu-id="29dee-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="29dee-137">Możliwe wartości: "Wszystko", "Utwórz", "Aktualizacja", "Usuń", "Zamień"</span><span class="sxs-lookup"><span data-stu-id="29dee-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="29dee-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="29dee-138">-TriggerType</span></span>
<span data-ttu-id="29dee-139">Typ wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="29dee-139">Type of the Trigger.</span></span>
<span data-ttu-id="29dee-140">Możliwe wartości: "Przed", "Opublikuj"</span><span class="sxs-lookup"><span data-stu-id="29dee-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="29dee-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dee-141">-WhatIf</span></span>
<span data-ttu-id="29dee-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29dee-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29dee-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="29dee-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29dee-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dee-144">CommonParameters</span></span>
<span data-ttu-id="29dee-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29dee-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dee-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29dee-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dee-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29dee-147">INPUTS</span></span>

### <span data-ttu-id="29dee-148">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="29dee-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="29dee-149">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="29dee-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="29dee-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29dee-150">OUTPUTS</span></span>

### <span data-ttu-id="29dee-151">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="29dee-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="29dee-152">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="29dee-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="29dee-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29dee-153">NOTES</span></span>

## <span data-ttu-id="29dee-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29dee-154">RELATED LINKS</span></span>
