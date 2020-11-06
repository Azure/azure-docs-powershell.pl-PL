---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
ms.openlocfilehash: fa24f61d0e638cb38e7cf882aac2191a5119b1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547416"
---
# <span data-ttu-id="80d13-101">Update-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="80d13-101">Update-AzureRmVpnSite</span></span>

## <span data-ttu-id="80d13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80d13-102">SYNOPSIS</span></span>
<span data-ttu-id="80d13-103">Aktualizuje VpnSite reprezentujący oddział klienta do zamierzonego stanu celu.</span><span class="sxs-lookup"><span data-stu-id="80d13-103">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80d13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80d13-104">SYNTAX</span></span>

### <span data-ttu-id="80d13-105">ByVpnSiteNameNoVirtualWanUpdate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80d13-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="80d13-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="80d13-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="80d13-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="80d13-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="80d13-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="80d13-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="80d13-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="80d13-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="80d13-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="80d13-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d13-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="80d13-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d13-117">Opis</span><span class="sxs-lookup"><span data-stu-id="80d13-117">DESCRIPTION</span></span>
<span data-ttu-id="80d13-118">Aktualizuje VpnSite reprezentujący oddział klienta do zamierzonego stanu celu.</span><span class="sxs-lookup"><span data-stu-id="80d13-118">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

## <span data-ttu-id="80d13-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80d13-119">EXAMPLES</span></span>

### <span data-ttu-id="80d13-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80d13-120">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

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

<span data-ttu-id="80d13-121">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="80d13-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="80d13-122">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="80d13-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="80d13-123">Po utworzeniu witryny wiadomość zostanie zaktualizowana w adresie IP witryny przy użyciu polecenia Set-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="80d13-123">Once the site is created, it updates the IpAddress of the site using the Set-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="80d13-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80d13-124">PARAMETERS</span></span>

### <span data-ttu-id="80d13-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="80d13-125">-AddressSpace</span></span>
<span data-ttu-id="80d13-126">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80d13-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="80d13-127">Użyj tego lub AddressSpaceObject, ale nie obu.</span><span class="sxs-lookup"><span data-stu-id="80d13-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d13-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80d13-128">-AsJob</span></span>
<span data-ttu-id="80d13-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="80d13-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80d13-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="80d13-130">-BgpAsn</span></span>
<span data-ttu-id="80d13-131">Protokół BGP ASN dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="80d13-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="80d13-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="80d13-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="80d13-133">Adres równorzędny BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="80d13-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="80d13-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="80d13-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="80d13-135">Waga komunikacji równorzędnej BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="80d13-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="80d13-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d13-136">-DefaultProfile</span></span>
<span data-ttu-id="80d13-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80d13-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d13-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="80d13-138">-DeviceModel</span></span>
<span data-ttu-id="80d13-139">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="80d13-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="80d13-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="80d13-140">-DeviceVendor</span></span>
<span data-ttu-id="80d13-141">Dostawca urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="80d13-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="80d13-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80d13-142">-InputObject</span></span>
<span data-ttu-id="80d13-143">Obiekt witryny sieci VPN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="80d13-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="80d13-144">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="80d13-144">-IpAddress</span></span>
<span data-ttu-id="80d13-145">Adres IP bramy sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="80d13-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="80d13-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="80d13-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="80d13-147">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="80d13-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="80d13-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80d13-148">-Name</span></span>
<span data-ttu-id="80d13-149">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="80d13-149">The resource name.</span></span>

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

### <span data-ttu-id="80d13-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d13-150">-ResourceGroupName</span></span>
<span data-ttu-id="80d13-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="80d13-151">The resource group name.</span></span>

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

### <span data-ttu-id="80d13-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80d13-152">-ResourceId</span></span>
<span data-ttu-id="80d13-153">Identyfikator zasobu platformy Azure dla witryny sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="80d13-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="80d13-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="80d13-154">-Tag</span></span>
<span data-ttu-id="80d13-155">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="80d13-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="80d13-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="80d13-156">-VirtualWan</span></span>
<span data-ttu-id="80d13-157">VirtualWan ten VpnSite musi być podłączony.</span><span class="sxs-lookup"><span data-stu-id="80d13-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="80d13-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="80d13-158">-VirtualWanId</span></span>
<span data-ttu-id="80d13-159">Identyfikator zasobu ResourceId VirtualWan, do którego należy podłączyć ten VpnSite.</span><span class="sxs-lookup"><span data-stu-id="80d13-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="80d13-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="80d13-160">-VirtualWanName</span></span>
<span data-ttu-id="80d13-161">Nazwa VirtualWan, do której należy ten VpnSite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="80d13-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="80d13-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d13-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="80d13-163">Nazwa grupy zasobów VirtualWan, do której należy ten VpnSite należy połączyć.</span><span class="sxs-lookup"><span data-stu-id="80d13-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="80d13-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80d13-164">-Confirm</span></span>
<span data-ttu-id="80d13-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d13-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d13-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d13-166">-WhatIf</span></span>
<span data-ttu-id="80d13-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d13-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d13-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80d13-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d13-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d13-169">CommonParameters</span></span>
<span data-ttu-id="80d13-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d13-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d13-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80d13-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d13-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80d13-172">INPUTS</span></span>

### <span data-ttu-id="80d13-173">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="80d13-173">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="80d13-174">System. String</span><span class="sxs-lookup"><span data-stu-id="80d13-174">System.String</span></span>

## <span data-ttu-id="80d13-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80d13-175">OUTPUTS</span></span>

### <span data-ttu-id="80d13-176">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="80d13-176">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="80d13-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80d13-177">NOTES</span></span>

## <span data-ttu-id="80d13-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80d13-178">RELATED LINKS</span></span>
