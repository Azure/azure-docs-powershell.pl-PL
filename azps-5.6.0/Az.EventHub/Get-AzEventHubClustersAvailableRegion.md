---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 633881b298059c35a54591bb1ff93d4e93a267d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954714"
---
# <span data-ttu-id="c48e9-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="c48e9-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="c48e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c48e9-103">Pobiera szczegółowe informacje dotyczące pojedynczego klastra aplikacji Eventhub lub listy klastrów w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c48e9-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="c48e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c48e9-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c48e9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c48e9-105">DESCRIPTION</span></span>
<span data-ttu-id="c48e9-106">Lista Get-AzEventHubClustersAvailableRegion cmdlet regionów, w których można tworzyć dedykowane obszary.</span><span class="sxs-lookup"><span data-stu-id="c48e9-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="c48e9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c48e9-107">EXAMPLES</span></span>

### <span data-ttu-id="c48e9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c48e9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="c48e9-109">Lista regionów jest zwracana w miejscu</span><span class="sxs-lookup"><span data-stu-id="c48e9-109">List of regions is returned where</span></span>

## <span data-ttu-id="c48e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c48e9-110">PARAMETERS</span></span>

### <span data-ttu-id="c48e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48e9-111">-DefaultProfile</span></span>
<span data-ttu-id="c48e9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c48e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48e9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48e9-113">CommonParameters</span></span>
<span data-ttu-id="c48e9-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48e9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48e9-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c48e9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48e9-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c48e9-116">INPUTS</span></span>

### <span data-ttu-id="c48e9-117">Brak</span><span class="sxs-lookup"><span data-stu-id="c48e9-117">None</span></span>

## <span data-ttu-id="c48e9-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c48e9-118">OUTPUTS</span></span>

### <span data-ttu-id="c48e9-119">System.Collections.generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlet.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c48e9-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c48e9-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c48e9-120">NOTES</span></span>

## <span data-ttu-id="c48e9-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c48e9-121">RELATED LINKS</span></span>
