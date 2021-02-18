---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193259"
---
# <span data-ttu-id="9132c-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9132c-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="9132c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9132c-102">SYNOPSIS</span></span>
<span data-ttu-id="9132c-103">Aktualizuje witrynę VPN.</span><span class="sxs-lookup"><span data-stu-id="9132c-103">Updates a VPN site.</span></span>

## <span data-ttu-id="9132c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9132c-104">SYNTAX</span></span>

### <span data-ttu-id="9132c-105">ByVpnSiteNameNoVirtualWanUpdate (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9132c-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9132c-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9132c-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9132c-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9132c-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9132c-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9132c-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9132c-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9132c-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9132c-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9132c-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9132c-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9132c-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9132c-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="9132c-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9132c-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9132c-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9132c-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9132c-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9132c-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9132c-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9132c-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="9132c-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9132c-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="9132c-117">DESCRIPTION</span></span>
<span data-ttu-id="9132c-118">Polecenie **cmdlet Update-AzVpnSite** aktualizuje witrynę VPN.</span><span class="sxs-lookup"><span data-stu-id="9132c-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="9132c-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9132c-119">EXAMPLES</span></span>

### <span data-ttu-id="9132c-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9132c-120">Example 1</span></span>

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

<span data-ttu-id="9132c-121">Powyższe spowoduje utworzenie grupy zasobów — wirtualnej sieci WAN w zachód Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9132c-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="9132c-122">Następnie tworzy witrynę VpnSite reprezentującą gałąź klienta i łączy ją z wirtualną siecią WAN.</span><span class="sxs-lookup"><span data-stu-id="9132c-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="9132c-123">Po utworzeniu witryny aktualizuje ona adres IpAddress witryny przy użyciu Set-AzVpnSite adresu.</span><span class="sxs-lookup"><span data-stu-id="9132c-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="9132c-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9132c-124">PARAMETERS</span></span>

### <span data-ttu-id="9132c-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="9132c-125">-AddressSpace</span></span>
<span data-ttu-id="9132c-126">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9132c-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="9132c-127">Użyj tego lub AddressSpaceObject, ale nie obu.</span><span class="sxs-lookup"><span data-stu-id="9132c-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="9132c-128">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9132c-128">-AsJob</span></span>
<span data-ttu-id="9132c-129">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9132c-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9132c-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="9132c-130">-BgpAsn</span></span>
<span data-ttu-id="9132c-131">The BGP ASN for this VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9132c-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="9132c-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9132c-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="9132c-133">Adres komunikacji równorzędnej BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="9132c-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="9132c-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="9132c-135">Waga komunikacji równorzędnej BGP dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="9132c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9132c-136">-DefaultProfile</span></span>
<span data-ttu-id="9132c-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9132c-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9132c-138">— DeviceModel</span><span class="sxs-lookup"><span data-stu-id="9132c-138">-DeviceModel</span></span>
<span data-ttu-id="9132c-139">Model urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9132c-140">- DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9132c-140">-DeviceVendor</span></span>
<span data-ttu-id="9132c-141">Dostawca urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="9132c-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9132c-142">-InputObject</span></span>
<span data-ttu-id="9132c-143">Obiekt witryny vpn do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="9132c-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="9132c-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="9132c-144">-IpAddress</span></span>
<span data-ttu-id="9132c-145">Adres IP lokalnej bramy sieciowej.</span><span class="sxs-lookup"><span data-stu-id="9132c-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="9132c-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="9132c-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="9132c-147">Model urządzenia zdalnego połączenia vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9132c-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9132c-148">-Name</span></span>
<span data-ttu-id="9132c-149">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9132c-149">The resource name.</span></span>

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

### <span data-ttu-id="9132c-150">—O365Policy</span><span class="sxs-lookup"><span data-stu-id="9132c-150">-O365Policy</span></span>
<span data-ttu-id="9132c-151">Zasady dotyczące przerw w ruchu usługi Office 365 dla tej lokacji vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="9132c-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9132c-152">-ResourceGroupName</span></span>
<span data-ttu-id="9132c-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9132c-153">The resource group name.</span></span>

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

### <span data-ttu-id="9132c-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9132c-154">-ResourceId</span></span>
<span data-ttu-id="9132c-155">Identyfikator zasobu Azure dla witryny vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="9132c-156">— Tag</span><span class="sxs-lookup"><span data-stu-id="9132c-156">-Tag</span></span>
<span data-ttu-id="9132c-157">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="9132c-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9132c-158">— VirtualWan</span><span class="sxs-lookup"><span data-stu-id="9132c-158">-VirtualWan</span></span>
<span data-ttu-id="9132c-159">Należy połączyć użytkownika VirtualWan z tą lokacją vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9132c-160">— VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="9132c-160">-VirtualWanId</span></span>
<span data-ttu-id="9132c-161">Z wirtualnym urządzeniem ResourceId VirtualWan musi być połączona ta lokacja vpn.</span><span class="sxs-lookup"><span data-stu-id="9132c-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9132c-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9132c-162">-VirtualWanName</span></span>
<span data-ttu-id="9132c-163">Nazwa użytkownika VirtualWan, z który jest połączona ta vpnsite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="9132c-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9132c-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9132c-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="9132c-165">Nazwa grupy zasobów virtualwan, z tą lokacją vpn, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="9132c-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9132c-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="9132c-166">-VpnSiteLink</span></span>
<span data-ttu-id="9132c-167">Lista vpnsitelinków, które ta vpnsite ma.</span><span class="sxs-lookup"><span data-stu-id="9132c-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="9132c-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9132c-168">-Confirm</span></span>
<span data-ttu-id="9132c-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9132c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9132c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9132c-170">-WhatIf</span></span>
<span data-ttu-id="9132c-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9132c-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9132c-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9132c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9132c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9132c-173">CommonParameters</span></span>
<span data-ttu-id="9132c-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9132c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9132c-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9132c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9132c-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9132c-176">INPUTS</span></span>

### <span data-ttu-id="9132c-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="9132c-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="9132c-178">System.String</span><span class="sxs-lookup"><span data-stu-id="9132c-178">System.String</span></span>

## <span data-ttu-id="9132c-179">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9132c-179">OUTPUTS</span></span>

### <span data-ttu-id="9132c-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="9132c-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="9132c-181">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9132c-181">NOTES</span></span>

## <span data-ttu-id="9132c-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9132c-182">RELATED LINKS</span></span>

[<span data-ttu-id="9132c-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9132c-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="9132c-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9132c-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="9132c-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9132c-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
