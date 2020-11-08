---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050883"
---
# <span data-ttu-id="11750-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="11750-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="11750-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11750-102">SYNOPSIS</span></span>
<span data-ttu-id="11750-103">Ponowne generowanie danego klucza konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="11750-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="11750-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11750-104">SYNTAX</span></span>

### <span data-ttu-id="11750-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11750-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11750-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11750-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11750-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11750-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11750-108">Opis</span><span class="sxs-lookup"><span data-stu-id="11750-108">DESCRIPTION</span></span>
<span data-ttu-id="11750-109">Utwórz nowe konto usługi CosmosDB w danym przystawce zasobów.</span><span class="sxs-lookup"><span data-stu-id="11750-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="11750-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11750-110">EXAMPLES</span></span>

### <span data-ttu-id="11750-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11750-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="11750-112">Nowe klucze są generowane dla konta o nazwie dbname (nazwa konta) w RG.</span><span class="sxs-lookup"><span data-stu-id="11750-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="11750-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11750-113">PARAMETERS</span></span>

### <span data-ttu-id="11750-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11750-114">-AsJob</span></span>
<span data-ttu-id="11750-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="11750-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11750-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11750-116">-Confirm</span></span>
<span data-ttu-id="11750-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11750-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11750-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11750-118">-DefaultProfile</span></span>
<span data-ttu-id="11750-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11750-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11750-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11750-120">-InputObject</span></span>
<span data-ttu-id="11750-121">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="11750-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="11750-122">-Rodzaj</span><span class="sxs-lookup"><span data-stu-id="11750-122">-KeyKind</span></span>
<span data-ttu-id="11750-123">Klawisz dostępu do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="11750-123">The access key to regenerate.</span></span>
<span data-ttu-id="11750-124">Akceptowane wartości: podstawowe, primaryReadonly, dodatkowe, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="11750-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

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

### <span data-ttu-id="11750-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11750-125">-Name</span></span>
<span data-ttu-id="11750-126">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="11750-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="11750-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11750-127">-ResourceGroupName</span></span>
<span data-ttu-id="11750-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11750-128">Name of resource group.</span></span>

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

### <span data-ttu-id="11750-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11750-129">-ResourceId</span></span>
<span data-ttu-id="11750-130">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="11750-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="11750-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11750-131">-WhatIf</span></span>
<span data-ttu-id="11750-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11750-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11750-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11750-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11750-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11750-134">CommonParameters</span></span>
<span data-ttu-id="11750-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11750-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11750-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11750-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11750-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11750-137">INPUTS</span></span>

### <span data-ttu-id="11750-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="11750-138">None</span></span>

## <span data-ttu-id="11750-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11750-139">OUTPUTS</span></span>

### <span data-ttu-id="11750-140">System. void</span><span class="sxs-lookup"><span data-stu-id="11750-140">System.Void</span></span>

## <span data-ttu-id="11750-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11750-141">NOTES</span></span>

## <span data-ttu-id="11750-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11750-142">RELATED LINKS</span></span>
