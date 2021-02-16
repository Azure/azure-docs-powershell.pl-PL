---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243907"
---
# <span data-ttu-id="69dce-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="69dce-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="69dce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69dce-102">SYNOPSIS</span></span>
<span data-ttu-id="69dce-103">Usuwa wykres Gremlin Graph o formancie GrassDB.</span><span class="sxs-lookup"><span data-stu-id="69dce-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="69dce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69dce-104">SYNTAX</span></span>

### <span data-ttu-id="69dce-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="69dce-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69dce-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69dce-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69dce-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="69dce-107">DESCRIPTION</span></span>
<span data-ttu-id="69dce-108">Polecenie **cmdlet Remove-AzCosmosDBGremlinGraph** usuwa wykres Gremlin Graph o formancie Grasdb.</span><span class="sxs-lookup"><span data-stu-id="69dce-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="69dce-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69dce-109">EXAMPLES</span></span>

### <span data-ttu-id="69dce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69dce-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="69dce-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="69dce-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="69dce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69dce-112">PARAMETERS</span></span>

### <span data-ttu-id="69dce-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="69dce-113">-AccountName</span></span>
<span data-ttu-id="69dce-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="69dce-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="69dce-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69dce-115">-Confirm</span></span>
<span data-ttu-id="69dce-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69dce-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69dce-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69dce-117">-DatabaseName</span></span>
<span data-ttu-id="69dce-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="69dce-118">Database name.</span></span>

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

### <span data-ttu-id="69dce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dce-119">-DefaultProfile</span></span>
<span data-ttu-id="69dce-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69dce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69dce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69dce-121">-InputObject</span></span>
<span data-ttu-id="69dce-122">Obiekt Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="69dce-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69dce-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69dce-123">-Name</span></span>
<span data-ttu-id="69dce-124">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="69dce-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="69dce-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69dce-125">-PassThru</span></span>
<span data-ttu-id="69dce-126">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="69dce-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="69dce-127">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="69dce-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="69dce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69dce-128">-ResourceGroupName</span></span>
<span data-ttu-id="69dce-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69dce-129">Name of resource group.</span></span>

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

### <span data-ttu-id="69dce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69dce-130">-WhatIf</span></span>
<span data-ttu-id="69dce-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69dce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69dce-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69dce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69dce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dce-133">CommonParameters</span></span>
<span data-ttu-id="69dce-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69dce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dce-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69dce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dce-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69dce-136">INPUTS</span></span>

### <span data-ttu-id="69dce-137">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="69dce-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="69dce-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69dce-138">OUTPUTS</span></span>

### <span data-ttu-id="69dce-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="69dce-139">System.Void</span></span>

### <span data-ttu-id="69dce-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69dce-140">System.Boolean</span></span>

## <span data-ttu-id="69dce-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69dce-141">NOTES</span></span>

## <span data-ttu-id="69dce-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69dce-142">RELATED LINKS</span></span>
