---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196339"
---
# <span data-ttu-id="67a0d-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="67a0d-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="67a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="67a0d-103">Pobiera szczegółowe informacje dotyczące pojedynczego klastra w aplikacji Eventhub lub listy klastrów w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="67a0d-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="67a0d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67a0d-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67a0d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="67a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="67a0d-106">Lista Get-AzEventHubClustersAvailableRegion cmdlet regionów, w których można tworzyć dedykowane obszary.</span><span class="sxs-lookup"><span data-stu-id="67a0d-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="67a0d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="67a0d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67a0d-108">Example 1</span></span>
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

<span data-ttu-id="67a0d-109">Zwracana jest lista regionów, w których</span><span class="sxs-lookup"><span data-stu-id="67a0d-109">List of regions is returned where</span></span>

## <span data-ttu-id="67a0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67a0d-110">PARAMETERS</span></span>

### <span data-ttu-id="67a0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a0d-111">-DefaultProfile</span></span>
<span data-ttu-id="67a0d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67a0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67a0d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a0d-113">CommonParameters</span></span>
<span data-ttu-id="67a0d-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a0d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a0d-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67a0d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a0d-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a0d-116">INPUTS</span></span>

### <span data-ttu-id="67a0d-117">Brak</span><span class="sxs-lookup"><span data-stu-id="67a0d-117">None</span></span>

## <span data-ttu-id="67a0d-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67a0d-118">OUTPUTS</span></span>

### <span data-ttu-id="67a0d-119">System.Collections.generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlet.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="67a0d-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="67a0d-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67a0d-120">NOTES</span></span>

## <span data-ttu-id="67a0d-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67a0d-121">RELATED LINKS</span></span>
