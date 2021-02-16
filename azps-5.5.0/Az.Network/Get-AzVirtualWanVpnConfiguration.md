---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: 6e67f192cab1d1183d8c8cfd1a38f6c398311bf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191939"
---
# <span data-ttu-id="580b9-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="580b9-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="580b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="580b9-102">SYNOPSIS</span></span>
<span data-ttu-id="580b9-103">Pobiera konfigurację sieci Vpn dla podzestawu vpnsites połączonych z tą siecią WAN za pośrednictwem sieci VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="580b9-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="580b9-104">Przesyła wygenerowaną konfigurację sieci Vpn do obiektu blob magazynu określonego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="580b9-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="580b9-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="580b9-105">SYNTAX</span></span>

### <span data-ttu-id="580b9-106">ByVirtualWanNameByVpnSiteObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="580b9-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="580b9-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="580b9-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="580b9-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="580b9-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="580b9-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="580b9-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="580b9-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="580b9-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="580b9-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="580b9-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="580b9-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="580b9-112">DESCRIPTION</span></span>
<span data-ttu-id="580b9-113">Pobiera konfigurację sieci Vpn dla podzestawu vpnsites połączonych z tą siecią WAN za pośrednictwem sieci VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="580b9-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="580b9-114">Przesyła wygenerowaną konfigurację sieci Vpn do obiektu blob magazynu określonego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="580b9-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="580b9-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="580b9-115">EXAMPLES</span></span>

### <span data-ttu-id="580b9-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="580b9-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="580b9-117">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="580b9-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="580b9-118">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="580b9-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="580b9-119">Po utworzeniu brama jest połączona z lokacją VpnSite za pomocą New-AzVpnConnection sieci.</span><span class="sxs-lookup"><span data-stu-id="580b9-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="580b9-120">Konfiguracja zostanie pobrana za pomocą tego polecenia commandlet.</span><span class="sxs-lookup"><span data-stu-id="580b9-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="580b9-121">Jeśli polecenie polecenia powiedzie się, konfiguracja pobierania zostanie napisana w obiekcie blob wskazanym przez obiekt SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="580b9-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="580b9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="580b9-122">PARAMETERS</span></span>

### <span data-ttu-id="580b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580b9-123">-DefaultProfile</span></span>
<span data-ttu-id="580b9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="580b9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="580b9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="580b9-125">-InputObject</span></span>
<span data-ttu-id="580b9-126">Obiekt witryny vpn do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="580b9-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="580b9-127">-Name</span></span>
<span data-ttu-id="580b9-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="580b9-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="580b9-129">-ResourceGroupName</span></span>
<span data-ttu-id="580b9-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="580b9-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="580b9-131">-ResourceId</span></span>
<span data-ttu-id="580b9-132">Identyfikator zasobu Azure dla wirtualnej sieci Wan.</span><span class="sxs-lookup"><span data-stu-id="580b9-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-133">- StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="580b9-133">-StorageSasUrl</span></span>
<span data-ttu-id="580b9-134">Adres URL SAS lokalizacji przechowywania, w której ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="580b9-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="580b9-135">- VpnSite</span><span class="sxs-lookup"><span data-stu-id="580b9-135">-VpnSite</span></span>
<span data-ttu-id="580b9-136">Lista identyfikatorów zasobów vpnsite, dla których ma być generowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="580b9-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="580b9-137">-VpnSiteId</span></span>
<span data-ttu-id="580b9-138">Lista identyfikatorów zasobów vpnsite, dla których ma być generowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="580b9-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="580b9-139">-Confirm</span></span>
<span data-ttu-id="580b9-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="580b9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="580b9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="580b9-141">-WhatIf</span></span>
<span data-ttu-id="580b9-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="580b9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="580b9-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="580b9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="580b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580b9-144">CommonParameters</span></span>
<span data-ttu-id="580b9-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="580b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580b9-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="580b9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580b9-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="580b9-147">INPUTS</span></span>

### <span data-ttu-id="580b9-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="580b9-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="580b9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="580b9-149">System.String</span></span>

## <span data-ttu-id="580b9-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="580b9-150">OUTPUTS</span></span>

### <span data-ttu-id="580b9-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="580b9-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="580b9-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="580b9-152">NOTES</span></span>

## <span data-ttu-id="580b9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="580b9-153">RELATED LINKS</span></span>
