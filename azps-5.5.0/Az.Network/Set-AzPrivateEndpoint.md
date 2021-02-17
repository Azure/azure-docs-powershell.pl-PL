---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184178"
---
# <span data-ttu-id="46c35-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46c35-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="46c35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46c35-102">SYNOPSIS</span></span>
<span data-ttu-id="46c35-103">Aktualizuje prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="46c35-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="46c35-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46c35-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46c35-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="46c35-105">DESCRIPTION</span></span>
<span data-ttu-id="46c35-106">Polecenie **cmdlet Set-AzPrivateEndpoint** aktualizuje prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="46c35-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="46c35-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46c35-107">EXAMPLES</span></span>

### <span data-ttu-id="46c35-108">1. Tworzy prywatny punkt końcowy i zamienia jedną z jego podsieci na inną</span><span class="sxs-lookup"><span data-stu-id="46c35-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="46c35-109">W tym przykładzie jest tworzyny prywatny punkt końcowy z jedną podsiecią, a następnie zamieniany na inną podsieci z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="46c35-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="46c35-110">To Set-PrivateEndpoint cmdlet służy do zapisu zmodyfikowanego stanu prywatnego punktu końcowego po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="46c35-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="46c35-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46c35-111">PARAMETERS</span></span>

### <span data-ttu-id="46c35-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="46c35-112">-AsJob</span></span>
<span data-ttu-id="46c35-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="46c35-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46c35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c35-114">-DefaultProfile</span></span>
<span data-ttu-id="46c35-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46c35-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c35-116">- PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46c35-116">-PrivateEndpoint</span></span>
<span data-ttu-id="46c35-117">Określa prywatny obiekt punktu końcowego reprezentujący stan, dla którego powinien zostać ustawiony prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="46c35-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="46c35-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c35-118">CommonParameters</span></span>
<span data-ttu-id="46c35-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c35-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c35-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46c35-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c35-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46c35-121">INPUTS</span></span>

### <span data-ttu-id="46c35-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46c35-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="46c35-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46c35-123">OUTPUTS</span></span>

### <span data-ttu-id="46c35-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46c35-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="46c35-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46c35-125">NOTES</span></span>

## <span data-ttu-id="46c35-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46c35-126">RELATED LINKS</span></span>

[<span data-ttu-id="46c35-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46c35-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="46c35-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46c35-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="46c35-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46c35-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


