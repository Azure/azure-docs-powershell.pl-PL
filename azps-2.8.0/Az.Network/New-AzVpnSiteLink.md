---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869799"
---
# <span data-ttu-id="71e4a-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="71e4a-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="71e4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="71e4a-103">Tworzy obiekt Azure VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="71e4a-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="71e4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71e4a-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71e4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="71e4a-106">Tworzy obiekt Azure VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="71e4a-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="71e4a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71e4a-107">EXAMPLES</span></span>

### <span data-ttu-id="71e4a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71e4a-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="71e4a-109">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN i VpnSite z 1 VpnSiteLinks w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="71e4a-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="71e4a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71e4a-110">PARAMETERS</span></span>

### <span data-ttu-id="71e4a-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="71e4a-111">-BGPAsn</span></span>
<span data-ttu-id="71e4a-112">Protokół BGP ASN dla tego VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="71e4a-112">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="71e4a-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="71e4a-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="71e4a-114">Adres równorzędny BGP dla tego VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="71e4a-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="71e4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e4a-115">-DefaultProfile</span></span>
<span data-ttu-id="71e4a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71e4a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e4a-117">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="71e4a-117">-IPAddress</span></span>
<span data-ttu-id="71e4a-118">Adres IP następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="71e4a-118">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="71e4a-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="71e4a-119">-LinkProviderName</span></span>
<span data-ttu-id="71e4a-120">Nazwa dostawcy linku.</span><span class="sxs-lookup"><span data-stu-id="71e4a-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="71e4a-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="71e4a-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="71e4a-122">Szybkość linku w MB/s.</span><span class="sxs-lookup"><span data-stu-id="71e4a-122">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="71e4a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71e4a-123">-Name</span></span>
<span data-ttu-id="71e4a-124">Nazwę</span><span class="sxs-lookup"><span data-stu-id="71e4a-124">Name</span></span>

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

### <span data-ttu-id="71e4a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e4a-125">CommonParameters</span></span>
<span data-ttu-id="71e4a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e4a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e4a-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71e4a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e4a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e4a-128">INPUTS</span></span>

### <span data-ttu-id="71e4a-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="71e4a-129">None</span></span>

## <span data-ttu-id="71e4a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71e4a-130">OUTPUTS</span></span>

### <span data-ttu-id="71e4a-131">Microsoft. Azure. Commands. Network. models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="71e4a-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="71e4a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71e4a-132">NOTES</span></span>

## <span data-ttu-id="71e4a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71e4a-133">RELATED LINKS</span></span>

[<span data-ttu-id="71e4a-134">Nowe — AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="71e4a-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)