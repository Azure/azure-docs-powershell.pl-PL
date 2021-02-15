---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196755"
---
# <span data-ttu-id="e971c-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e971c-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e971c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e971c-102">SYNOPSIS</span></span>
<span data-ttu-id="e971c-103">Usuń konto WołodekDB.</span><span class="sxs-lookup"><span data-stu-id="e971c-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="e971c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e971c-104">SYNTAX</span></span>

### <span data-ttu-id="e971c-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e971c-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e971c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e971c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e971c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e971c-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e971c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e971c-108">DESCRIPTION</span></span>
<span data-ttu-id="e971c-109">Usuń konto WołodekDB z podaną nazwą w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e971c-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="e971c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e971c-110">EXAMPLES</span></span>

### <span data-ttu-id="e971c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e971c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="e971c-112">Konto o nazwie konta o nazwie dbname w zasobie grupy zasobów zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="e971c-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="e971c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e971c-113">PARAMETERS</span></span>

### <span data-ttu-id="e971c-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e971c-114">-AsJob</span></span>
<span data-ttu-id="e971c-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e971c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e971c-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e971c-116">-Confirm</span></span>
<span data-ttu-id="e971c-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e971c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e971c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e971c-118">-DefaultProfile</span></span>
<span data-ttu-id="e971c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e971c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e971c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e971c-120">-InputObject</span></span>
<span data-ttu-id="e971c-121">Obiekt Konto bazy danych</span><span class="sxs-lookup"><span data-stu-id="e971c-121">The Database Account object</span></span>

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

### <span data-ttu-id="e971c-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e971c-122">-Name</span></span>
<span data-ttu-id="e971c-123">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="e971c-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e971c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e971c-124">-PassThru</span></span>
<span data-ttu-id="e971c-125">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="e971c-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e971c-126">Wynik jest prawdziwy, jeśli operacja powiodła się, a w przypadku jej wystąpienia zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="e971c-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e971c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e971c-127">-ResourceGroupName</span></span>
<span data-ttu-id="e971c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e971c-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e971c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e971c-129">-ResourceId</span></span>
<span data-ttu-id="e971c-130">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="e971c-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="e971c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e971c-131">-WhatIf</span></span>
<span data-ttu-id="e971c-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e971c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e971c-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e971c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e971c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e971c-134">CommonParameters</span></span>
<span data-ttu-id="e971c-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e971c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e971c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e971c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e971c-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e971c-137">INPUTS</span></span>

### <span data-ttu-id="e971c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e971c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e971c-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e971c-139">OUTPUTS</span></span>

### <span data-ttu-id="e971c-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="e971c-140">System.Void</span></span>

## <span data-ttu-id="e971c-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e971c-141">NOTES</span></span>

## <span data-ttu-id="e971c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e971c-142">RELATED LINKS</span></span>
