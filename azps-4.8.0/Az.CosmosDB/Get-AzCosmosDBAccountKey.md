---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221844"
---
# <span data-ttu-id="350fb-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="350fb-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="350fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="350fb-102">SYNOPSIS</span></span>
<span data-ttu-id="350fb-103">Pobierz klucze {"ConnectionKeys", "PrimaryReadOnly" lub "Keys"} dla danego konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="350fb-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="350fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="350fb-104">SYNTAX</span></span>

### <span data-ttu-id="350fb-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="350fb-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="350fb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="350fb-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="350fb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="350fb-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="350fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="350fb-108">DESCRIPTION</span></span>
<span data-ttu-id="350fb-109">Pobieranie listy kluczy połączeń.</span><span class="sxs-lookup"><span data-stu-id="350fb-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="350fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="350fb-110">EXAMPLES</span></span>

### <span data-ttu-id="350fb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="350fb-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="350fb-112">Lista kluczy dla konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="350fb-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="350fb-113">Typem klucza może być wartość z: ConnectionStrings, Keys i ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="350fb-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="350fb-114">Wartość domyślna to Keys.</span><span class="sxs-lookup"><span data-stu-id="350fb-114">Default is Keys.</span></span>

## <span data-ttu-id="350fb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="350fb-115">PARAMETERS</span></span>

### <span data-ttu-id="350fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350fb-116">-DefaultProfile</span></span>
<span data-ttu-id="350fb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="350fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="350fb-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="350fb-118">-InputObject</span></span>
<span data-ttu-id="350fb-119">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="350fb-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="350fb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="350fb-120">-Name</span></span>
<span data-ttu-id="350fb-121">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="350fb-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="350fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="350fb-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="350fb-123">Name of resource group.</span></span>

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

### <span data-ttu-id="350fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="350fb-124">-ResourceId</span></span>
<span data-ttu-id="350fb-125">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="350fb-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="350fb-126">-Type</span><span class="sxs-lookup"><span data-stu-id="350fb-126">-Type</span></span>
<span data-ttu-id="350fb-127">Wartość z: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="350fb-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="350fb-128">Wartość domyślna to Keys.</span><span class="sxs-lookup"><span data-stu-id="350fb-128">Default is Keys.</span></span>

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

### <span data-ttu-id="350fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350fb-129">CommonParameters</span></span>
<span data-ttu-id="350fb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350fb-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="350fb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350fb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="350fb-132">INPUTS</span></span>

### <span data-ttu-id="350fb-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="350fb-133">None</span></span>

## <span data-ttu-id="350fb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="350fb-134">OUTPUTS</span></span>

### <span data-ttu-id="350fb-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="350fb-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="350fb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="350fb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="350fb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="350fb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="350fb-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="350fb-138">NOTES</span></span>

## <span data-ttu-id="350fb-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="350fb-139">RELATED LINKS</span></span>
