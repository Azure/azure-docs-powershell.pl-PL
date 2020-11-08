---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233168"
---
# <span data-ttu-id="8d8d6-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="8d8d6-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="8d8d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8d6-103">Pobiera szczegóły pojedynczego klastra centrum zdarzeń lub listę klastrów centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="8d8d6-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="8d8d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d8d6-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d8d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="8d8d6-106">Polecenie cmdlet Get-AzEventHubCluster zwraca informacje o klastrze centrum zdarzeń lub listę wszystkich klastrów centrum zdarzeń w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d8d6-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="8d8d6-107">W przypadku podanej nazwy klastra zostaną zwrócone szczegółowe dane dotyczące pojedynczego klastra.</span><span class="sxs-lookup"><span data-stu-id="8d8d6-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="8d8d6-108">Jeśli nie podano nazwy klastra, zostanie zwrócona lista wszystkich klastrów w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d8d6-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="8d8d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d8d6-109">EXAMPLES</span></span>

### <span data-ttu-id="8d8d6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8d8d6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="8d8d6-111">Zwraca detials klastra "Eventhub-5557" z grupy zasobów "RSG-Cluster27651".</span><span class="sxs-lookup"><span data-stu-id="8d8d6-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="8d8d6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d8d6-112">PARAMETERS</span></span>

### <span data-ttu-id="8d8d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8d6-113">-DefaultProfile</span></span>
<span data-ttu-id="8d8d6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d8d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d8d6-115">-Name</span></span>
<span data-ttu-id="8d8d6-116">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="8d8d6-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8d6-117">-ResourceGroupName</span></span>
<span data-ttu-id="8d8d6-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8d8d6-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8d6-119">CommonParameters</span></span>
<span data-ttu-id="8d8d6-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d8d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8d6-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d8d6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8d6-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d8d6-122">INPUTS</span></span>

### <span data-ttu-id="8d8d6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8d8d6-123">System.String</span></span>

## <span data-ttu-id="8d8d6-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d8d6-124">OUTPUTS</span></span>

### <span data-ttu-id="8d8d6-125">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8d8d6-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="8d8d6-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d8d6-126">NOTES</span></span>

## <span data-ttu-id="8d8d6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d8d6-127">RELATED LINKS</span></span>
