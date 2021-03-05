---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: 64d6f0bd604e8074d593f20a572768b54ced8a59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960785"
---
# <span data-ttu-id="b69cf-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b69cf-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b69cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b69cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b69cf-103">Usuń konto WołodekDB.</span><span class="sxs-lookup"><span data-stu-id="b69cf-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="b69cf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b69cf-104">SYNTAX</span></span>

### <span data-ttu-id="b69cf-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b69cf-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b69cf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b69cf-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b69cf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b69cf-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b69cf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b69cf-108">DESCRIPTION</span></span>
<span data-ttu-id="b69cf-109">Usuń konto WołodekDB z podaną nazwą w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b69cf-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="b69cf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b69cf-110">EXAMPLES</span></span>

### <span data-ttu-id="b69cf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b69cf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="b69cf-112">Konto o nazwie konta o nazwie dbname w zasobie grupy zasobów zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="b69cf-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="b69cf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b69cf-113">PARAMETERS</span></span>

### <span data-ttu-id="b69cf-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b69cf-114">-AsJob</span></span>
<span data-ttu-id="b69cf-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b69cf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b69cf-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b69cf-116">-Confirm</span></span>
<span data-ttu-id="b69cf-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b69cf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b69cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69cf-118">-DefaultProfile</span></span>
<span data-ttu-id="b69cf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b69cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b69cf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b69cf-120">-InputObject</span></span>
<span data-ttu-id="b69cf-121">Obiekt Konto bazy danych</span><span class="sxs-lookup"><span data-stu-id="b69cf-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b69cf-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b69cf-122">-Name</span></span>
<span data-ttu-id="b69cf-123">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="b69cf-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b69cf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b69cf-124">-PassThru</span></span>
<span data-ttu-id="b69cf-125">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="b69cf-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b69cf-126">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="b69cf-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b69cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b69cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="b69cf-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b69cf-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b69cf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b69cf-129">-ResourceId</span></span>
<span data-ttu-id="b69cf-130">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="b69cf-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b69cf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b69cf-131">-WhatIf</span></span>
<span data-ttu-id="b69cf-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b69cf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b69cf-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b69cf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b69cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69cf-134">CommonParameters</span></span>
<span data-ttu-id="b69cf-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b69cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69cf-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b69cf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69cf-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b69cf-137">INPUTS</span></span>

### <span data-ttu-id="b69cf-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b69cf-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b69cf-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b69cf-139">OUTPUTS</span></span>

### <span data-ttu-id="b69cf-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b69cf-140">System.Void</span></span>

## <span data-ttu-id="b69cf-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b69cf-141">NOTES</span></span>

## <span data-ttu-id="b69cf-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b69cf-142">RELATED LINKS</span></span>
