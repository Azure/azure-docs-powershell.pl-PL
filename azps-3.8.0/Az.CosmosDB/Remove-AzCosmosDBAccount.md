---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: e9ec1f1626a1fb4335c6e5df43a96727692538c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052681"
---
# <span data-ttu-id="daa94-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="daa94-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="daa94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="daa94-102">SYNOPSIS</span></span>
<span data-ttu-id="daa94-103">Usuwanie konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="daa94-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="daa94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="daa94-104">SYNTAX</span></span>

### <span data-ttu-id="daa94-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="daa94-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daa94-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="daa94-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daa94-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daa94-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa94-108">Opis</span><span class="sxs-lookup"><span data-stu-id="daa94-108">DESCRIPTION</span></span>
<span data-ttu-id="daa94-109">Usuń konto CosmosDB o podanej nazwie w danym przystawce zasobów.</span><span class="sxs-lookup"><span data-stu-id="daa94-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="daa94-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="daa94-110">EXAMPLES</span></span>

### <span data-ttu-id="daa94-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="daa94-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="daa94-112">Konto o nazwie dbname (nazwa konta) w RG.</span><span class="sxs-lookup"><span data-stu-id="daa94-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="daa94-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="daa94-113">PARAMETERS</span></span>

### <span data-ttu-id="daa94-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daa94-114">-AsJob</span></span>
<span data-ttu-id="daa94-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="daa94-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="daa94-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="daa94-116">-Confirm</span></span>
<span data-ttu-id="daa94-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa94-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa94-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa94-118">-DefaultProfile</span></span>
<span data-ttu-id="daa94-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="daa94-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa94-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="daa94-120">-InputObject</span></span>
<span data-ttu-id="daa94-121">Obiekt konta bazy danych</span><span class="sxs-lookup"><span data-stu-id="daa94-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daa94-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="daa94-122">-Name</span></span>
<span data-ttu-id="daa94-123">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="daa94-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="daa94-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="daa94-124">-PassThru</span></span>
<span data-ttu-id="daa94-125">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="daa94-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="daa94-126">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="daa94-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="daa94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa94-127">-ResourceGroupName</span></span>
<span data-ttu-id="daa94-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="daa94-128">Name of resource group.</span></span>

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

### <span data-ttu-id="daa94-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daa94-129">-ResourceId</span></span>
<span data-ttu-id="daa94-130">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="daa94-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="daa94-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa94-131">-WhatIf</span></span>
<span data-ttu-id="daa94-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa94-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daa94-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="daa94-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa94-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa94-134">CommonParameters</span></span>
<span data-ttu-id="daa94-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa94-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa94-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daa94-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa94-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daa94-137">INPUTS</span></span>

### <span data-ttu-id="daa94-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="daa94-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="daa94-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="daa94-139">OUTPUTS</span></span>

### <span data-ttu-id="daa94-140">System. void</span><span class="sxs-lookup"><span data-stu-id="daa94-140">System.Void</span></span>

## <span data-ttu-id="daa94-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="daa94-141">NOTES</span></span>

## <span data-ttu-id="daa94-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daa94-142">RELATED LINKS</span></span>
