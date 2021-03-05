---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016170"
---
# <span data-ttu-id="467e2-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="467e2-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="467e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="467e2-102">SYNOPSIS</span></span>
<span data-ttu-id="467e2-103">Aktualizuje prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="467e2-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="467e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="467e2-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="467e2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="467e2-105">DESCRIPTION</span></span>
<span data-ttu-id="467e2-106">Polecenie **cmdlet Set-AzPrivateEndpoint** aktualizuje prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="467e2-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="467e2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="467e2-107">EXAMPLES</span></span>

### <span data-ttu-id="467e2-108">1. Tworzy prywatny punkt końcowy i zamienia jedną z jego podsieci na inną</span><span class="sxs-lookup"><span data-stu-id="467e2-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="467e2-109">W tym przykładzie jest tworzyny prywatny punkt końcowy z jedną podsiecią, a następnie zamieniany na inną podsieci z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="467e2-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="467e2-110">To Set-PrivateEndpoint cmdlet służy do pisania zmodyfikowanego stanu prywatnego punktu końcowego po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="467e2-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="467e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="467e2-111">PARAMETERS</span></span>

### <span data-ttu-id="467e2-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="467e2-112">-AsJob</span></span>
<span data-ttu-id="467e2-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="467e2-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467e2-114">-DefaultProfile</span></span>
<span data-ttu-id="467e2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="467e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467e2-116">- PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="467e2-116">-PrivateEndpoint</span></span>
<span data-ttu-id="467e2-117">Określa prywatny obiekt punktu końcowego reprezentujący stan, dla którego powinien zostać ustawiony prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="467e2-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="467e2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467e2-118">CommonParameters</span></span>
<span data-ttu-id="467e2-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467e2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467e2-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="467e2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467e2-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="467e2-121">INPUTS</span></span>

### <span data-ttu-id="467e2-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="467e2-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="467e2-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="467e2-123">OUTPUTS</span></span>

### <span data-ttu-id="467e2-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="467e2-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="467e2-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="467e2-125">NOTES</span></span>

## <span data-ttu-id="467e2-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="467e2-126">RELATED LINKS</span></span>

[<span data-ttu-id="467e2-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="467e2-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="467e2-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="467e2-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="467e2-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="467e2-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


