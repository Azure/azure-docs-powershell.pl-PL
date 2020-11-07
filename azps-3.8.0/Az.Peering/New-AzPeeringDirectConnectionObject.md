---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896161"
---
# <span data-ttu-id="64d9d-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="64d9d-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="64d9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="64d9d-103">Tworzy PSObject pamięci w celu użycia do tworzenia lub modyfikowania komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="64d9d-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="64d9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64d9d-104">SYNTAX</span></span>

### <span data-ttu-id="64d9d-105">IPv4PrefixIPv6Prefix (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64d9d-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64d9d-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="64d9d-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64d9d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64d9d-107">DESCRIPTION</span></span>
<span data-ttu-id="64d9d-108">Tworzy w pamięci PSObject</span><span class="sxs-lookup"><span data-stu-id="64d9d-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="64d9d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64d9d-109">EXAMPLES</span></span>

### <span data-ttu-id="64d9d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64d9d-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="64d9d-111">Nowe połączenie lokalne</span><span class="sxs-lookup"><span data-stu-id="64d9d-111">New local connection</span></span>

### <span data-ttu-id="64d9d-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="64d9d-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="64d9d-113">Tworzenie bezpośredniego połączenia równorzędnego z włączonymi usługami równorzędnymi i adresami IP dostarczonymi przez firmę Microsoft</span><span class="sxs-lookup"><span data-stu-id="64d9d-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="64d9d-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="64d9d-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="64d9d-115">Tworzenie bezpośredniego połączenia równorzędnego przy użyciu usług równorzędnych i adresów IP dostarczanych przez elementy równorzędne</span><span class="sxs-lookup"><span data-stu-id="64d9d-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="64d9d-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="64d9d-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="64d9d-117">Utwórz bezpośrednie połączenie równorzędne bez adresów IP sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="64d9d-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="64d9d-118">Aby można było skonfigurować sesję BGP, końcówka musi ustawić adresy IP.</span><span class="sxs-lookup"><span data-stu-id="64d9d-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="64d9d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64d9d-119">PARAMETERS</span></span>

### <span data-ttu-id="64d9d-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="64d9d-120">-BandwidthInMbps</span></span>
<span data-ttu-id="64d9d-121">Przepustowość oferowana w tej lokalizacji w MB/s.</span><span class="sxs-lookup"><span data-stu-id="64d9d-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d9d-122">-DefaultProfile</span></span>
<span data-ttu-id="64d9d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64d9d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64d9d-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="64d9d-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="64d9d-125">Maksymalny anonsowany protokół IPv4</span><span class="sxs-lookup"><span data-stu-id="64d9d-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="64d9d-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="64d9d-127">Maksymalny anonsowany protokół IPv6</span><span class="sxs-lookup"><span data-stu-id="64d9d-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="64d9d-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="64d9d-129">Klucz uwierzytelniania MD5 sesji.</span><span class="sxs-lookup"><span data-stu-id="64d9d-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="64d9d-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="64d9d-131">Flaga włączenia informująca firmę Microsoft o udostępnieniu adresów sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="64d9d-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="64d9d-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="64d9d-133">Znaleziono identyfikator funkcji komunikacji równorzędnej w witrynie https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="64d9d-133">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="64d9d-134">-SessionPrefixV4</span></span>
<span data-ttu-id="64d9d-135">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="64d9d-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="64d9d-136">-SessionPrefixV6</span></span>
<span data-ttu-id="64d9d-137">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="64d9d-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d9d-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="64d9d-138">-UseForPeeringService</span></span>
<span data-ttu-id="64d9d-139">Włącz korzystanie z usługi Microsoft peer Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="64d9d-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="64d9d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d9d-140">CommonParameters</span></span>
<span data-ttu-id="64d9d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d9d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d9d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64d9d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d9d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64d9d-143">INPUTS</span></span>

### <span data-ttu-id="64d9d-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="64d9d-144">None</span></span>

## <span data-ttu-id="64d9d-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64d9d-145">OUTPUTS</span></span>

### <span data-ttu-id="64d9d-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="64d9d-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="64d9d-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64d9d-147">NOTES</span></span>

## <span data-ttu-id="64d9d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64d9d-148">RELATED LINKS</span></span>
