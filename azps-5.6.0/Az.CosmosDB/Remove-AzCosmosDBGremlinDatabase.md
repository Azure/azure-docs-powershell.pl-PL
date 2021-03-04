---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 2a09582c57cdb06dea955dcbd1c4728b822d229c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971322"
---
# <span data-ttu-id="6df33-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="6df33-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="6df33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6df33-102">SYNOPSIS</span></span>
<span data-ttu-id="6df33-103">Usuwa bazę danych Grasdb Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6df33-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="6df33-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6df33-104">SYNTAX</span></span>

### <span data-ttu-id="6df33-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6df33-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df33-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6df33-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6df33-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6df33-107">DESCRIPTION</span></span>
<span data-ttu-id="6df33-108">Polecenie **cmdlet Remove-AzCosmosDBGremlinDatabase** usuwa bazę danych GrysDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6df33-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="6df33-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6df33-109">EXAMPLES</span></span>

### <span data-ttu-id="6df33-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6df33-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="6df33-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="6df33-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="6df33-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6df33-112">PARAMETERS</span></span>

### <span data-ttu-id="6df33-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6df33-113">-AccountName</span></span>
<span data-ttu-id="6df33-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="6df33-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6df33-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6df33-115">-Confirm</span></span>
<span data-ttu-id="6df33-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6df33-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df33-117">-DefaultProfile</span></span>
<span data-ttu-id="6df33-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6df33-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df33-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6df33-119">-InputObject</span></span>
<span data-ttu-id="6df33-120">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6df33-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6df33-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6df33-121">-Name</span></span>
<span data-ttu-id="6df33-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6df33-122">Database name.</span></span>

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

### <span data-ttu-id="6df33-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6df33-123">-PassThru</span></span>
<span data-ttu-id="6df33-124">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="6df33-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="6df33-125">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="6df33-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="6df33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df33-126">-ResourceGroupName</span></span>
<span data-ttu-id="6df33-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6df33-127">Name of resource group.</span></span>

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

### <span data-ttu-id="6df33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df33-128">-WhatIf</span></span>
<span data-ttu-id="6df33-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6df33-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df33-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6df33-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df33-131">CommonParameters</span></span>
<span data-ttu-id="6df33-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df33-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6df33-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df33-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6df33-134">INPUTS</span></span>

### <span data-ttu-id="6df33-135">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6df33-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="6df33-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6df33-136">OUTPUTS</span></span>

### <span data-ttu-id="6df33-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="6df33-137">System.Void</span></span>

### <span data-ttu-id="6df33-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6df33-138">System.Boolean</span></span>

## <span data-ttu-id="6df33-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6df33-139">NOTES</span></span>

## <span data-ttu-id="6df33-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6df33-140">RELATED LINKS</span></span>
