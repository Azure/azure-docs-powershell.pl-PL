---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 6df8d425967133e50dc45e44b6d567aca58465a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004385"
---
# <span data-ttu-id="9d556-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="9d556-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="9d556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d556-102">SYNOPSIS</span></span>
<span data-ttu-id="9d556-103">Pobierz konto DosyćDB.</span><span class="sxs-lookup"><span data-stu-id="9d556-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="9d556-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d556-104">SYNTAX</span></span>

### <span data-ttu-id="9d556-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9d556-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d556-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d556-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d556-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d556-107">DESCRIPTION</span></span>
<span data-ttu-id="9d556-108">Polecenie cmdlet **Get-AzCosmosDBAccount** pobiera listę wszystkich istniejących kont Wsad.</span><span class="sxs-lookup"><span data-stu-id="9d556-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="9d556-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d556-109">EXAMPLES</span></span>

### <span data-ttu-id="9d556-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d556-110">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="9d556-111">Pobierz konto bazy danych DossDB z nazwą databaseAccountName w resourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9d556-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="9d556-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d556-112">PARAMETERS</span></span>

### <span data-ttu-id="9d556-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d556-113">-DefaultProfile</span></span>
<span data-ttu-id="9d556-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d556-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d556-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d556-115">-Name</span></span>
<span data-ttu-id="9d556-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="9d556-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9d556-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d556-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d556-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d556-118">Name of resource group.</span></span>

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

### <span data-ttu-id="9d556-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d556-119">-ResourceId</span></span>
<span data-ttu-id="9d556-120">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d556-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="9d556-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d556-121">CommonParameters</span></span>
<span data-ttu-id="9d556-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d556-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d556-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d556-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d556-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d556-124">INPUTS</span></span>

### <span data-ttu-id="9d556-125">Brak</span><span class="sxs-lookup"><span data-stu-id="9d556-125">None</span></span>

## <span data-ttu-id="9d556-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d556-126">OUTPUTS</span></span>

### <span data-ttu-id="9d556-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9d556-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9d556-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d556-128">NOTES</span></span>

## <span data-ttu-id="9d556-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d556-129">RELATED LINKS</span></span>
