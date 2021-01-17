---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378926"
---
# <span data-ttu-id="82f76-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="82f76-101">New-AzVpnSite</span></span>

## <span data-ttu-id="82f76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82f76-102">SYNOPSIS</span></span>
<span data-ttu-id="82f76-103">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="82f76-104">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="82f76-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="82f76-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82f76-105">SYNTAX</span></span>

### <span data-ttu-id="82f76-106">ByVirtualWanNameByVpnSiteIpAddress (domyślny)</span><span class="sxs-lookup"><span data-stu-id="82f76-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f76-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="82f76-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f76-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="82f76-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82f76-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="82f76-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82f76-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="82f76-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82f76-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="82f76-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82f76-112">Opis</span><span class="sxs-lookup"><span data-stu-id="82f76-112">DESCRIPTION</span></span>
<span data-ttu-id="82f76-113">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="82f76-114">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="82f76-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="82f76-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82f76-115">EXAMPLES</span></span>

### <span data-ttu-id="82f76-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="82f76-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="82f76-117">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w Stanach Zjednoczonych na wschodnim Wschodzie w grupie zasobów "nonlinkSite" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="82f76-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="82f76-118">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="82f76-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="82f76-119">Połączenie IPSec może być następnie skonfigurowane z tą gałęzią i VpnGateway przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="82f76-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="82f76-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="82f76-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="82f76-121">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN i VpnSite z 1 VpnSiteLinks w Stanach Zjednoczonych na wschodnim Wschodzie w grupie zasobów "łącze wielokrotne" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="82f76-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="82f76-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="82f76-122">Example 3</span></span>

<span data-ttu-id="82f76-123">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="82f76-124">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="82f76-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="82f76-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82f76-125">PARAMETERS</span></span>

### <span data-ttu-id="82f76-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="82f76-126">-AddressSpace</span></span>
<span data-ttu-id="82f76-127">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="82f76-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="82f76-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82f76-128">-AsJob</span></span>
<span data-ttu-id="82f76-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="82f76-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82f76-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="82f76-130">-BgpAsn</span></span>
<span data-ttu-id="82f76-131">Protokół BGP ASN dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="82f76-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="82f76-133">Adres równorzędny BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="82f76-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="82f76-135">Waga komunikacji równorzędnej BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f76-136">-DefaultProfile</span></span>
<span data-ttu-id="82f76-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82f76-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82f76-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="82f76-138">-DeviceModel</span></span>
<span data-ttu-id="82f76-139">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="82f76-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="82f76-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="82f76-140">-DeviceVendor</span></span>
<span data-ttu-id="82f76-141">Dostawca urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="82f76-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="82f76-142">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="82f76-142">-IpAddress</span></span>
<span data-ttu-id="82f76-143">Adres IP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="82f76-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="82f76-145">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="82f76-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="82f76-146">-Location</span></span>
<span data-ttu-id="82f76-147">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="82f76-147">The resource location.</span></span>

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

### <span data-ttu-id="82f76-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82f76-148">-Name</span></span>
<span data-ttu-id="82f76-149">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="82f76-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="82f76-150">-O365Policy</span></span>
<span data-ttu-id="82f76-151">Zasady podgrupa ruchu pakietów Office 365 dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f76-152">-ResourceGroupName</span></span>
<span data-ttu-id="82f76-153">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="82f76-153">The resource name.</span></span>

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

### <span data-ttu-id="82f76-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="82f76-154">-Tag</span></span>
<span data-ttu-id="82f76-155">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="82f76-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="82f76-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="82f76-156">-VirtualWan</span></span>
<span data-ttu-id="82f76-157">VirtualWan ten VpnSite musi być podłączony.</span><span class="sxs-lookup"><span data-stu-id="82f76-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="82f76-158">-VirtualWanId</span></span>
<span data-ttu-id="82f76-159">Identyfikator zasobu ResourceId VirtualWan, do którego należy podłączyć ten VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="82f76-160">-VirtualWanName</span></span>
<span data-ttu-id="82f76-161">Nazwa VirtualWan, do której należy ten VpnSite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="82f76-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f76-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="82f76-163">Nazwa grupy zasobów VirtualWan, do której należy ten VpnSite należy połączyć.</span><span class="sxs-lookup"><span data-stu-id="82f76-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="82f76-164">-VpnSiteLink</span></span>
<span data-ttu-id="82f76-165">Lista VpnSiteLinks, które posiada ta VpnSite.</span><span class="sxs-lookup"><span data-stu-id="82f76-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f76-166">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="82f76-166">-Confirm</span></span>
<span data-ttu-id="82f76-167">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f76-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f76-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f76-168">-WhatIf</span></span>
<span data-ttu-id="82f76-169">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f76-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f76-170">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="82f76-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f76-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f76-171">CommonParameters</span></span>
<span data-ttu-id="82f76-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f76-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f76-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82f76-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f76-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82f76-174">INPUTS</span></span>

### <span data-ttu-id="82f76-175">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="82f76-175">None</span></span>

## <span data-ttu-id="82f76-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82f76-176">OUTPUTS</span></span>

### <span data-ttu-id="82f76-177">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="82f76-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="82f76-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82f76-178">NOTES</span></span>

## <span data-ttu-id="82f76-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82f76-179">RELATED LINKS</span></span>

[<span data-ttu-id="82f76-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="82f76-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="82f76-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="82f76-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="82f76-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="82f76-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
