---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: e0a2722a59a9ffe1b6a7c3fb401b4faca85a1650
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951450"
---
# <span data-ttu-id="9ca4d-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="9ca4d-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="9ca4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca4d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca4d-103">Aktualizuje regułę NAT skojarzoną z usługą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="9ca4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9ca4d-104">SYNTAX</span></span>

### <span data-ttu-id="9ca4d-105">ByVpnGatewayNatRuleName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="9ca4d-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca4d-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca4d-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca4d-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="9ca4d-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca4d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9ca4d-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca4d-109">Polecenie **cmdlet Update-AzVpnGatewayNatRule** aktualizuje regułę NAT skojarzoną z aplikacją VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="9ca4d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9ca4d-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca4d-111">Przykład</span><span class="sxs-lookup"><span data-stu-id="9ca4d-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
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

<span data-ttu-id="9ca4d-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="9ca4d-113">Następnie utworzymy bramę VpnGateway w ramach tego centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="9ca4d-114">Następnie utwórz nową regułę NAT skojarzoną z utworzoną usługą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="9ca4d-115">Za pomocą tego polecenia: Update-AzVpnGatewayNatRule, zaktualizuj regułę NAT.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="9ca4d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ca4d-116">PARAMETERS</span></span>

### <span data-ttu-id="9ca4d-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9ca4d-117">-AsJob</span></span>
<span data-ttu-id="9ca4d-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9ca4d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ca4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca4d-119">-DefaultProfile</span></span>
<span data-ttu-id="9ca4d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca4d-121">- Mapowanie zewnętrzne</span><span class="sxs-lookup"><span data-stu-id="9ca4d-121">-ExternalMapping</span></span>
<span data-ttu-id="9ca4d-122">Lista mapowania zewnętrznych podsieci prywatnych adresów IP dla nat</span><span class="sxs-lookup"><span data-stu-id="9ca4d-122">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca4d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca4d-123">-InputObject</span></span>
<span data-ttu-id="9ca4d-124">Obiekt VpnGatewayNatRule do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-124">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca4d-125">- Mapowanie wewnętrzne</span><span class="sxs-lookup"><span data-stu-id="9ca4d-125">-InternalMapping</span></span>
<span data-ttu-id="9ca4d-126">Lista wewnętrznych mapowań wewnętrznych prywatnych adresów IP dla nat</span><span class="sxs-lookup"><span data-stu-id="9ca4d-126">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca4d-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9ca4d-127">-IpConfigurationId</span></span>
<span data-ttu-id="9ca4d-128">Identyfikator konfiguracji protokołu IP, do których ma zastosowanie ta reguła nat</span><span class="sxs-lookup"><span data-stu-id="9ca4d-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="9ca4d-129">— tryb</span><span class="sxs-lookup"><span data-stu-id="9ca4d-129">-Mode</span></span>
<span data-ttu-id="9ca4d-130">Kierunek źródłowego nat sieci VPN</span><span class="sxs-lookup"><span data-stu-id="9ca4d-130">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="9ca4d-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9ca4d-131">-Name</span></span>
<span data-ttu-id="9ca4d-132">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca4d-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9ca4d-133">-ParentResourceName</span></span>
<span data-ttu-id="9ca4d-134">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-134">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca4d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca4d-135">-ResourceGroupName</span></span>
<span data-ttu-id="9ca4d-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca4d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca4d-137">-ResourceId</span></span>
<span data-ttu-id="9ca4d-138">Identyfikator zasobu obiektu VpnGatewayNatRule do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca4d-139">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="9ca4d-139">-Type</span></span>
<span data-ttu-id="9ca4d-140">Typ reguły NAT dla sieci VPN NAT</span><span class="sxs-lookup"><span data-stu-id="9ca4d-140">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="9ca4d-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ca4d-141">-Confirm</span></span>
<span data-ttu-id="9ca4d-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca4d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca4d-143">-WhatIf</span></span>
<span data-ttu-id="9ca4d-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ca4d-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca4d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca4d-146">CommonParameters</span></span>
<span data-ttu-id="9ca4d-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca4d-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ca4d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca4d-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ca4d-149">INPUTS</span></span>

### <span data-ttu-id="9ca4d-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9ca4d-150">System.String</span></span>

### <span data-ttu-id="9ca4d-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="9ca4d-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="9ca4d-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ca4d-152">OUTPUTS</span></span>

### <span data-ttu-id="9ca4d-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="9ca4d-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="9ca4d-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9ca4d-154">NOTES</span></span>

## <span data-ttu-id="9ca4d-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ca4d-155">RELATED LINKS</span></span>
