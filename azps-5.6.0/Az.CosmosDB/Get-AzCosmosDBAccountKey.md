---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: c143fed64e99dd9f564b4375c4ef20e5b5ad4354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983729"
---
# <span data-ttu-id="fe35c-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="fe35c-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="fe35c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe35c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe35c-103">Pobierz klucze{"ConnectionKeys", "PrimaryReadOnly" lub "Keys"} dla danego konta DanychSDB.</span><span class="sxs-lookup"><span data-stu-id="fe35c-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="fe35c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe35c-104">SYNTAX</span></span>

### <span data-ttu-id="fe35c-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fe35c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe35c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe35c-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe35c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe35c-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe35c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe35c-108">DESCRIPTION</span></span>
<span data-ttu-id="fe35c-109">Pobierz listę klawiszy połączeń.</span><span class="sxs-lookup"><span data-stu-id="fe35c-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="fe35c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe35c-110">EXAMPLES</span></span>

### <span data-ttu-id="fe35c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe35c-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="fe35c-112">Wyświetla listę kluczy dla konta AADB.</span><span class="sxs-lookup"><span data-stu-id="fe35c-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="fe35c-113">Typem klucza może być wartość z: ConnectionStrings, Keys and ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="fe35c-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="fe35c-114">Wartością domyślną są klawisze.</span><span class="sxs-lookup"><span data-stu-id="fe35c-114">Default is Keys.</span></span>

## <span data-ttu-id="fe35c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe35c-115">PARAMETERS</span></span>

### <span data-ttu-id="fe35c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe35c-116">-DefaultProfile</span></span>
<span data-ttu-id="fe35c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe35c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe35c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe35c-118">-InputObject</span></span>
<span data-ttu-id="fe35c-119">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="fe35c-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fe35c-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe35c-120">-Name</span></span>
<span data-ttu-id="fe35c-121">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="fe35c-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fe35c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe35c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe35c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe35c-123">Name of resource group.</span></span>

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

### <span data-ttu-id="fe35c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe35c-124">-ResourceId</span></span>
<span data-ttu-id="fe35c-125">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="fe35c-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="fe35c-126">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="fe35c-126">-Type</span></span>
<span data-ttu-id="fe35c-127">Wartość od: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="fe35c-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="fe35c-128">Wartością domyślną są klawisze.</span><span class="sxs-lookup"><span data-stu-id="fe35c-128">Default is Keys.</span></span>

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

### <span data-ttu-id="fe35c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe35c-129">CommonParameters</span></span>
<span data-ttu-id="fe35c-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe35c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe35c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe35c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe35c-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe35c-132">INPUTS</span></span>

### <span data-ttu-id="fe35c-133">Brak</span><span class="sxs-lookup"><span data-stu-id="fe35c-133">None</span></span>

## <span data-ttu-id="fe35c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe35c-134">OUTPUTS</span></span>

### <span data-ttu-id="fe35c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="fe35c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="fe35c-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="fe35c-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="fe35c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="fe35c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="fe35c-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe35c-138">NOTES</span></span>

## <span data-ttu-id="fe35c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe35c-139">RELATED LINKS</span></span>
