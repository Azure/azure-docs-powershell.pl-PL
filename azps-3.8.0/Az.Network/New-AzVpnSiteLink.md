---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049981"
---
# <span data-ttu-id="c0416-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c0416-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="c0416-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0416-102">SYNOPSIS</span></span>
<span data-ttu-id="c0416-103">Tworzy obiekt Azure VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="c0416-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="c0416-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0416-104">SYNTAX</span></span>

### <span data-ttu-id="c0416-105">ByVpnSiteLinkIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0416-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0416-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="c0416-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0416-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c0416-107">DESCRIPTION</span></span>
<span data-ttu-id="c0416-108">Tworzy obiekt Azure VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="c0416-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="c0416-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0416-109">EXAMPLES</span></span>

### <span data-ttu-id="c0416-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0416-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="c0416-111">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN i VpnSite z 1 VpnSiteLinks w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c0416-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="c0416-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0416-112">PARAMETERS</span></span>

### <span data-ttu-id="c0416-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="c0416-113">-BGPAsn</span></span>
<span data-ttu-id="c0416-114">Protokół BGP ASN dla tego VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="c0416-114">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="c0416-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="c0416-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="c0416-116">Adres równorzędny BGP dla tego VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="c0416-116">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="c0416-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0416-117">-DefaultProfile</span></span>
<span data-ttu-id="c0416-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0416-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0416-119">-FQDN</span><span class="sxs-lookup"><span data-stu-id="c0416-119">-Fqdn</span></span>
<span data-ttu-id="c0416-120">Następna nazwa FQDN przeskoku.</span><span class="sxs-lookup"><span data-stu-id="c0416-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0416-121">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="c0416-121">-IPAddress</span></span>
<span data-ttu-id="c0416-122">Adres IP następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="c0416-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0416-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="c0416-123">-LinkProviderName</span></span>
<span data-ttu-id="c0416-124">Nazwa dostawcy linku.</span><span class="sxs-lookup"><span data-stu-id="c0416-124">Link Provider Name.</span></span>

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

### <span data-ttu-id="c0416-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="c0416-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="c0416-126">Szybkość linku w MB/s.</span><span class="sxs-lookup"><span data-stu-id="c0416-126">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="c0416-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0416-127">-Name</span></span>
<span data-ttu-id="c0416-128">Nazwę</span><span class="sxs-lookup"><span data-stu-id="c0416-128">Name</span></span>

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

### <span data-ttu-id="c0416-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0416-129">CommonParameters</span></span>
<span data-ttu-id="c0416-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0416-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0416-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0416-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0416-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0416-132">INPUTS</span></span>

### <span data-ttu-id="c0416-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c0416-133">None</span></span>

## <span data-ttu-id="c0416-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0416-134">OUTPUTS</span></span>

### <span data-ttu-id="c0416-135">Microsoft. Azure. Commands. Network. models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c0416-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="c0416-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0416-136">NOTES</span></span>

## <span data-ttu-id="c0416-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0416-137">RELATED LINKS</span></span>

[<span data-ttu-id="c0416-138">Nowe — AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c0416-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)