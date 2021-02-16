---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: 60f68795e79e751dda75ae4d549d2b25a43392e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186795"
---
# <span data-ttu-id="480de-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="480de-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="480de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="480de-102">SYNOPSIS</span></span>
<span data-ttu-id="480de-103">Aktualizuje regułę NAT skojarzoną z vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="480de-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="480de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="480de-104">SYNTAX</span></span>

### <span data-ttu-id="480de-105">ByVpnGatewayNatRuleName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="480de-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="480de-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="480de-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="480de-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="480de-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="480de-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="480de-108">DESCRIPTION</span></span>
<span data-ttu-id="480de-109">Polecenie **cmdlet Update-AzVpnGatewayNatRule** aktualizuje regułę NAT skojarzoną z aplikacją VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="480de-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="480de-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="480de-110">EXAMPLES</span></span>

### <span data-ttu-id="480de-111">Przykład</span><span class="sxs-lookup"><span data-stu-id="480de-111">Example</span></span>

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

<span data-ttu-id="480de-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="480de-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="480de-113">Następnie utworzymy bramę VpnGateway w ramach tego centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="480de-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="480de-114">Następnie utwórz nową regułę NAT skojarzoną z utworzoną usługą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="480de-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="480de-115">Za pomocą tego polecenia: Update-AzVpnGatewayNatRule, zaktualizuj regułę NAT.</span><span class="sxs-lookup"><span data-stu-id="480de-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="480de-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="480de-116">PARAMETERS</span></span>

### <span data-ttu-id="480de-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="480de-117">-AsJob</span></span>
<span data-ttu-id="480de-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="480de-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="480de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480de-119">-DefaultProfile</span></span>
<span data-ttu-id="480de-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="480de-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480de-121">- Mapowanie zewnętrzne</span><span class="sxs-lookup"><span data-stu-id="480de-121">-ExternalMapping</span></span>
<span data-ttu-id="480de-122">Lista mapowania zewnętrznych podsieci prywatnych adresów IP dla nat</span><span class="sxs-lookup"><span data-stu-id="480de-122">The list of private IP address subnet external mappings for NAT</span></span>

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

### <span data-ttu-id="480de-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="480de-123">-InputObject</span></span>
<span data-ttu-id="480de-124">Obiekt VpnGatewayNatRule do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="480de-124">The VpnGatewayNatRule object to update.</span></span>

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

### <span data-ttu-id="480de-125">- Mapowanie wewnętrzne</span><span class="sxs-lookup"><span data-stu-id="480de-125">-InternalMapping</span></span>
<span data-ttu-id="480de-126">Lista wewnętrznych mapowań wewnętrznych prywatnych adresów IP dla nat</span><span class="sxs-lookup"><span data-stu-id="480de-126">The list of private IP address subnet internal mappings for NAT</span></span>

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

### <span data-ttu-id="480de-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="480de-127">-IpConfigurationId</span></span>
<span data-ttu-id="480de-128">Identyfikator konfiguracji protokołu IP, do których ma zastosowanie ta reguła nat</span><span class="sxs-lookup"><span data-stu-id="480de-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="480de-129">— tryb</span><span class="sxs-lookup"><span data-stu-id="480de-129">-Mode</span></span>
<span data-ttu-id="480de-130">Kierunek źródłowego nat sieci VPN</span><span class="sxs-lookup"><span data-stu-id="480de-130">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="480de-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="480de-131">-Name</span></span>
<span data-ttu-id="480de-132">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="480de-132">The resource name.</span></span>

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

### <span data-ttu-id="480de-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="480de-133">-ParentResourceName</span></span>
<span data-ttu-id="480de-134">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="480de-134">The parent resource name.</span></span>

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

### <span data-ttu-id="480de-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480de-135">-ResourceGroupName</span></span>
<span data-ttu-id="480de-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="480de-136">The resource group name.</span></span>

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

### <span data-ttu-id="480de-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="480de-137">-ResourceId</span></span>
<span data-ttu-id="480de-138">Identyfikator zasobu obiektu VpnGatewayNatRule do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="480de-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

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

### <span data-ttu-id="480de-139">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="480de-139">-Type</span></span>
<span data-ttu-id="480de-140">Typ reguły NAT dla sieci VPN NAT</span><span class="sxs-lookup"><span data-stu-id="480de-140">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="480de-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="480de-141">-Confirm</span></span>
<span data-ttu-id="480de-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="480de-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="480de-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="480de-143">-WhatIf</span></span>
<span data-ttu-id="480de-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="480de-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="480de-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="480de-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="480de-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480de-146">CommonParameters</span></span>
<span data-ttu-id="480de-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480de-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480de-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="480de-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480de-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="480de-149">INPUTS</span></span>

### <span data-ttu-id="480de-150">System.String</span><span class="sxs-lookup"><span data-stu-id="480de-150">System.String</span></span>

### <span data-ttu-id="480de-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="480de-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="480de-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="480de-152">OUTPUTS</span></span>

### <span data-ttu-id="480de-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="480de-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="480de-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="480de-154">NOTES</span></span>

## <span data-ttu-id="480de-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="480de-155">RELATED LINKS</span></span>
