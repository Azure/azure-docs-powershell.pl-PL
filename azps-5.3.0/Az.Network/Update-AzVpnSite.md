---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503113"
---
# <span data-ttu-id="6b8b3-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b8b3-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="6b8b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8b3-103">Umożliwia zaktualizowanie witryny sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-103">Updates a VPN site.</span></span>

## <span data-ttu-id="6b8b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b8b3-104">SYNTAX</span></span>

### <span data-ttu-id="6b8b3-105">ByVpnSiteNameNoVirtualWanUpdate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b8b3-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="6b8b3-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="6b8b3-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6b8b3-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="6b8b3-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="6b8b3-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6b8b3-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="6b8b3-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="6b8b3-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="6b8b3-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6b8b3-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b8b3-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="6b8b3-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b8b3-117">Opis</span><span class="sxs-lookup"><span data-stu-id="6b8b3-117">DESCRIPTION</span></span>
<span data-ttu-id="6b8b3-118">Polecenie cmdlet **Update-AzVpnSite** aktualizuje witrynę sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="6b8b3-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b8b3-119">EXAMPLES</span></span>

### <span data-ttu-id="6b8b3-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b8b3-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="6b8b3-121">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="6b8b3-122">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="6b8b3-123">Po utworzeniu witryny wiadomość zostanie zaktualizowana w adresie IP witryny przy użyciu polecenia Set-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="6b8b3-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b8b3-124">PARAMETERS</span></span>

### <span data-ttu-id="6b8b3-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="6b8b3-125">-AddressSpace</span></span>
<span data-ttu-id="6b8b3-126">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="6b8b3-127">Użyj tego lub AddressSpaceObject, ale nie obu.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="6b8b3-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b8b3-128">-AsJob</span></span>
<span data-ttu-id="6b8b3-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6b8b3-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b8b3-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="6b8b3-130">-BgpAsn</span></span>
<span data-ttu-id="6b8b3-131">Protokół BGP ASN dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="6b8b3-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="6b8b3-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="6b8b3-133">Adres równorzędny BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="6b8b3-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="6b8b3-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="6b8b3-135">Waga komunikacji równorzędnej BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="6b8b3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8b3-136">-DefaultProfile</span></span>
<span data-ttu-id="6b8b3-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b8b3-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="6b8b3-138">-DeviceModel</span></span>
<span data-ttu-id="6b8b3-139">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="6b8b3-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="6b8b3-140">-DeviceVendor</span></span>
<span data-ttu-id="6b8b3-141">Dostawca urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="6b8b3-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b8b3-142">-InputObject</span></span>
<span data-ttu-id="6b8b3-143">Obiekt witryny sieci VPN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="6b8b3-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-144">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="6b8b3-144">-IpAddress</span></span>
<span data-ttu-id="6b8b3-145">Adres IP bramy sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="6b8b3-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="6b8b3-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="6b8b3-147">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="6b8b3-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b8b3-148">-Name</span></span>
<span data-ttu-id="6b8b3-149">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="6b8b3-150">-O365Policy</span></span>
<span data-ttu-id="6b8b3-151">Zasady podgrupa ruchu pakietów Office 365 dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="6b8b3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8b3-152">-ResourceGroupName</span></span>
<span data-ttu-id="6b8b3-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-153">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b8b3-154">-ResourceId</span></span>
<span data-ttu-id="6b8b3-155">Identyfikator zasobu platformy Azure dla witryny sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-155">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b8b3-156">-Tag</span></span>
<span data-ttu-id="6b8b3-157">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6b8b3-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="6b8b3-158">-VirtualWan</span></span>
<span data-ttu-id="6b8b3-159">VirtualWan ten VpnSite musi być podłączony.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="6b8b3-160">-VirtualWanId</span></span>
<span data-ttu-id="6b8b3-161">Identyfikator zasobu ResourceId VirtualWan, do którego należy podłączyć ten VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="6b8b3-162">-VirtualWanName</span></span>
<span data-ttu-id="6b8b3-163">Nazwa VirtualWan, do której należy ten VpnSite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8b3-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="6b8b3-165">Nazwa grupy zasobów VirtualWan, do której należy ten VpnSite należy połączyć.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="6b8b3-166">-VpnSiteLink</span></span>
<span data-ttu-id="6b8b3-167">Lista VpnSiteLinks, które posiada ta VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b3-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b8b3-168">-Confirm</span></span>
<span data-ttu-id="6b8b3-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b8b3-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b8b3-170">-WhatIf</span></span>
<span data-ttu-id="6b8b3-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b8b3-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b8b3-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8b3-173">CommonParameters</span></span>
<span data-ttu-id="6b8b3-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8b3-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8b3-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b8b3-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8b3-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b8b3-176">INPUTS</span></span>

### <span data-ttu-id="6b8b3-177">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b8b3-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="6b8b3-178">System. String</span><span class="sxs-lookup"><span data-stu-id="6b8b3-178">System.String</span></span>

## <span data-ttu-id="6b8b3-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b8b3-179">OUTPUTS</span></span>

### <span data-ttu-id="6b8b3-180">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b8b3-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="6b8b3-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b8b3-181">NOTES</span></span>

## <span data-ttu-id="6b8b3-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b8b3-182">RELATED LINKS</span></span>

[<span data-ttu-id="6b8b3-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b8b3-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="6b8b3-184">Nowe — AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b8b3-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="6b8b3-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6b8b3-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
