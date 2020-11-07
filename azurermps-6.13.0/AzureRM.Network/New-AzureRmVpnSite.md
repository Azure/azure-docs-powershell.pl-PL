---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
ms.openlocfilehash: b8594aab0b9475ed37a0a205010e92fdb2a4db7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716778"
---
# <span data-ttu-id="9e24f-101">New-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="9e24f-101">New-AzureRmVpnSite</span></span>

## <span data-ttu-id="9e24f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e24f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e24f-103">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9e24f-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="9e24f-104">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="9e24f-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e24f-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e24f-105">SYNTAX</span></span>

### <span data-ttu-id="9e24f-106">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e24f-106">ByVirtualWanName (Default)</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e24f-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9e24f-107">ByVirtualWanObject</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e24f-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9e24f-108">ByVirtualWanResourceId</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e24f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9e24f-109">DESCRIPTION</span></span>
<span data-ttu-id="9e24f-110">Tworzy nowy zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9e24f-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="9e24f-111">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="9e24f-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="9e24f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e24f-112">EXAMPLES</span></span>

### <span data-ttu-id="9e24f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e24f-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

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

<span data-ttu-id="9e24f-114">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9e24f-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="9e24f-115">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="9e24f-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="9e24f-116">Połączenie IPSec może być następnie skonfigurowane z tą gałęzią i VpnGateway przy użyciu polecenia New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="9e24f-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="9e24f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e24f-117">PARAMETERS</span></span>

### <span data-ttu-id="9e24f-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="9e24f-118">-AddressSpace</span></span>
<span data-ttu-id="9e24f-119">Prefiksy adresów sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e24f-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="9e24f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e24f-120">-AsJob</span></span>
<span data-ttu-id="9e24f-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9e24f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e24f-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="9e24f-122">-BgpAsn</span></span>
<span data-ttu-id="9e24f-123">Protokół BGP ASN dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9e24f-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="9e24f-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9e24f-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="9e24f-125">Adres równorzędny BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9e24f-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="9e24f-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="9e24f-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="9e24f-127">Waga komunikacji równorzędnej BGP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9e24f-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="9e24f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e24f-128">-DefaultProfile</span></span>
<span data-ttu-id="9e24f-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e24f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e24f-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="9e24f-130">-DeviceModel</span></span>
<span data-ttu-id="9e24f-131">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="9e24f-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9e24f-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9e24f-132">-DeviceVendor</span></span>
<span data-ttu-id="9e24f-133">Dostawca urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="9e24f-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="9e24f-134">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="9e24f-134">-IpAddress</span></span>
<span data-ttu-id="9e24f-135">Adres IP dla tego VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9e24f-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="9e24f-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="9e24f-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="9e24f-137">Model urządzenia zdalnego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="9e24f-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="9e24f-138">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9e24f-138">-Location</span></span>
<span data-ttu-id="9e24f-139">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="9e24f-139">The resource location.</span></span>

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

### <span data-ttu-id="9e24f-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e24f-140">-Name</span></span>
<span data-ttu-id="9e24f-141">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9e24f-141">The resource name.</span></span>

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

### <span data-ttu-id="9e24f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e24f-142">-ResourceGroupName</span></span>
<span data-ttu-id="9e24f-143">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9e24f-143">The resource name.</span></span>

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

### <span data-ttu-id="9e24f-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e24f-144">-Tag</span></span>
<span data-ttu-id="9e24f-145">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e24f-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9e24f-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="9e24f-146">-VirtualWan</span></span>
<span data-ttu-id="9e24f-147">VirtualWan ten VpnSite musi być podłączony.</span><span class="sxs-lookup"><span data-stu-id="9e24f-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9e24f-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="9e24f-148">-VirtualWanId</span></span>
<span data-ttu-id="9e24f-149">Identyfikator zasobu ResourceId VirtualWan, do którego należy podłączyć ten VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9e24f-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9e24f-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9e24f-150">-VirtualWanName</span></span>
<span data-ttu-id="9e24f-151">Nazwa VirtualWan, do której należy ten VpnSite, musi być połączona.</span><span class="sxs-lookup"><span data-stu-id="9e24f-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9e24f-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e24f-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="9e24f-153">Nazwa grupy zasobów VirtualWan, do której należy ten VpnSite należy połączyć.</span><span class="sxs-lookup"><span data-stu-id="9e24f-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="9e24f-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e24f-154">-Confirm</span></span>
<span data-ttu-id="9e24f-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e24f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e24f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e24f-156">-WhatIf</span></span>
<span data-ttu-id="9e24f-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e24f-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e24f-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e24f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e24f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e24f-159">CommonParameters</span></span>
<span data-ttu-id="9e24f-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e24f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e24f-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e24f-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e24f-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e24f-162">INPUTS</span></span>

### <span data-ttu-id="9e24f-163">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e24f-163">None</span></span>

## <span data-ttu-id="9e24f-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e24f-164">OUTPUTS</span></span>

### <span data-ttu-id="9e24f-165">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="9e24f-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="9e24f-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e24f-166">NOTES</span></span>

## <span data-ttu-id="9e24f-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e24f-167">RELATED LINKS</span></span>
