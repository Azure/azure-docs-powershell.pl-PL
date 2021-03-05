---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: e6bead229b8ee37c4b63d3f20ebdfdf55b281e80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983265"
---
# <span data-ttu-id="40fcf-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="40fcf-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="40fcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="40fcf-103">Usuwa wyzwalacz języka SQL Dla firmy azwę języka SQL.</span><span class="sxs-lookup"><span data-stu-id="40fcf-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="40fcf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40fcf-104">SYNTAX</span></span>

### <span data-ttu-id="40fcf-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40fcf-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40fcf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40fcf-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40fcf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="40fcf-107">DESCRIPTION</span></span>
<span data-ttu-id="40fcf-108">Polecenie **cmdlet Remove-AzCosmosDBSqlTrigger** powoduje usunięcie wyzwalacza sql DoscDb odpowiadającego podanej nazwie ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="40fcf-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="40fcf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40fcf-109">EXAMPLES</span></span>

### <span data-ttu-id="40fcf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="40fcf-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="40fcf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40fcf-111">PARAMETERS</span></span>

### <span data-ttu-id="40fcf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40fcf-112">-AccountName</span></span>
<span data-ttu-id="40fcf-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="40fcf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40fcf-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40fcf-114">-Confirm</span></span>
<span data-ttu-id="40fcf-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="40fcf-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40fcf-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="40fcf-116">-ContainerName</span></span>
<span data-ttu-id="40fcf-117">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="40fcf-117">Container name.</span></span>

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

### <span data-ttu-id="40fcf-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40fcf-118">-DatabaseName</span></span>
<span data-ttu-id="40fcf-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="40fcf-119">Database name.</span></span>

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

### <span data-ttu-id="40fcf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fcf-120">-DefaultProfile</span></span>
<span data-ttu-id="40fcf-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40fcf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40fcf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40fcf-122">-InputObject</span></span>
<span data-ttu-id="40fcf-123">Obiekt wyzwalacza języka Sql</span><span class="sxs-lookup"><span data-stu-id="40fcf-123">Sql trigger Object</span></span>

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

### <span data-ttu-id="40fcf-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="40fcf-124">-Name</span></span>
<span data-ttu-id="40fcf-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="40fcf-125">Trigger name.</span></span>

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

### <span data-ttu-id="40fcf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40fcf-126">-PassThru</span></span>
<span data-ttu-id="40fcf-127">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="40fcf-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="40fcf-128">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="40fcf-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fcf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40fcf-129">-ResourceGroupName</span></span>
<span data-ttu-id="40fcf-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40fcf-130">Name of resource group.</span></span>

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

### <span data-ttu-id="40fcf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40fcf-131">-WhatIf</span></span>
<span data-ttu-id="40fcf-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40fcf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40fcf-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="40fcf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40fcf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fcf-134">CommonParameters</span></span>
<span data-ttu-id="40fcf-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40fcf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fcf-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40fcf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fcf-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40fcf-137">INPUTS</span></span>

### <span data-ttu-id="40fcf-138">Brak</span><span class="sxs-lookup"><span data-stu-id="40fcf-138">None</span></span>

## <span data-ttu-id="40fcf-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40fcf-139">OUTPUTS</span></span>

### <span data-ttu-id="40fcf-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="40fcf-140">System.Void</span></span>

### <span data-ttu-id="40fcf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40fcf-141">System.Boolean</span></span>

## <span data-ttu-id="40fcf-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40fcf-142">NOTES</span></span>

## <span data-ttu-id="40fcf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40fcf-143">RELATED LINKS</span></span>
