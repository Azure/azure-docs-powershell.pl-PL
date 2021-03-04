---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: bd9b0b2a61edf70dfb4cebf392bb64fa742c0417
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951434"
---
# <span data-ttu-id="04b65-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04b65-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="04b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b65-102">SYNOPSIS</span></span>
<span data-ttu-id="04b65-103">Aktualizuje witrynę VPN.</span><span class="sxs-lookup"><span data-stu-id="04b65-103">Updates a VPN site.</span></span>

## <span data-ttu-id="04b65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04b65-104">SYNTAX</span></span>

### <span data-ttu-id="04b65-105">ByVpnSiteNameNoVirtualWanUpdate (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="04b65-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b65-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="04b65-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b65-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="04b65-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b65-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="04b65-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b65-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="04b65-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b65-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="04b65-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b65-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="04b65-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b65-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="04b65-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b65-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="04b65-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b65-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="04b65-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b65-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="04b65-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b65-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="04b65-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b65-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="04b65-117">DESCRIPTION</span></span>
<span data-ttu-id="04b65-118">Polecenie **cmdlet Update-AzVpnSite** aktualizuje witrynę VPN.</span><span class="sxs-lookup"><span data-stu-id="04b65-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="04b65-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04b65-119">EXAMPLES</span></span>

### <span data-ttu-id="04b65-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04b65-120">Example 1</span></span>

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

<span data-ttu-id="04b65-121">Powyższe spowoduje utworzenie grupy zasobów o wirtualnej sieci WAN w Zachód USA w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="04b65-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="04b65-122">Następnie tworzy witrynę VpnSite reprezentującą gałąź klienta i łączy ją z wirtualną siecią WAN.</span><span class="sxs-lookup"><span data-stu-id="04b65-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="04b65-123">Po utworzeniu witryny aktualizuje ona adres IpAddress witryny przy użyciu Set-AzVpnSite adresu.</span><span class="sxs-lookup"><span data-stu-id="04b65-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="04b65-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04b65-124">PARAMETERS</span></span>

### <span data-ttu-id="04b65-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="04b65-125">-AddressSpace</span></span>
<span data-ttu-id="04b65-126">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04b65-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="04b65-127">Użyj tej lub AddressSpaceObject, ale nie obu.</span><span class="sxs-lookup"><span data-stu-id="04b65-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="04b65-128">— AsJob</span><span class="sxs-lookup"><span data-stu-id="04b65-128">-AsJob</span></span>
<span data-ttu-id="04b65-129">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="04b65-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04b65-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="04b65-130">-BgpAsn</span></span>
<span data-ttu-id="04b65-131">Asn BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="04b65-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="04b65-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="04b65-133">Adres komunikacji równorzędnej BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="04b65-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="04b65-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="04b65-135">Waga komunikacji równorzędnej BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="04b65-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b65-136">-DefaultProfile</span></span>
<span data-ttu-id="04b65-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04b65-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b65-138">— DeviceModel</span><span class="sxs-lookup"><span data-stu-id="04b65-138">-DeviceModel</span></span>
<span data-ttu-id="04b65-139">Model urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="04b65-140">- DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="04b65-140">-DeviceVendor</span></span>
<span data-ttu-id="04b65-141">Dostawca urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="04b65-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04b65-142">-InputObject</span></span>
<span data-ttu-id="04b65-143">Obiekt witryny vpn do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="04b65-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="04b65-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="04b65-144">-IpAddress</span></span>
<span data-ttu-id="04b65-145">Adres IP lokalnej bramy sieciowej.</span><span class="sxs-lookup"><span data-stu-id="04b65-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="04b65-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="04b65-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="04b65-147">Model urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="04b65-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="04b65-148">-Name</span></span>
<span data-ttu-id="04b65-149">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="04b65-149">The resource name.</span></span>

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

### <span data-ttu-id="04b65-150">—O365Policy</span><span class="sxs-lookup"><span data-stu-id="04b65-150">-O365Policy</span></span>
<span data-ttu-id="04b65-151">Zasady dotyczące przerw w ruchu usługi Office 365 dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="04b65-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b65-152">-ResourceGroupName</span></span>
<span data-ttu-id="04b65-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="04b65-153">The resource group name.</span></span>

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

### <span data-ttu-id="04b65-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04b65-154">-ResourceId</span></span>
<span data-ttu-id="04b65-155">Identyfikator zasobu Azure dla witryny vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="04b65-156">— Tag</span><span class="sxs-lookup"><span data-stu-id="04b65-156">-Tag</span></span>
<span data-ttu-id="04b65-157">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="04b65-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="04b65-158">— VirtualWan</span><span class="sxs-lookup"><span data-stu-id="04b65-158">-VirtualWan</span></span>
<span data-ttu-id="04b65-159">Należy połączyć użytkownika VirtualWan z tą lokacją vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04b65-160">— VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="04b65-160">-VirtualWanId</span></span>
<span data-ttu-id="04b65-161">Z wirtualnym urządzeniem ResourceId VirtualWan musi być połączona ta lokacja vpn.</span><span class="sxs-lookup"><span data-stu-id="04b65-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04b65-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="04b65-162">-VirtualWanName</span></span>
<span data-ttu-id="04b65-163">Nazwa użytkownika VirtualWan, z który jest połączona ta vpnsite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="04b65-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04b65-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b65-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="04b65-165">Nazwa grupy zasobów dla użytkownika VirtualWan, z który jest połączona ta lokacja vpn, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="04b65-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04b65-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="04b65-166">-VpnSiteLink</span></span>
<span data-ttu-id="04b65-167">Lista vpnsitelinków, które ta vpnsite ma.</span><span class="sxs-lookup"><span data-stu-id="04b65-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="04b65-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04b65-168">-Confirm</span></span>
<span data-ttu-id="04b65-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04b65-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b65-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b65-170">-WhatIf</span></span>
<span data-ttu-id="04b65-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04b65-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04b65-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04b65-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b65-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b65-173">CommonParameters</span></span>
<span data-ttu-id="04b65-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b65-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b65-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04b65-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b65-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04b65-176">INPUTS</span></span>

### <span data-ttu-id="04b65-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="04b65-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="04b65-178">System.String</span><span class="sxs-lookup"><span data-stu-id="04b65-178">System.String</span></span>

## <span data-ttu-id="04b65-179">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04b65-179">OUTPUTS</span></span>

### <span data-ttu-id="04b65-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="04b65-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="04b65-181">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04b65-181">NOTES</span></span>

## <span data-ttu-id="04b65-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04b65-182">RELATED LINKS</span></span>

[<span data-ttu-id="04b65-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04b65-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="04b65-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04b65-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="04b65-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04b65-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
