---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 682f6bdb8eb0ce80d4b81dc12b9ed8d09de4713a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350809"
---
# <span data-ttu-id="43372-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="43372-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="43372-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43372-102">SYNOPSIS</span></span>
<span data-ttu-id="43372-103">Zaktualizuj istniejące P2SVpnGateway w obszarze VirtualHub, aby wskazać łączność witryny.</span><span class="sxs-lookup"><span data-stu-id="43372-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="43372-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43372-104">SYNTAX</span></span>

### <span data-ttu-id="43372-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43372-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43372-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="43372-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43372-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="43372-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43372-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="43372-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43372-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="43372-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>]
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43372-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="43372-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43372-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="43372-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43372-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="43372-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43372-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="43372-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43372-114">Opis</span><span class="sxs-lookup"><span data-stu-id="43372-114">DESCRIPTION</span></span>
<span data-ttu-id="43372-115">Polecenie cmdlet **Update-AzP2sVpnGateway** umożliwia zaktualizowanie istniejącego P2SVpnGateway w obszarze VirtualHub przy użyciu nowych VpnClientAddressPool lub nowych VpnServerConfiguration lub zmian VpnGatewayScaleUnit.</span><span class="sxs-lookup"><span data-stu-id="43372-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="43372-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43372-116">EXAMPLES</span></span>

### <span data-ttu-id="43372-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43372-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces -EnableInternetSecurityFlag                                

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
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
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="43372-118">Polecenie cmdlet **Update-AzP2sVpnGateway** umożliwia zaktualizowanie istniejącego P2SVpnGateway w obszarze VirtualHub przy użyciu nowego VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="43372-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="43372-119">Gdy wskażesz połączenie klienta witryny z tym P2SVpnGateway, jednym z adresów IP z tego VpnClientAddressPool przydzielono temu klientowi.</span><span class="sxs-lookup"><span data-stu-id="43372-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

### <span data-ttu-id="43372-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="43372-120">Example 2</span></span>

<span data-ttu-id="43372-121">Zaktualizuj istniejące P2SVpnGateway w obszarze VirtualHub, aby wskazać łączność witryny.</span><span class="sxs-lookup"><span data-stu-id="43372-121">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span> <span data-ttu-id="43372-122">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="43372-122">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzP2sVpnGateway -AsJob -Name 00000000-0000-0000-0000-00000000000000000-westus-gw -ResourceGroupName P2SCortexGATesting -VpnClientAddressPool <String[]> -VpnGatewayScaleUnit 1 -VpnServerConfiguration <PSVpnServerConfiguration>
```

## <span data-ttu-id="43372-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43372-123">PARAMETERS</span></span>

### <span data-ttu-id="43372-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43372-124">-AsJob</span></span>
<span data-ttu-id="43372-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="43372-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43372-126">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="43372-126">-CustomDnsServer</span></span>
<span data-ttu-id="43372-127">Lista niestandardowych serwerów DNS.</span><span class="sxs-lookup"><span data-stu-id="43372-127">The list of Custom Dns Servers.</span></span>

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

### <span data-ttu-id="43372-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43372-128">-DefaultProfile</span></span>
<span data-ttu-id="43372-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43372-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43372-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43372-130">-InputObject</span></span>
<span data-ttu-id="43372-131">Obiekt bramy sieci VPN P2S, który ma zostać zmodyfikowany</span><span class="sxs-lookup"><span data-stu-id="43372-131">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43372-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43372-132">-Name</span></span>
<span data-ttu-id="43372-133">Nazwa bramy sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="43372-133">The P2S vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43372-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43372-134">-ResourceGroupName</span></span>
<span data-ttu-id="43372-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43372-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43372-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43372-136">-ResourceId</span></span>
<span data-ttu-id="43372-137">Identyfikator zasobu platformy Azure P2SVpnGateway, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="43372-137">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43372-138">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="43372-138">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="43372-139">Włącz flagę zabezpieczeń internetowych dla tych połączeń P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="43372-139">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="43372-140">-DisableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="43372-140">-DisableInternetSecurityFlag</span></span>
<span data-ttu-id="43372-141">Wyłącz flagę zabezpieczeń internetowych dla tego połączenia P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="43372-141">Disable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="43372-142">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="43372-142">-RoutingConfiguration</span></span>
<span data-ttu-id="43372-143">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="43372-143">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="43372-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="43372-144">-Tag</span></span>
<span data-ttu-id="43372-145">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="43372-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="43372-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="43372-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="43372-147">P2S VpnClient AddressPool dla tego P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="43372-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="43372-148">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="43372-148">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="43372-149">Jednostka skali dla tego P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="43372-149">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43372-150">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="43372-150">-VpnServerConfiguration</span></span>
<span data-ttu-id="43372-151">VpnServerConfiguration, który ma być dołączany do tego P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="43372-151">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43372-152">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="43372-152">-VpnServerConfigurationId</span></span>
<span data-ttu-id="43372-153">Identyfikator obiektu konfiguracji serwera sieci VPN, do którego jest dołączona ta P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="43372-153">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43372-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43372-154">-Confirm</span></span>
<span data-ttu-id="43372-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43372-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43372-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43372-156">-WhatIf</span></span>
<span data-ttu-id="43372-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43372-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43372-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43372-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43372-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43372-159">CommonParameters</span></span>
<span data-ttu-id="43372-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43372-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43372-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43372-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43372-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43372-162">INPUTS</span></span>

### <span data-ttu-id="43372-163">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="43372-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="43372-164">System. String Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="43372-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="43372-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43372-165">OUTPUTS</span></span>

### <span data-ttu-id="43372-166">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="43372-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="43372-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43372-167">NOTES</span></span>

## <span data-ttu-id="43372-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43372-168">RELATED LINKS</span></span>

[<span data-ttu-id="43372-169">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="43372-169">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
