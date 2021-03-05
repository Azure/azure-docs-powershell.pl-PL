---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 578835b000b6efecb3a1429b884ad2416f6c289d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984337"
---
# <span data-ttu-id="1a109-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1a109-101">New-AzVpnSite</span></span>

## <span data-ttu-id="1a109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a109-102">SYNOPSIS</span></span>
<span data-ttu-id="1a109-103">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="1a109-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="1a109-104">Jest to reprezentacja RM gałęzi klienta, które są przekazywane na platformę Azure dla S2S za pomocą centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="1a109-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="1a109-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a109-105">SYNTAX</span></span>

### <span data-ttu-id="1a109-106">ByVirtualWanNameByVpnSiteIpAddress (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="1a109-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a109-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="1a109-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a109-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="1a109-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a109-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="1a109-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a109-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="1a109-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a109-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="1a109-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a109-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a109-112">DESCRIPTION</span></span>
<span data-ttu-id="1a109-113">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="1a109-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="1a109-114">Jest to reprezentacja RM gałęzi klienta, które są przekazywane na platformę Azure dla S2S za pomocą centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="1a109-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="1a109-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a109-115">EXAMPLES</span></span>

### <span data-ttu-id="1a109-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a109-116">Example 1</span></span>

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

<span data-ttu-id="1a109-117">Powyższe spowoduje utworzenie grupy zasobów — wirtualnej sieci WAN we wschodnich usa w grupie zasobów "nonlinkSite" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1a109-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="1a109-118">Następnie tworzy witrynę VpnSite reprezentującą gałąź klienta i łączy ją z wirtualną siecią WAN.</span><span class="sxs-lookup"><span data-stu-id="1a109-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="1a109-119">Połączenie IPSec można następnie skonfigurować przy użyciu tej gałęzi i aplikacji VpnGateway za pomocą New-AzVpnConnection sieci.</span><span class="sxs-lookup"><span data-stu-id="1a109-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="1a109-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1a109-120">Example 2</span></span>
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

<span data-ttu-id="1a109-121">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN i witryny VpnSite z 1 siecią VpnSiteLinks we wschódch Stanów Zjednoczonych w grupie zasobów "multilink" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1a109-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="1a109-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1a109-122">Example 3</span></span>

<span data-ttu-id="1a109-123">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="1a109-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="1a109-124">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="1a109-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="1a109-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a109-125">PARAMETERS</span></span>

### <span data-ttu-id="1a109-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="1a109-126">-AddressSpace</span></span>
<span data-ttu-id="1a109-127">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1a109-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="1a109-128">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1a109-128">-AsJob</span></span>
<span data-ttu-id="1a109-129">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1a109-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a109-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="1a109-130">-BgpAsn</span></span>
<span data-ttu-id="1a109-131">Asn BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="1a109-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="1a109-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="1a109-133">Adres komunikacji równorzędnej BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="1a109-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="1a109-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="1a109-135">Waga komunikacji równorzędnej BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="1a109-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a109-136">-DefaultProfile</span></span>
<span data-ttu-id="1a109-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a109-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a109-138">— DeviceModel</span><span class="sxs-lookup"><span data-stu-id="1a109-138">-DeviceModel</span></span>
<span data-ttu-id="1a109-139">Model urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="1a109-140">- DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="1a109-140">-DeviceVendor</span></span>
<span data-ttu-id="1a109-141">Dostawca urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="1a109-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="1a109-142">-IpAddress</span></span>
<span data-ttu-id="1a109-143">Adres IPAddress tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="1a109-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="1a109-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="1a109-145">Model urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="1a109-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1a109-146">-Location</span></span>
<span data-ttu-id="1a109-147">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1a109-147">The resource location.</span></span>

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

### <span data-ttu-id="1a109-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1a109-148">-Name</span></span>
<span data-ttu-id="1a109-149">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1a109-149">The resource name.</span></span>

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

### <span data-ttu-id="1a109-150">—O365Policy</span><span class="sxs-lookup"><span data-stu-id="1a109-150">-O365Policy</span></span>
<span data-ttu-id="1a109-151">Zasady dotyczące przerw w ruchu usługi Office 365 dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="1a109-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a109-152">-ResourceGroupName</span></span>
<span data-ttu-id="1a109-153">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1a109-153">The resource name.</span></span>

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

### <span data-ttu-id="1a109-154">— Tag</span><span class="sxs-lookup"><span data-stu-id="1a109-154">-Tag</span></span>
<span data-ttu-id="1a109-155">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a109-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1a109-156">— VirtualWan</span><span class="sxs-lookup"><span data-stu-id="1a109-156">-VirtualWan</span></span>
<span data-ttu-id="1a109-157">Należy połączyć użytkownika VirtualWan z tą lokacją vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="1a109-158">— VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="1a109-158">-VirtualWanId</span></span>
<span data-ttu-id="1a109-159">Z wirtualnym urządzeniem ResourceId VirtualWan musi być połączona ta lokacja vpn.</span><span class="sxs-lookup"><span data-stu-id="1a109-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="1a109-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="1a109-160">-VirtualWanName</span></span>
<span data-ttu-id="1a109-161">Nazwa użytkownika VirtualWan, z który jest połączona ta vpnsite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="1a109-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="1a109-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a109-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="1a109-163">Nazwa grupy zasobów dla użytkownika VirtualWan, z który jest połączona ta lokacja vpn, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="1a109-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="1a109-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="1a109-164">-VpnSiteLink</span></span>
<span data-ttu-id="1a109-165">Lista vpnsitelinków, które ta vpnsite ma.</span><span class="sxs-lookup"><span data-stu-id="1a109-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="1a109-166">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a109-166">-Confirm</span></span>
<span data-ttu-id="1a109-167">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1a109-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a109-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a109-168">-WhatIf</span></span>
<span data-ttu-id="1a109-169">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a109-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a109-170">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1a109-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a109-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a109-171">CommonParameters</span></span>
<span data-ttu-id="1a109-172">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a109-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a109-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a109-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a109-174">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a109-174">INPUTS</span></span>

### <span data-ttu-id="1a109-175">Brak</span><span class="sxs-lookup"><span data-stu-id="1a109-175">None</span></span>

## <span data-ttu-id="1a109-176">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a109-176">OUTPUTS</span></span>

### <span data-ttu-id="1a109-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="1a109-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="1a109-178">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a109-178">NOTES</span></span>

## <span data-ttu-id="1a109-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a109-179">RELATED LINKS</span></span>

[<span data-ttu-id="1a109-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1a109-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="1a109-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1a109-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="1a109-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1a109-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
