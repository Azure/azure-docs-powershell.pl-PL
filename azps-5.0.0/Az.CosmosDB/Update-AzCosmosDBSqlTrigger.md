---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306733"
---
# <span data-ttu-id="e776d-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="e776d-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="e776d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e776d-102">SYNOPSIS</span></span>
<span data-ttu-id="e776d-103">Umożliwia zaktualizowanie wyzwalacza SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e776d-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="e776d-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejący wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="e776d-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="e776d-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e776d-105">SYNTAX</span></span>

### <span data-ttu-id="e776d-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e776d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e776d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e776d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e776d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e776d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e776d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e776d-109">DESCRIPTION</span></span>
<span data-ttu-id="e776d-110">Umożliwia zaktualizowanie wyzwalacza SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e776d-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="e776d-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejący wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="e776d-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="e776d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e776d-112">EXAMPLES</span></span>

### <span data-ttu-id="e776d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e776d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="e776d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e776d-114">PARAMETERS</span></span>

### <span data-ttu-id="e776d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e776d-115">-AccountName</span></span>
<span data-ttu-id="e776d-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e776d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e776d-117">-Body</span><span class="sxs-lookup"><span data-stu-id="e776d-117">-Body</span></span>
<span data-ttu-id="e776d-118">Treść wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e776d-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="e776d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e776d-119">-Confirm</span></span>
<span data-ttu-id="e776d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e776d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e776d-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e776d-121">-ContainerName</span></span>
<span data-ttu-id="e776d-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="e776d-122">Container name.</span></span>

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

### <span data-ttu-id="e776d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e776d-123">-DatabaseName</span></span>
<span data-ttu-id="e776d-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e776d-124">Database name.</span></span>

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

### <span data-ttu-id="e776d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e776d-125">-DefaultProfile</span></span>
<span data-ttu-id="e776d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e776d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e776d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e776d-127">-InputObject</span></span>
<span data-ttu-id="e776d-128">Obiekt wyzwalacza SQL</span><span class="sxs-lookup"><span data-stu-id="e776d-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="e776d-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e776d-129">-Name</span></span>
<span data-ttu-id="e776d-130">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e776d-130">Trigger name.</span></span>

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

### <span data-ttu-id="e776d-131">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e776d-131">-ParentObject</span></span>
<span data-ttu-id="e776d-132">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="e776d-132">Sql Container object.</span></span>

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

### <span data-ttu-id="e776d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e776d-133">-ResourceGroupName</span></span>
<span data-ttu-id="e776d-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e776d-134">Name of resource group.</span></span>

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

### <span data-ttu-id="e776d-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="e776d-135">-TriggerOperation</span></span>
<span data-ttu-id="e776d-136">Operacja, z którą jest skojarzony wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="e776d-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="e776d-137">Możliwe wartości to: "wszystko", "Utwórz", "Aktualizuj", "Usuń", "Zamień".</span><span class="sxs-lookup"><span data-stu-id="e776d-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="e776d-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="e776d-138">-TriggerType</span></span>
<span data-ttu-id="e776d-139">Typ wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e776d-139">Type of the Trigger.</span></span>
<span data-ttu-id="e776d-140">Możliwe są następujące wartości: "pre", "post"</span><span class="sxs-lookup"><span data-stu-id="e776d-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="e776d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e776d-141">-WhatIf</span></span>
<span data-ttu-id="e776d-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e776d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e776d-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e776d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e776d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e776d-144">CommonParameters</span></span>
<span data-ttu-id="e776d-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e776d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e776d-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e776d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e776d-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e776d-147">INPUTS</span></span>

### <span data-ttu-id="e776d-148">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e776d-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e776d-149">Microsoft. Azure. Commands. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="e776d-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="e776d-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e776d-150">OUTPUTS</span></span>

### <span data-ttu-id="e776d-151">Microsoft. Azure. Commands. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="e776d-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="e776d-152">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e776d-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e776d-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e776d-153">NOTES</span></span>

## <span data-ttu-id="e776d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e776d-154">RELATED LINKS</span></span>
