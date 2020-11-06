---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
ms.openlocfilehash: be0fbc9b9fc6d91a5bf94344f432b67dfc38cab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543743"
---
# <span data-ttu-id="93100-101">Get-AzureRmVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="93100-101">Get-AzureRmVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="93100-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93100-102">SYNOPSIS</span></span>
<span data-ttu-id="93100-103">Pobiera konfigurację sieci VPN dla podzestawu VpnSites połączonych z tą siecią WAN za pośrednictwem VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="93100-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="93100-104">Umożliwia przekazanie wygenerowanej konfiguracji sieci VPN do obiektu BLOB magazynowania określonego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="93100-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93100-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93100-105">SYNTAX</span></span>

### <span data-ttu-id="93100-106">ByVirtualWanNameByVpnSiteObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="93100-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93100-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="93100-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93100-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="93100-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93100-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="93100-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93100-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="93100-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93100-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="93100-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93100-112">Opis</span><span class="sxs-lookup"><span data-stu-id="93100-112">DESCRIPTION</span></span>
<span data-ttu-id="93100-113">Pobiera konfigurację sieci VPN dla podzestawu VpnSites połączonych z tą siecią WAN za pośrednictwem VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="93100-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="93100-114">Umożliwia przekazanie wygenerowanej konfiguracji sieci VPN do obiektu BLOB magazynowania określonego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="93100-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="93100-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93100-115">EXAMPLES</span></span>

### <span data-ttu-id="93100-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="93100-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzureRmVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="93100-117">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="93100-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="93100-118">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="93100-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="93100-119">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="93100-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="93100-120">Konfiguracja zostanie następnie pobrana przy użyciu tego unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="93100-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="93100-121">Jeśli unifiedgroup się uda, konfiguracja pobierania zostanie zapisana w obiekcie blob wskazanym przez SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="93100-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="93100-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93100-122">PARAMETERS</span></span>

### <span data-ttu-id="93100-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93100-123">-DefaultProfile</span></span>
<span data-ttu-id="93100-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93100-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93100-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="93100-125">-InputObject</span></span>
<span data-ttu-id="93100-126">Obiekt witryny sieci VPN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="93100-126">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="93100-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93100-127">-Name</span></span>
<span data-ttu-id="93100-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="93100-128">The resource name.</span></span>

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

### <span data-ttu-id="93100-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93100-129">-ResourceGroupName</span></span>
<span data-ttu-id="93100-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93100-130">The resource group name.</span></span>

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

### <span data-ttu-id="93100-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93100-131">-ResourceId</span></span>
<span data-ttu-id="93100-132">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="93100-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="93100-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="93100-133">-StorageSasUrl</span></span>
<span data-ttu-id="93100-134">Adres URL SAS lokalizacji magazynu, w którym ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="93100-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="93100-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="93100-135">-VpnSite</span></span>
<span data-ttu-id="93100-136">Lista identyfikatorów zasobów VpnSite, dla których ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="93100-136">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="93100-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="93100-137">-VpnSiteId</span></span>
<span data-ttu-id="93100-138">Lista identyfikatorów zasobów VpnSite, dla których ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="93100-138">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="93100-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93100-139">-Confirm</span></span>
<span data-ttu-id="93100-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93100-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93100-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93100-141">-WhatIf</span></span>
<span data-ttu-id="93100-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93100-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93100-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="93100-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93100-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93100-144">CommonParameters</span></span>
<span data-ttu-id="93100-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93100-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93100-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93100-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93100-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93100-147">INPUTS</span></span>

### <span data-ttu-id="93100-148">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="93100-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="93100-149">System. String</span><span class="sxs-lookup"><span data-stu-id="93100-149">System.String</span></span>

## <span data-ttu-id="93100-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93100-150">OUTPUTS</span></span>

### <span data-ttu-id="93100-151">Microsoft. Azure. Commands. Network. models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="93100-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="93100-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93100-152">NOTES</span></span>

## <span data-ttu-id="93100-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93100-153">RELATED LINKS</span></span>
