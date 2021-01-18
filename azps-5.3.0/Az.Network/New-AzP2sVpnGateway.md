---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 516cd38257a8742f1bc23b3207b7e3c982d9eb36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501243"
---
# <span data-ttu-id="4687e-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4687e-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="4687e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4687e-102">SYNOPSIS</span></span>
<span data-ttu-id="4687e-103">Utwórz nową P2SVpnGateway w obszarze VirtualHub, aby wskazać łączność witryny.</span><span class="sxs-lookup"><span data-stu-id="4687e-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="4687e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4687e-104">SYNTAX</span></span>

### <span data-ttu-id="4687e-105">ByVirtualHubNameByVpnServerConfigurationObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4687e-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4687e-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="4687e-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4687e-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4687e-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4687e-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="4687e-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4687e-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4687e-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4687e-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="4687e-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4687e-111">Opis</span><span class="sxs-lookup"><span data-stu-id="4687e-111">DESCRIPTION</span></span>
<span data-ttu-id="4687e-112">Polecenie cmdlet **New-AzP2sVpnGateway** umożliwia utworzenie nowego P2SVpnGateway w obszarze VirtualHub na potrzeby punktu połączenia z witryną od klientów do usługi Azure VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4687e-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="4687e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4687e-113">EXAMPLES</span></span>

### <span data-ttu-id="4687e-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4687e-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="4687e-115">Polecenie cmdlet **New-AzP2sVpnGateway** umożliwia utworzenie nowego P2SVpnGateway w obszarze VirtualHub na potrzeby punktu połączenia z witryną.</span><span class="sxs-lookup"><span data-stu-id="4687e-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="4687e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4687e-116">PARAMETERS</span></span>

### <span data-ttu-id="4687e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4687e-117">-AsJob</span></span>
<span data-ttu-id="4687e-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4687e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4687e-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="4687e-119">-CustomDnsServer</span></span>
<span data-ttu-id="4687e-120">Lista niestandardowych serwerów DNS.</span><span class="sxs-lookup"><span data-stu-id="4687e-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4687e-121">-DefaultProfile</span></span>
<span data-ttu-id="4687e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4687e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4687e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4687e-123">-Name</span></span>
<span data-ttu-id="4687e-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4687e-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4687e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4687e-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4687e-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="4687e-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="4687e-128">Włącz flagę zabezpieczeń internetowych dla tych połączeń P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4687e-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="4687e-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4687e-129">-RoutingConfiguration</span></span>
<span data-ttu-id="4687e-130">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="4687e-130">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4687e-131">-Tag</span></span>
<span data-ttu-id="4687e-132">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="4687e-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="4687e-133">-VirtualHub</span></span>
<span data-ttu-id="4687e-134">VirtualHub, do tego P2SVpnGateway należy skojarzyć.</span><span class="sxs-lookup"><span data-stu-id="4687e-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="4687e-135">-VirtualHubId</span></span>
<span data-ttu-id="4687e-136">Identyfikator VirtualHub, do którego należy ten P2SVpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="4687e-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="4687e-137">-VirtualHubName</span></span>
<span data-ttu-id="4687e-138">Identyfikator VirtualHub, do którego należy ten P2SVpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="4687e-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="4687e-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="4687e-140">P2S VpnClient AddressPool dla tego P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4687e-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="4687e-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4687e-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="4687e-142">Jednostka skali dla tego P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4687e-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4687e-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="4687e-144">VpnServerConfiguration, który ma być dołączany do tego P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4687e-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4687e-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="4687e-146">Identyfikator obiektu konfiguracji serwera sieci VPN, do którego jest dołączona ta P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4687e-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4687e-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4687e-147">-Confirm</span></span>
<span data-ttu-id="4687e-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4687e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4687e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4687e-149">-WhatIf</span></span>
<span data-ttu-id="4687e-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4687e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4687e-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4687e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4687e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4687e-152">CommonParameters</span></span>
<span data-ttu-id="4687e-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4687e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4687e-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4687e-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4687e-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4687e-155">INPUTS</span></span>

### <span data-ttu-id="4687e-156">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4687e-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="4687e-157">System. String Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4687e-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="4687e-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4687e-158">OUTPUTS</span></span>

### <span data-ttu-id="4687e-159">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4687e-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="4687e-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4687e-160">NOTES</span></span>

## <span data-ttu-id="4687e-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4687e-161">RELATED LINKS</span></span>

[<span data-ttu-id="4687e-162">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4687e-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
