---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193707"
---
# <span data-ttu-id="57418-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="57418-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="57418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57418-102">SYNOPSIS</span></span>
<span data-ttu-id="57418-103">Lista tras poznanych przez bramę sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57418-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="57418-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57418-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57418-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="57418-105">DESCRIPTION</span></span>
<span data-ttu-id="57418-106">Wylicza trasy poznane przez bramę sieci wirtualnej platformy Azure z różnych źródeł.</span><span class="sxs-lookup"><span data-stu-id="57418-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="57418-107">Obejmuje to trasy poznane za pośrednictwem BGP, a także trasy statyczne.</span><span class="sxs-lookup"><span data-stu-id="57418-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="57418-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57418-108">EXAMPLES</span></span>

### <span data-ttu-id="57418-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57418-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="57418-110">Dla bramy sieci wirtualnej platformy Azure o nazwie nazwana nazwa bramy w grupie zasobów grupy zasobów pobiera trasy, które wie brama platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57418-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="57418-111">Brama sieci wirtualnej Azure w tym przypadku ma dwie trasy statyczne (10.1.0.0/16 i 10.0.0.254/32) oraz jedną trasę poznaną za pośrednictwem BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="57418-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="57418-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57418-112">PARAMETERS</span></span>

### <span data-ttu-id="57418-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="57418-113">-AsJob</span></span>
<span data-ttu-id="57418-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="57418-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57418-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57418-115">-DefaultProfile</span></span>
<span data-ttu-id="57418-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57418-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57418-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57418-117">-ResourceGroupName</span></span>
<span data-ttu-id="57418-118">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57418-118">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57418-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="57418-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="57418-120">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57418-120">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57418-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57418-121">CommonParameters</span></span>
<span data-ttu-id="57418-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57418-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57418-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57418-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57418-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57418-124">INPUTS</span></span>

### <span data-ttu-id="57418-125">System.String</span><span class="sxs-lookup"><span data-stu-id="57418-125">System.String</span></span>

## <span data-ttu-id="57418-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57418-126">OUTPUTS</span></span>

### <span data-ttu-id="57418-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="57418-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="57418-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57418-128">NOTES</span></span>

## <span data-ttu-id="57418-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57418-129">RELATED LINKS</span></span>
