---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: ca9235ddfb4b16b80cd0df9ad61bd6936672b889
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872347"
---
# <span data-ttu-id="f179f-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f179f-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="f179f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f179f-102">SYNOPSIS</span></span>
<span data-ttu-id="f179f-103">Ustawia lub aktualizuje informacje o połączeniu bezpośrednim.</span><span class="sxs-lookup"><span data-stu-id="f179f-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="f179f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f179f-104">SYNTAX</span></span>

### <span data-ttu-id="f179f-105">Przepustowość (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f179f-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f179f-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="f179f-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f179f-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="f179f-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f179f-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="f179f-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f179f-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="f179f-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f179f-110">Opis</span><span class="sxs-lookup"><span data-stu-id="f179f-110">DESCRIPTION</span></span>
<span data-ttu-id="f179f-111">W połączeniu z usługą Update-AzPeering jest to operacja w pamięci i będzie trwała tylko z `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="f179f-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="f179f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f179f-112">EXAMPLES</span></span>

### <span data-ttu-id="f179f-113">Przepustowość uaktualnienia</span><span class="sxs-lookup"><span data-stu-id="f179f-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="f179f-114">Umożliwia uaktualnienie przepustowości dla pierwszego połączenia w obiekcie równorzędnym w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f179f-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="f179f-115">Aktualizowanie adresu sesji BGP</span><span class="sxs-lookup"><span data-stu-id="f179f-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="f179f-116">Aktualizuje adres równorzędny dla pierwszego połączenia w obiekcie równorzędnym w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f179f-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="f179f-117">Aktualizowanie użytkowania usługi peer</span><span class="sxs-lookup"><span data-stu-id="f179f-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="f179f-118">Aktualizuje połączenie do użytku z usługą komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="f179f-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="f179f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f179f-119">PARAMETERS</span></span>

### <span data-ttu-id="f179f-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="f179f-120">-BandwidthInMbps</span></span>
<span data-ttu-id="f179f-121">Przepustowość oferowana w tej lokalizacji w MB/s.</span><span class="sxs-lookup"><span data-stu-id="f179f-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="f179f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f179f-122">-DefaultProfile</span></span>
<span data-ttu-id="f179f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f179f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f179f-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f179f-124">-InputObject</span></span>
<span data-ttu-id="f179f-125">Obiekt połączenie bezpośrednie</span><span class="sxs-lookup"><span data-stu-id="f179f-125">The direct connection Object</span></span>

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

### <span data-ttu-id="f179f-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="f179f-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="f179f-127">Maksymalny anonsowany protokół IPv4</span><span class="sxs-lookup"><span data-stu-id="f179f-127">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="f179f-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="f179f-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="f179f-129">Maksymalny anonsowany protokół IPv6</span><span class="sxs-lookup"><span data-stu-id="f179f-129">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="f179f-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="f179f-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="f179f-131">Klucz uwierzytelniania MD5 sesji.</span><span class="sxs-lookup"><span data-stu-id="f179f-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="f179f-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="f179f-132">-SessionPrefixV4</span></span>
<span data-ttu-id="f179f-133">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="f179f-133">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="f179f-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="f179f-134">-SessionPrefixV6</span></span>
<span data-ttu-id="f179f-135">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="f179f-135">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="f179f-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="f179f-136">-UseForPeeringService</span></span>
<span data-ttu-id="f179f-137">Włącz korzystanie z usługi Microsoft peer Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="f179f-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="f179f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f179f-138">CommonParameters</span></span>
<span data-ttu-id="f179f-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f179f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f179f-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f179f-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f179f-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f179f-141">INPUTS</span></span>

### <span data-ttu-id="f179f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="f179f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="f179f-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f179f-143">OUTPUTS</span></span>

### <span data-ttu-id="f179f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="f179f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="f179f-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f179f-145">NOTES</span></span>

## <span data-ttu-id="f179f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f179f-146">RELATED LINKS</span></span>
