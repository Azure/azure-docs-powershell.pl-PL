---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052889"
---
# <span data-ttu-id="43032-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="43032-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="43032-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43032-102">SYNOPSIS</span></span>
<span data-ttu-id="43032-103">Ustawia lub aktualizuje informacje o połączeniu bezpośrednim.</span><span class="sxs-lookup"><span data-stu-id="43032-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="43032-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43032-104">SYNTAX</span></span>

### <span data-ttu-id="43032-105">Przepustowość (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="43032-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43032-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="43032-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43032-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="43032-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43032-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="43032-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43032-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="43032-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43032-110">Opis</span><span class="sxs-lookup"><span data-stu-id="43032-110">DESCRIPTION</span></span>
<span data-ttu-id="43032-111">W połączeniu z usługą Update-AzPeering jest to operacja w pamięci i będzie trwała tylko z `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="43032-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="43032-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43032-112">EXAMPLES</span></span>

### <span data-ttu-id="43032-113">Przepustowość uaktualnienia</span><span class="sxs-lookup"><span data-stu-id="43032-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="43032-114">Umożliwia uaktualnienie przepustowości dla pierwszego połączenia w obiekcie równorzędnym w pamięci.</span><span class="sxs-lookup"><span data-stu-id="43032-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="43032-115">Aktualizowanie adresu sesji BGP</span><span class="sxs-lookup"><span data-stu-id="43032-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="43032-116">Aktualizuje adres równorzędny dla pierwszego połączenia w obiekcie równorzędnym w pamięci.</span><span class="sxs-lookup"><span data-stu-id="43032-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="43032-117">Aktualizowanie użytkowania usługi peer</span><span class="sxs-lookup"><span data-stu-id="43032-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="43032-118">Aktualizuje połączenie do użytku z usługą komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="43032-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="43032-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43032-119">PARAMETERS</span></span>

### <span data-ttu-id="43032-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="43032-120">-BandwidthInMbps</span></span>
<span data-ttu-id="43032-121">Przepustowość oferowana w tej lokalizacji w MB/s.</span><span class="sxs-lookup"><span data-stu-id="43032-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43032-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43032-122">-DefaultProfile</span></span>
<span data-ttu-id="43032-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43032-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43032-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43032-124">-InputObject</span></span>
<span data-ttu-id="43032-125">Obiekt połączenie bezpośrednie</span><span class="sxs-lookup"><span data-stu-id="43032-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43032-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="43032-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="43032-127">Maksymalny anonsowany protokół IPv4</span><span class="sxs-lookup"><span data-stu-id="43032-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43032-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="43032-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="43032-129">Maksymalny anonsowany protokół IPv6</span><span class="sxs-lookup"><span data-stu-id="43032-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43032-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="43032-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="43032-131">Klucz uwierzytelniania MD5 sesji.</span><span class="sxs-lookup"><span data-stu-id="43032-131">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43032-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="43032-132">-SessionPrefixV4</span></span>
<span data-ttu-id="43032-133">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="43032-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43032-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="43032-134">-SessionPrefixV6</span></span>
<span data-ttu-id="43032-135">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="43032-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43032-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="43032-136">-UseForPeeringService</span></span>
<span data-ttu-id="43032-137">Włącz korzystanie z usługi Microsoft peer Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="43032-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43032-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43032-138">CommonParameters</span></span>
<span data-ttu-id="43032-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43032-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43032-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43032-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43032-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43032-141">INPUTS</span></span>

### <span data-ttu-id="43032-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="43032-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="43032-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43032-143">OUTPUTS</span></span>

### <span data-ttu-id="43032-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="43032-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="43032-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43032-145">NOTES</span></span>

## <span data-ttu-id="43032-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43032-146">RELATED LINKS</span></span>
