---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 6b0eb456c2134e6ed64d8e6c441db041776fcf39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179803"
---
# <span data-ttu-id="d6f51-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="d6f51-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="d6f51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f51-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f51-103">Uzyskiwanie skojarzeń zabezpieczeń IKE dla połączenia wirtualnej bramy sieciowej</span><span class="sxs-lookup"><span data-stu-id="d6f51-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="d6f51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6f51-104">SYNTAX</span></span>

### <span data-ttu-id="d6f51-105">ByName</span><span class="sxs-lookup"><span data-stu-id="d6f51-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6f51-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d6f51-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6f51-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f51-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6f51-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6f51-108">DESCRIPTION</span></span>
<span data-ttu-id="d6f51-109">Polecenie **cmdlet Get-AzVirtualNetworkGatewayConnectionIkeSa** zwraca skojarzenia zabezpieczeń IKE połączenia na podstawie nazwy połączenia i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6f51-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="d6f51-110">Jeśli polecenie **cmdlet Get-AzVirtualNetworkGatewayConnection** zostanie wydane bez określenia parametru -Name, dane wyjściowe nie będą zawierały skojarzeń zabezpieczeń IKE.</span><span class="sxs-lookup"><span data-stu-id="d6f51-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="d6f51-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6f51-111">EXAMPLES</span></span>

### <span data-ttu-id="d6f51-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6f51-112">Example 1</span></span>
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

<span data-ttu-id="d6f51-113">Zwraca skojarzenia zabezpieczeń IKE dla połączenia wirtualnej bramy sieciowej o nazwie "myTunnel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="d6f51-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="d6f51-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6f51-114">PARAMETERS</span></span>

### <span data-ttu-id="d6f51-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f51-115">-AsJob</span></span>
<span data-ttu-id="d6f51-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="d6f51-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d6f51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f51-117">-DefaultProfile</span></span>
<span data-ttu-id="d6f51-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f51-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f51-119">-InputObject</span></span>
<span data-ttu-id="d6f51-120">Obiekt połączenia bramy sieci wirtualnej, dla którego należy uzyskać zdalnego dostępu do usług IKE.</span><span class="sxs-lookup"><span data-stu-id="d6f51-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="d6f51-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6f51-121">-Name</span></span>
<span data-ttu-id="d6f51-122">Nazwa połączenia bramy sieci wirtualnej, dla której należy uzyskać zdalnego dostępu do usług IKE.</span><span class="sxs-lookup"><span data-stu-id="d6f51-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="d6f51-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f51-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6f51-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6f51-124">The resource group name.</span></span>

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

### <span data-ttu-id="d6f51-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f51-125">-ResourceId</span></span>
<span data-ttu-id="d6f51-126">Identyfikator zasobu Azure połączenia wirtualnej bramy sieciowej, do którego należy uzyskać zdalnego dostępu.</span><span class="sxs-lookup"><span data-stu-id="d6f51-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="d6f51-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f51-127">CommonParameters</span></span>
<span data-ttu-id="d6f51-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f51-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f51-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6f51-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f51-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f51-130">INPUTS</span></span>

### <span data-ttu-id="d6f51-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d6f51-131">System.String</span></span>

## <span data-ttu-id="d6f51-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f51-132">OUTPUTS</span></span>

### <span data-ttu-id="d6f51-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="d6f51-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="d6f51-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6f51-134">NOTES</span></span>

## <span data-ttu-id="d6f51-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6f51-135">RELATED LINKS</span></span>
