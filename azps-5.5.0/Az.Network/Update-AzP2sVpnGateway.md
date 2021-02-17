---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 682f6bdb8eb0ce80d4b81dc12b9ed8d09de4713a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193306"
---
# <span data-ttu-id="bd895-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd895-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="bd895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd895-102">SYNOPSIS</span></span>
<span data-ttu-id="bd895-103">Zaktualizuj istniejącą witrynę P2SVpnGateway w obszarze VirtualHub, aby uzyskać punkt łączności z witryną.</span><span class="sxs-lookup"><span data-stu-id="bd895-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="bd895-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bd895-104">SYNTAX</span></span>

### <span data-ttu-id="bd895-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bd895-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd895-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="bd895-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd895-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="bd895-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd895-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="bd895-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd895-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="bd895-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>]
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd895-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="bd895-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd895-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="bd895-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd895-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="bd895-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd895-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="bd895-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd895-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="bd895-114">DESCRIPTION</span></span>
<span data-ttu-id="bd895-115">Polecenie cmdlet **Update-AzP2sVpnGateway** umożliwia zaktualizowanie istniejącej aplikacji P2SVpnGateway w obszarze VirtualHub za pomocą nowego pliku VpnClientAddressPool lub nowej konfiguracji VpnServerConfiguration albo zmiany vpnGatewayScaleUnit.</span><span class="sxs-lookup"><span data-stu-id="bd895-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="bd895-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bd895-116">EXAMPLES</span></span>

### <span data-ttu-id="bd895-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd895-117">Example 1</span></span>
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

<span data-ttu-id="bd895-118">Polecenie cmdlet **Update-AzP2sVpnGateway** umożliwia zaktualizowanie istniejącej aplikacji P2SVpnGateway w obszarze VirtualHub za pomocą nowego pliku VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="bd895-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="bd895-119">Gdy klient wskaże witrynę łączy się z tą aplikacją P2SVpnGateway, do tego klienta jest przydzielany jeden z adresów IP z tego klienta VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="bd895-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

### <span data-ttu-id="bd895-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bd895-120">Example 2</span></span>

<span data-ttu-id="bd895-121">Zaktualizuj istniejącą witrynę P2SVpnGateway w obszarze VirtualHub, aby uzyskać punkt łączności z witryną.</span><span class="sxs-lookup"><span data-stu-id="bd895-121">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span> <span data-ttu-id="bd895-122">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="bd895-122">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzP2sVpnGateway -AsJob -Name 00000000-0000-0000-0000-00000000000000000-westus-gw -ResourceGroupName P2SCortexGATesting -VpnClientAddressPool <String[]> -VpnGatewayScaleUnit 1 -VpnServerConfiguration <PSVpnServerConfiguration>
```

## <span data-ttu-id="bd895-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd895-123">PARAMETERS</span></span>

### <span data-ttu-id="bd895-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bd895-124">-AsJob</span></span>
<span data-ttu-id="bd895-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bd895-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd895-126">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="bd895-126">-CustomDnsServer</span></span>
<span data-ttu-id="bd895-127">Lista niestandardowych serwerów DNS.</span><span class="sxs-lookup"><span data-stu-id="bd895-127">The list of Custom Dns Servers.</span></span>

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

### <span data-ttu-id="bd895-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd895-128">-DefaultProfile</span></span>
<span data-ttu-id="bd895-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd895-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd895-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd895-130">-InputObject</span></span>
<span data-ttu-id="bd895-131">Obiekt bramy sieci vpn p2s do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="bd895-131">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="bd895-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bd895-132">-Name</span></span>
<span data-ttu-id="bd895-133">Nazwa bramy sieci vpn P2S.</span><span class="sxs-lookup"><span data-stu-id="bd895-133">The P2S vpn gateway name.</span></span>

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

### <span data-ttu-id="bd895-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd895-134">-ResourceGroupName</span></span>
<span data-ttu-id="bd895-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd895-135">The resource group name.</span></span>

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

### <span data-ttu-id="bd895-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd895-136">-ResourceId</span></span>
<span data-ttu-id="bd895-137">Identyfikator zasobu Azure p2SVpnGateway do modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="bd895-137">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="bd895-138">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="bd895-138">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="bd895-139">Włącz flagę zabezpieczeń internetowych dla połączeń P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd895-139">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="bd895-140">-DisableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="bd895-140">-DisableInternetSecurityFlag</span></span>
<span data-ttu-id="bd895-141">Wyłącz flagę zabezpieczeń internetowych dla połączeń P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd895-141">Disable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="bd895-142">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd895-142">-RoutingConfiguration</span></span>
<span data-ttu-id="bd895-143">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="bd895-143">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="bd895-144">— Tag</span><span class="sxs-lookup"><span data-stu-id="bd895-144">-Tag</span></span>
<span data-ttu-id="bd895-145">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd895-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bd895-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="bd895-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="bd895-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bd895-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="bd895-148">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="bd895-148">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="bd895-149">Jednostka skali dla tego aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bd895-149">The scale unit for this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="bd895-150">- VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd895-150">-VpnServerConfiguration</span></span>
<span data-ttu-id="bd895-151">Konfiguracja VpnServerConfiguration dołączona do tej aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bd895-151">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="bd895-152">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bd895-152">-VpnServerConfigurationId</span></span>
<span data-ttu-id="bd895-153">Identyfikator obiektu konfiguracji serwera Vpn, do którym zostanie dołączona ta aplikacja P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bd895-153">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

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

### <span data-ttu-id="bd895-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd895-154">-Confirm</span></span>
<span data-ttu-id="bd895-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bd895-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd895-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd895-156">-WhatIf</span></span>
<span data-ttu-id="bd895-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd895-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd895-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bd895-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd895-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd895-159">CommonParameters</span></span>
<span data-ttu-id="bd895-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd895-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd895-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd895-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd895-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd895-162">INPUTS</span></span>

### <span data-ttu-id="bd895-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd895-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="bd895-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd895-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="bd895-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd895-165">OUTPUTS</span></span>

### <span data-ttu-id="bd895-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd895-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="bd895-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bd895-167">NOTES</span></span>

## <span data-ttu-id="bd895-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd895-168">RELATED LINKS</span></span>

[<span data-ttu-id="bd895-169">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd895-169">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
