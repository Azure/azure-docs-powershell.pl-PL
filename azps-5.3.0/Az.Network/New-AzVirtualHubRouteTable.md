---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501238"
---
# <span data-ttu-id="6fd77-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fd77-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="6fd77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fd77-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd77-103">Tworzy obiekt tabeli tras wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd77-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="6fd77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fd77-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fd77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fd77-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd77-106">Tworzy obiekt tabeli tras wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd77-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="6fd77-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fd77-107">EXAMPLES</span></span>

### <span data-ttu-id="6fd77-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fd77-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="6fd77-109">Powyższa grupa utworzy tabelę tras składającą się z wielu tras i dołączonych do nowego koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6fd77-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="6fd77-110">Jest to obiekt w pamięci, za pomocą którego można dodać tabelę tras do nowego lub istniejącego VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="6fd77-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="6fd77-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fd77-111">PARAMETERS</span></span>

### <span data-ttu-id="6fd77-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd77-112">-DefaultProfile</span></span>
<span data-ttu-id="6fd77-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd77-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd77-114">-Route</span><span class="sxs-lookup"><span data-stu-id="6fd77-114">-Route</span></span>
<span data-ttu-id="6fd77-115">Lista tras koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6fd77-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd77-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd77-116">CommonParameters</span></span>
<span data-ttu-id="6fd77-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd77-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd77-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd77-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd77-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fd77-119">INPUTS</span></span>

### <span data-ttu-id="6fd77-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6fd77-120">None</span></span>

## <span data-ttu-id="6fd77-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fd77-121">OUTPUTS</span></span>

### <span data-ttu-id="6fd77-122">Microsoft. Azure. Commands. Network. models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6fd77-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="6fd77-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fd77-123">NOTES</span></span>

## <span data-ttu-id="6fd77-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fd77-124">RELATED LINKS</span></span>

[<span data-ttu-id="6fd77-125">Nowe — AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6fd77-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
