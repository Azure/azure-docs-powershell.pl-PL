---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 401fa91682e68b74e950d5010b22ce140436b06a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184426"
---
# <span data-ttu-id="eb6f1-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb6f1-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="eb6f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6f1-103">Utwórz nową bramę P2SVpnGateway w obszarze VirtualHub, aby wskazać łączność z witryną.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="eb6f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eb6f1-104">SYNTAX</span></span>

### <span data-ttu-id="eb6f1-105">ByVirtualHubNameByVpnServerConfigurationObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="eb6f1-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb6f1-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="eb6f1-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb6f1-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="eb6f1-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb6f1-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="eb6f1-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb6f1-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="eb6f1-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb6f1-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="eb6f1-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb6f1-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="eb6f1-111">DESCRIPTION</span></span>
<span data-ttu-id="eb6f1-112">Polecenie cmdlet New-AzP2sVpnGateway umożliwia utworzenie nowej aplikacji P2SVpnGateway w obszarze VirtualHub for Point na łączność z witryną z klientów usługi Point do klientów witryny do usługi Azure VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-112">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="eb6f1-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eb6f1-113">EXAMPLES</span></span>

### <span data-ttu-id="eb6f1-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb6f1-114">Example 1</span></span>
```
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag -EnableRoutingPreferenceInternetFlag

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

<span data-ttu-id="eb6f1-115">Polecenie New-AzP2sVpnGateway cmdlet umożliwia utworzenie nowej aplikacji P2SVpnGateway w obszarze VirtualHub for Point to site connectivity.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-115">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="eb6f1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb6f1-116">PARAMETERS</span></span>

### <span data-ttu-id="eb6f1-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="eb6f1-117">-AsJob</span></span>
<span data-ttu-id="eb6f1-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="eb6f1-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="eb6f1-119">-CustomDnsServer</span></span>
<span data-ttu-id="eb6f1-120">Lista niestandardowych serwerów DNS.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6f1-121">-DefaultProfile</span></span>
<span data-ttu-id="eb6f1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb6f1-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eb6f1-123">-Name</span></span>
<span data-ttu-id="eb6f1-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb6f1-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="eb6f1-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="eb6f1-128">Włącz flagę zabezpieczeń internetowych dla połączeń P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb6f1-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb6f1-129">-RoutingConfiguration</span></span>
<span data-ttu-id="eb6f1-130">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="eb6f1-130">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="eb6f1-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="eb6f1-131">-Tag</span></span>
<span data-ttu-id="eb6f1-132">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-133">— VirtualHub</span><span class="sxs-lookup"><span data-stu-id="eb6f1-133">-VirtualHub</span></span>
<span data-ttu-id="eb6f1-134">Z tą aplikacją P2SVpnGateway musi być skojarzona usługa VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-135">- VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="eb6f1-135">-VirtualHubId</span></span>
<span data-ttu-id="eb6f1-136">Identyfikator aplikacji VirtualHub, z tą aplikacją P2SVpnGateway, musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-137">- VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="eb6f1-137">-VirtualHubName</span></span>
<span data-ttu-id="eb6f1-138">Identyfikator aplikacji VirtualHub, z tą aplikacją P2SVpnGateway, musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="eb6f1-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="eb6f1-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="eb6f1-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="eb6f1-142">Jednostka skali dla tego aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-143">- VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb6f1-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="eb6f1-144">Konfiguracja VpnServerConfiguration dołączona do tej aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="eb6f1-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="eb6f1-146">Identyfikator obiektu konfiguracji serwera Vpn, do którym zostanie dołączona aplikacja P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-147">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="eb6f1-147">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="eb6f1-148">Oflaguj, aby włączyć Internet preferencji routingu w tej aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-148">Flag to enable Routing Preference Internet on this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="eb6f1-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb6f1-149">-Confirm</span></span>
<span data-ttu-id="eb6f1-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb6f1-151">-WhatIf</span></span>
<span data-ttu-id="eb6f1-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb6f1-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6f1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6f1-154">CommonParameters</span></span>
<span data-ttu-id="eb6f1-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6f1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6f1-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb6f1-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6f1-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb6f1-157">INPUTS</span></span>

### <span data-ttu-id="eb6f1-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="eb6f1-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="eb6f1-159">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb6f1-159">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="eb6f1-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb6f1-160">OUTPUTS</span></span>

### <span data-ttu-id="eb6f1-161">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="eb6f1-161">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
## <span data-ttu-id="eb6f1-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eb6f1-162">NOTES</span></span>

## <span data-ttu-id="eb6f1-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb6f1-163">RELATED LINKS</span></span>

[<span data-ttu-id="eb6f1-164">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb6f1-164">New-AzRoutingConfiguration</span></span>]()

