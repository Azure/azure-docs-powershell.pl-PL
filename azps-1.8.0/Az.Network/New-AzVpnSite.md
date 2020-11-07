---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709203"
---
# <span data-ttu-id="bdafb-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdafb-101">New-AzVpnSite</span></span>

## <span data-ttu-id="bdafb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdafb-102">SYNOPSIS</span></span>
<span data-ttu-id="bdafb-103">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdafb-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="bdafb-104">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="bdafb-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="bdafb-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdafb-105">SYNTAX</span></span>

### <span data-ttu-id="bdafb-106">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdafb-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdafb-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="bdafb-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdafb-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="bdafb-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdafb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bdafb-109">DESCRIPTION</span></span>
<span data-ttu-id="bdafb-110">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdafb-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="bdafb-111">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="bdafb-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="bdafb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdafb-112">EXAMPLES</span></span>

### <span data-ttu-id="bdafb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdafb-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="bdafb-114">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bdafb-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="bdafb-115">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="bdafb-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="bdafb-116">Połączenie IPSec może być następnie skonfigurowane z tą gałęzią i VpnGateway przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="bdafb-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="bdafb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdafb-117">PARAMETERS</span></span>

### <span data-ttu-id="bdafb-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="bdafb-118">-AddressSpace</span></span>
<span data-ttu-id="bdafb-119">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bdafb-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="bdafb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdafb-120">-AsJob</span></span>
<span data-ttu-id="bdafb-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bdafb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdafb-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="bdafb-122">-BgpAsn</span></span>
<span data-ttu-id="bdafb-123">Protokół BGP ASN dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdafb-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="bdafb-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="bdafb-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="bdafb-125">Adres równorzędny BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdafb-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="bdafb-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="bdafb-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="bdafb-127">Waga komunikacji równorzędnej BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdafb-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="bdafb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdafb-128">-DefaultProfile</span></span>
<span data-ttu-id="bdafb-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdafb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdafb-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="bdafb-130">-DeviceModel</span></span>
<span data-ttu-id="bdafb-131">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="bdafb-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="bdafb-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="bdafb-132">-DeviceVendor</span></span>
<span data-ttu-id="bdafb-133">Dostawca urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="bdafb-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="bdafb-134">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="bdafb-134">-IpAddress</span></span>
<span data-ttu-id="bdafb-135">Adres IP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdafb-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="bdafb-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="bdafb-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="bdafb-137">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="bdafb-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="bdafb-138">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bdafb-138">-Location</span></span>
<span data-ttu-id="bdafb-139">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="bdafb-139">The resource location.</span></span>

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

### <span data-ttu-id="bdafb-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdafb-140">-Name</span></span>
<span data-ttu-id="bdafb-141">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bdafb-141">The resource name.</span></span>

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

### <span data-ttu-id="bdafb-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdafb-142">-ResourceGroupName</span></span>
<span data-ttu-id="bdafb-143">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bdafb-143">The resource name.</span></span>

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

### <span data-ttu-id="bdafb-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="bdafb-144">-Tag</span></span>
<span data-ttu-id="bdafb-145">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdafb-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bdafb-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="bdafb-146">-VirtualWan</span></span>
<span data-ttu-id="bdafb-147">VirtualWan ten VpnSite musi być podłączony.</span><span class="sxs-lookup"><span data-stu-id="bdafb-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdafb-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="bdafb-148">-VirtualWanId</span></span>
<span data-ttu-id="bdafb-149">Identyfikator zasobu ResourceId VirtualWan, do którego należy podłączyć ten VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bdafb-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdafb-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="bdafb-150">-VirtualWanName</span></span>
<span data-ttu-id="bdafb-151">Nazwa VirtualWan, do której należy ten VpnSite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="bdafb-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdafb-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdafb-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="bdafb-153">Nazwa grupy zasobów VirtualWan, do której należy ten VpnSite należy połączyć.</span><span class="sxs-lookup"><span data-stu-id="bdafb-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdafb-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdafb-154">-Confirm</span></span>
<span data-ttu-id="bdafb-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdafb-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdafb-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdafb-156">-WhatIf</span></span>
<span data-ttu-id="bdafb-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdafb-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdafb-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdafb-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdafb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdafb-159">CommonParameters</span></span>
<span data-ttu-id="bdafb-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdafb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdafb-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdafb-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdafb-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdafb-162">INPUTS</span></span>

### <span data-ttu-id="bdafb-163">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bdafb-163">None</span></span>

## <span data-ttu-id="bdafb-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdafb-164">OUTPUTS</span></span>

### <span data-ttu-id="bdafb-165">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdafb-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="bdafb-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdafb-166">NOTES</span></span>

## <span data-ttu-id="bdafb-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdafb-167">RELATED LINKS</span></span>

[<span data-ttu-id="bdafb-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdafb-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="bdafb-169">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdafb-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="bdafb-170">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bdafb-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
