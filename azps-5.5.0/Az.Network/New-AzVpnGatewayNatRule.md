---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: 45ec34bf437c64b96c3c46afa142d5e5b12f6010
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193538"
---
# <span data-ttu-id="c2215-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c2215-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="c2215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2215-102">SYNOPSIS</span></span>
<span data-ttu-id="c2215-103">Tworzy regułę NAT w sieci VpnGateway, którą można skojarzyć z usługą VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="c2215-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="c2215-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2215-104">SYNTAX</span></span>

### <span data-ttu-id="c2215-105">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c2215-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2215-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c2215-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2215-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c2215-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2215-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2215-108">DESCRIPTION</span></span>
<span data-ttu-id="c2215-109">Tworzy regułę NAT w sieci VpnGateway, którą można skojarzyć z siecią VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c2215-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="c2215-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2215-110">EXAMPLES</span></span>

### <span data-ttu-id="c2215-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2215-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule
```

<span data-ttu-id="c2215-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="c2215-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="c2215-113">Następnie utworzymy bramę VpnGateway w ramach tego centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="c2215-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="c2215-114">Następnie przy użyciu tego polecenia: New-AzVpnGatewayNatRule można utworzyć regułę NAT i skojarzyć ją z utworzoną aplikacją VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c2215-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="c2215-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2215-115">PARAMETERS</span></span>

### <span data-ttu-id="c2215-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c2215-116">-AsJob</span></span>
<span data-ttu-id="c2215-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c2215-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2215-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2215-118">-DefaultProfile</span></span>
<span data-ttu-id="c2215-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2215-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2215-120">- Mapowanie zewnętrzne</span><span class="sxs-lookup"><span data-stu-id="c2215-120">-ExternalMapping</span></span>
<span data-ttu-id="c2215-121">Lista mapowania zewnętrznych podsieci prywatnych adresów IP dla nat</span><span class="sxs-lookup"><span data-stu-id="c2215-121">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-122">- Mapowanie wewnętrzne</span><span class="sxs-lookup"><span data-stu-id="c2215-122">-InternalMapping</span></span>
<span data-ttu-id="c2215-123">Lista wewnętrznych mapowań wewnętrznych prywatnych adresów IP dla nat</span><span class="sxs-lookup"><span data-stu-id="c2215-123">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c2215-124">-IpConfigurationId</span></span>
<span data-ttu-id="c2215-125">Identyfikator konfiguracji protokołu IP, do których ma zastosowanie ta reguła nat</span><span class="sxs-lookup"><span data-stu-id="c2215-125">The IP Configuration ID this NAT rule applies to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-126">— tryb</span><span class="sxs-lookup"><span data-stu-id="c2215-126">-Mode</span></span>
<span data-ttu-id="c2215-127">Kierunek źródłowego nat sieci VPN</span><span class="sxs-lookup"><span data-stu-id="c2215-127">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2215-128">-Name</span></span>
<span data-ttu-id="c2215-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c2215-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-130">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2215-130">-ParentObject</span></span>
<span data-ttu-id="c2215-131">Nadrzędna aplikacja VpnGateway dla tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="c2215-131">The parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c2215-132">-ParentResourceId</span></span>
<span data-ttu-id="c2215-133">Identyfikator zasobu nadrzędnej aplikacji VpnGateway dla tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="c2215-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c2215-134">-ParentResourceName</span></span>
<span data-ttu-id="c2215-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2215-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2215-136">-ResourceGroupName</span></span>
<span data-ttu-id="c2215-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2215-137">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-138">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="c2215-138">-Type</span></span>
<span data-ttu-id="c2215-139">Typ reguły NAT dla sieci VPN NAT</span><span class="sxs-lookup"><span data-stu-id="c2215-139">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2215-140">-Confirm</span></span>
<span data-ttu-id="c2215-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2215-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2215-142">-WhatIf</span></span>
<span data-ttu-id="c2215-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2215-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2215-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2215-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2215-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2215-145">CommonParameters</span></span>
<span data-ttu-id="c2215-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2215-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2215-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2215-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2215-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2215-148">INPUTS</span></span>

### <span data-ttu-id="c2215-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c2215-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="c2215-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c2215-150">System.String</span></span>

## <span data-ttu-id="c2215-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2215-151">OUTPUTS</span></span>

### <span data-ttu-id="c2215-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c2215-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="c2215-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2215-153">NOTES</span></span>

## <span data-ttu-id="c2215-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2215-154">RELATED LINKS</span></span>
