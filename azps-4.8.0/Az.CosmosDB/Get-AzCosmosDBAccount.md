---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221845"
---
# <span data-ttu-id="296da-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="296da-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="296da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="296da-102">SYNOPSIS</span></span>
<span data-ttu-id="296da-103">Uzyskaj konto CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="296da-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="296da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="296da-104">SYNTAX</span></span>

### <span data-ttu-id="296da-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="296da-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="296da-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="296da-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="296da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="296da-107">DESCRIPTION</span></span>
<span data-ttu-id="296da-108">Polecenie cmdlet **Get-AzCosmosDBAccount** pobiera listę wszystkich istniejących kont CosmosDB dla danego ResourceGroupName i pobiera pojedyncze konto CosmosDB dla danego ResourceGroupName i konta.</span><span class="sxs-lookup"><span data-stu-id="296da-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="296da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="296da-109">EXAMPLES</span></span>

### <span data-ttu-id="296da-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="296da-110">Example 1</span></span>
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

<span data-ttu-id="296da-111">Pobierz konto bazy danych CosmosDB z nazwą databaseAccountName w polu resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="296da-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="296da-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="296da-112">PARAMETERS</span></span>

### <span data-ttu-id="296da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296da-113">-DefaultProfile</span></span>
<span data-ttu-id="296da-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="296da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="296da-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="296da-115">-Name</span></span>
<span data-ttu-id="296da-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="296da-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="296da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="296da-117">-ResourceGroupName</span></span>
<span data-ttu-id="296da-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="296da-118">Name of resource group.</span></span>

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

### <span data-ttu-id="296da-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="296da-119">-ResourceId</span></span>
<span data-ttu-id="296da-120">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="296da-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="296da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296da-121">CommonParameters</span></span>
<span data-ttu-id="296da-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="296da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296da-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="296da-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296da-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="296da-124">INPUTS</span></span>

### <span data-ttu-id="296da-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="296da-125">None</span></span>

## <span data-ttu-id="296da-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="296da-126">OUTPUTS</span></span>

### <span data-ttu-id="296da-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="296da-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="296da-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="296da-128">NOTES</span></span>

## <span data-ttu-id="296da-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="296da-129">RELATED LINKS</span></span>
