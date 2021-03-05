---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 0f5cedd29b7dcc296494519fe40f8ea7e0edb445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964250"
---
# <span data-ttu-id="10cc6-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="10cc6-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="10cc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="10cc6-103">Uzyskiwanie skojarzeń zabezpieczeń IKE dla połączenia wirtualnej bramy sieciowej</span><span class="sxs-lookup"><span data-stu-id="10cc6-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="10cc6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10cc6-104">SYNTAX</span></span>

### <span data-ttu-id="10cc6-105">ByName</span><span class="sxs-lookup"><span data-stu-id="10cc6-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cc6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10cc6-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cc6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10cc6-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10cc6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="10cc6-108">DESCRIPTION</span></span>
<span data-ttu-id="10cc6-109">Polecenie **cmdlet Get-AzVirtualNetworkGatewayConnectionIkeSa** zwraca skojarzenia zabezpieczeń IKE połączenia na podstawie nazwy połączenia i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10cc6-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="10cc6-110">Jeśli polecenie **cmdlet Get-AzVirtualNetworkGatewayConnection** zostanie wydane bez określenia parametru -Name, dane wyjściowe nie będą zawierały skojarzeń zabezpieczeń IKE.</span><span class="sxs-lookup"><span data-stu-id="10cc6-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="10cc6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10cc6-111">EXAMPLES</span></span>

### <span data-ttu-id="10cc6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10cc6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="10cc6-113">Zwraca skojarzenia zabezpieczeń IKE dla połączenia bramy sieci wirtualnej z nazwą "myTunnel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="10cc6-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="10cc6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10cc6-114">PARAMETERS</span></span>

### <span data-ttu-id="10cc6-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="10cc6-115">-AsJob</span></span>
<span data-ttu-id="10cc6-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="10cc6-116">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cc6-117">-DefaultProfile</span></span>
<span data-ttu-id="10cc6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10cc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cc6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10cc6-119">-InputObject</span></span>
<span data-ttu-id="10cc6-120">Obiekt połączenia bramy sieci wirtualnej, dla którego należy uzyskać zdalnego dostępu do usług IKE.</span><span class="sxs-lookup"><span data-stu-id="10cc6-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cc6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10cc6-121">-Name</span></span>
<span data-ttu-id="10cc6-122">Nazwa połączenia bramy sieci wirtualnej, dla której należy uzyskać zdalnego dostępu do usług IKE.</span><span class="sxs-lookup"><span data-stu-id="10cc6-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10cc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="10cc6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10cc6-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10cc6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10cc6-125">-ResourceId</span></span>
<span data-ttu-id="10cc6-126">Identyfikator zasobu Azure połączenia wirtualnej bramy sieciowej, do którego należy uzyskać zdalnego dostępu.</span><span class="sxs-lookup"><span data-stu-id="10cc6-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cc6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cc6-127">CommonParameters</span></span>
<span data-ttu-id="10cc6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10cc6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cc6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10cc6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cc6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10cc6-130">INPUTS</span></span>

### <span data-ttu-id="10cc6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="10cc6-131">System.String</span></span>

## <span data-ttu-id="10cc6-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10cc6-132">OUTPUTS</span></span>

### <span data-ttu-id="10cc6-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="10cc6-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="10cc6-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10cc6-134">NOTES</span></span>

## <span data-ttu-id="10cc6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10cc6-135">RELATED LINKS</span></span>
