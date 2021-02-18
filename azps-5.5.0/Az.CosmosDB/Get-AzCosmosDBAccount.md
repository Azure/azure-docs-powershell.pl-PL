---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181402"
---
# <span data-ttu-id="a3efb-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="a3efb-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="a3efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3efb-102">SYNOPSIS</span></span>
<span data-ttu-id="a3efb-103">Pobierz konto DosyćDB.</span><span class="sxs-lookup"><span data-stu-id="a3efb-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="a3efb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3efb-104">SYNTAX</span></span>

### <span data-ttu-id="a3efb-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a3efb-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3efb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3efb-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3efb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3efb-107">DESCRIPTION</span></span>
<span data-ttu-id="a3efb-108">Polecenie cmdlet **Get-AzCosmosDBAccount** pobiera listę wszystkich istniejących kont Wsad.</span><span class="sxs-lookup"><span data-stu-id="a3efb-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="a3efb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3efb-109">EXAMPLES</span></span>

### <span data-ttu-id="a3efb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3efb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="a3efb-111">Pobierz konto bazy danych DossDB z nazwą databaseAccountName w resourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a3efb-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="a3efb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3efb-112">PARAMETERS</span></span>

### <span data-ttu-id="a3efb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3efb-113">-DefaultProfile</span></span>
<span data-ttu-id="a3efb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3efb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3efb-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3efb-115">-Name</span></span>
<span data-ttu-id="a3efb-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="a3efb-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3efb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3efb-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3efb-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3efb-118">Name of resource group.</span></span>

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

### <span data-ttu-id="a3efb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3efb-119">-ResourceId</span></span>
<span data-ttu-id="a3efb-120">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="a3efb-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="a3efb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3efb-121">CommonParameters</span></span>
<span data-ttu-id="a3efb-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3efb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3efb-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3efb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3efb-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3efb-124">INPUTS</span></span>

### <span data-ttu-id="a3efb-125">Brak</span><span class="sxs-lookup"><span data-stu-id="a3efb-125">None</span></span>

## <span data-ttu-id="a3efb-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3efb-126">OUTPUTS</span></span>

### <span data-ttu-id="a3efb-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a3efb-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a3efb-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3efb-128">NOTES</span></span>

## <span data-ttu-id="a3efb-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3efb-129">RELATED LINKS</span></span>
