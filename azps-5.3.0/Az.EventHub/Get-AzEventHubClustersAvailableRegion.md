---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387060"
---
# <span data-ttu-id="ae5d2-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="ae5d2-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="ae5d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5d2-103">Pobiera szczegóły pojedynczego klastra Eventhub lub listy klastrów w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="ae5d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae5d2-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae5d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae5d2-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5d2-106">Lista Get-AzEventHubClustersAvailableRegion polecenia cmdlet, w której można tworzyć dedykowane regiony.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="ae5d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae5d2-107">EXAMPLES</span></span>

### <span data-ttu-id="ae5d2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae5d2-108">Example 1</span></span>
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

<span data-ttu-id="ae5d2-109">Lista regionów jest zwracana w miejscu, w którym</span><span class="sxs-lookup"><span data-stu-id="ae5d2-109">List of regions is returned where</span></span>

## <span data-ttu-id="ae5d2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae5d2-110">PARAMETERS</span></span>

### <span data-ttu-id="ae5d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5d2-111">-DefaultProfile</span></span>
<span data-ttu-id="ae5d2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae5d2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5d2-113">CommonParameters</span></span>
<span data-ttu-id="ae5d2-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5d2-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae5d2-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5d2-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae5d2-116">INPUTS</span></span>

### <span data-ttu-id="ae5d2-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ae5d2-117">None</span></span>

## <span data-ttu-id="ae5d2-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae5d2-118">OUTPUTS</span></span>

### <span data-ttu-id="ae5d2-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. EventHub. Framework. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. PowerShell.. EventHub, Version = 1.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ae5d2-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ae5d2-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae5d2-120">NOTES</span></span>

## <span data-ttu-id="ae5d2-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae5d2-121">RELATED LINKS</span></span>
