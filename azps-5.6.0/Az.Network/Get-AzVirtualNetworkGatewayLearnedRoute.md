---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 8dbc1ad62d11ac6b14897c27b11ebdb7f6fb8cc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960458"
---
# <span data-ttu-id="1ff31-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="1ff31-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="1ff31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ff31-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff31-103">Lista tras poznanych przez bramę sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1ff31-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="1ff31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1ff31-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ff31-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1ff31-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff31-106">Wylicza trasy poznane przez bramę sieci wirtualnej platformy Azure z różnych źródeł.</span><span class="sxs-lookup"><span data-stu-id="1ff31-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="1ff31-107">Obejmuje to trasy poznane za pośrednictwem BGP, a także trasy statyczne.</span><span class="sxs-lookup"><span data-stu-id="1ff31-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="1ff31-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1ff31-108">EXAMPLES</span></span>

### <span data-ttu-id="1ff31-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ff31-109">Example 1</span></span>
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

<span data-ttu-id="1ff31-110">Dla bramy sieci wirtualnej platformy Azure o nazwie nazwana nazwa bramy w grupie zasobów grupy zasobów pobiera trasy, które zna brama azure.</span><span class="sxs-lookup"><span data-stu-id="1ff31-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="1ff31-111">Brama sieci wirtualnej Azure w tym przypadku ma dwie trasy statyczne (10.1.0.0/16 i 10.0.0.254/32) oraz jedną trasę poznaną za pośrednictwem BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="1ff31-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="1ff31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ff31-112">PARAMETERS</span></span>

### <span data-ttu-id="1ff31-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1ff31-113">-AsJob</span></span>
<span data-ttu-id="1ff31-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1ff31-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ff31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff31-115">-DefaultProfile</span></span>
<span data-ttu-id="1ff31-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff31-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ff31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff31-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ff31-118">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1ff31-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="1ff31-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1ff31-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1ff31-120">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1ff31-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="1ff31-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff31-121">CommonParameters</span></span>
<span data-ttu-id="1ff31-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff31-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff31-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ff31-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff31-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ff31-124">INPUTS</span></span>

### <span data-ttu-id="1ff31-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1ff31-125">System.String</span></span>

## <span data-ttu-id="1ff31-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ff31-126">OUTPUTS</span></span>

### <span data-ttu-id="1ff31-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="1ff31-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="1ff31-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1ff31-128">NOTES</span></span>

## <span data-ttu-id="1ff31-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ff31-129">RELATED LINKS</span></span>
