---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504381"
---
# <span data-ttu-id="1ccb1-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ccb1-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="1ccb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ccb1-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccb1-103">Umożliwia zaktualizowanie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="1ccb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ccb1-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ccb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ccb1-105">DESCRIPTION</span></span>
<span data-ttu-id="1ccb1-106">Polecenie cmdlet **Set-AzPrivateEndpoint** umożliwia zaktualizowanie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="1ccb1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ccb1-107">EXAMPLES</span></span>

### <span data-ttu-id="1ccb1-108">1: Tworzenie prywatnego punktu końcowego i zamienianie jednej z jej podsieci na inną.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="1ccb1-109">W tym przykładzie przedstawiono tworzenie prywatnego punktu końcowego z jedną podsiecią, a następnie zastępowanie innej podsieci w reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="1ccb1-110">Polecenie cmdlet Set-PrivateEndpoint służy następnie do napisania zmodyfikowanego prywatnego stanu punktu końcowego po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="1ccb1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ccb1-111">PARAMETERS</span></span>

### <span data-ttu-id="1ccb1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ccb1-112">-AsJob</span></span>
<span data-ttu-id="1ccb1-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1ccb1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ccb1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccb1-114">-DefaultProfile</span></span>
<span data-ttu-id="1ccb1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ccb1-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ccb1-116">-PrivateEndpoint</span></span>
<span data-ttu-id="1ccb1-117">Określa prywatny obiekt punktu końcowego reprezentujący stan, do którego ma zostać ustawiony prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="1ccb1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccb1-118">CommonParameters</span></span>
<span data-ttu-id="1ccb1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccb1-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ccb1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccb1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ccb1-121">INPUTS</span></span>

### <span data-ttu-id="1ccb1-122">Microsoft. Azure. Commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ccb1-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="1ccb1-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ccb1-123">OUTPUTS</span></span>

### <span data-ttu-id="1ccb1-124">Microsoft. Azure. Commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ccb1-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="1ccb1-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ccb1-125">NOTES</span></span>

## <span data-ttu-id="1ccb1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ccb1-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ccb1-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ccb1-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="1ccb1-128">Nowe — AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ccb1-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="1ccb1-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ccb1-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


