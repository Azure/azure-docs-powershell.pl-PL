---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 7e7ffd7c06217b4e2d12aaf75684c85f8ab12e9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983258"
---
# <span data-ttu-id="8354c-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="8354c-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="8354c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8354c-102">SYNOPSIS</span></span>
<span data-ttu-id="8354c-103">Usuwa funkcję Sql UserDefinedFunction języka Sql.</span><span class="sxs-lookup"><span data-stu-id="8354c-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="8354c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8354c-104">SYNTAX</span></span>

### <span data-ttu-id="8354c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8354c-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8354c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8354c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8354c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8354c-107">DESCRIPTION</span></span>
<span data-ttu-id="8354c-108">Polecenie cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** powoduje usunięcie właściwości AlegosDB Sql UserDefinedFunction odpowiadającej danej nazwie ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="8354c-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="8354c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8354c-109">EXAMPLES</span></span>

### <span data-ttu-id="8354c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8354c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="8354c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8354c-111">PARAMETERS</span></span>

### <span data-ttu-id="8354c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8354c-112">-AccountName</span></span>
<span data-ttu-id="8354c-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="8354c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8354c-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8354c-114">-Confirm</span></span>
<span data-ttu-id="8354c-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8354c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8354c-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8354c-116">-ContainerName</span></span>
<span data-ttu-id="8354c-117">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="8354c-117">Container name.</span></span>

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

### <span data-ttu-id="8354c-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8354c-118">-DatabaseName</span></span>
<span data-ttu-id="8354c-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8354c-119">Database name.</span></span>

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

### <span data-ttu-id="8354c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8354c-120">-DefaultProfile</span></span>
<span data-ttu-id="8354c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8354c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8354c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8354c-122">-InputObject</span></span>
<span data-ttu-id="8354c-123">Obiekt funkcji zdefiniowany przez użytkownika sql</span><span class="sxs-lookup"><span data-stu-id="8354c-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8354c-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8354c-124">-Name</span></span>
<span data-ttu-id="8354c-125">Nazwa funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8354c-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="8354c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8354c-126">-PassThru</span></span>
<span data-ttu-id="8354c-127">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="8354c-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="8354c-128">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="8354c-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="8354c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8354c-129">-ResourceGroupName</span></span>
<span data-ttu-id="8354c-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8354c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="8354c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8354c-131">-WhatIf</span></span>
<span data-ttu-id="8354c-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8354c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8354c-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8354c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8354c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8354c-134">CommonParameters</span></span>
<span data-ttu-id="8354c-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8354c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8354c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8354c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8354c-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8354c-137">INPUTS</span></span>

### <span data-ttu-id="8354c-138">Brak</span><span class="sxs-lookup"><span data-stu-id="8354c-138">None</span></span>

## <span data-ttu-id="8354c-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8354c-139">OUTPUTS</span></span>

### <span data-ttu-id="8354c-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="8354c-140">System.Void</span></span>

### <span data-ttu-id="8354c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8354c-141">System.Boolean</span></span>

## <span data-ttu-id="8354c-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8354c-142">NOTES</span></span>

## <span data-ttu-id="8354c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8354c-143">RELATED LINKS</span></span>
