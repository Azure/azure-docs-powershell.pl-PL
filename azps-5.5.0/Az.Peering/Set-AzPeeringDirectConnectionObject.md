---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186666"
---
# <span data-ttu-id="d9959-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="d9959-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="d9959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9959-102">SYNOPSIS</span></span>
<span data-ttu-id="d9959-103">Ustawia lub aktualizuje informacje o połączeniu bezpośrednim.</span><span class="sxs-lookup"><span data-stu-id="d9959-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="d9959-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9959-104">SYNTAX</span></span>

### <span data-ttu-id="d9959-105">Przepustowość (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d9959-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9959-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="d9959-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9959-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="d9959-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9959-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="d9959-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9959-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="d9959-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9959-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9959-110">DESCRIPTION</span></span>
<span data-ttu-id="d9959-111">W połączeniu z funkcją Update-AzPeering jest to operacja w pamięci, która będzie trwała tylko `Update-AzPeering` przez.</span><span class="sxs-lookup"><span data-stu-id="d9959-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="d9959-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9959-112">EXAMPLES</span></span>

### <span data-ttu-id="d9959-113">Przepustowość uaktualnienia</span><span class="sxs-lookup"><span data-stu-id="d9959-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="d9959-114">Uaktualnia przepustowość pierwszego połączenia w obiekcie komunikacji równorzędnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="d9959-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="d9959-115">Aktualizowanie adresu sesji Bgp</span><span class="sxs-lookup"><span data-stu-id="d9959-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="d9959-116">Aktualizuje adres komunikacji równorzędnej dla pierwszego połączenia w obiekcie komunikacji równorzędnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="d9959-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="d9959-117">Używanie aktualizacji do komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="d9959-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="d9959-118">Aktualizuje połączenie do użycia z usługą komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="d9959-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="d9959-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9959-119">PARAMETERS</span></span>

### <span data-ttu-id="d9959-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="d9959-120">-BandwidthInMbps</span></span>
<span data-ttu-id="d9959-121">Przepustowość dostępna w tej lokalizacji w Mb/s.</span><span class="sxs-lookup"><span data-stu-id="d9959-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="d9959-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9959-122">-DefaultProfile</span></span>
<span data-ttu-id="d9959-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9959-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9959-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9959-124">-InputObject</span></span>
<span data-ttu-id="d9959-125">Obiekt połączenia bezpośredniego</span><span class="sxs-lookup"><span data-stu-id="d9959-125">The direct connection Object</span></span>

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

### <span data-ttu-id="d9959-126">-MaxPrefixesAdvertpv4</span><span class="sxs-lookup"><span data-stu-id="d9959-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="d9959-127">Maksymalna anonsowana wartość IPv4</span><span class="sxs-lookup"><span data-stu-id="d9959-127">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="d9959-128">-MaxPrefixesAdvertpv6</span><span class="sxs-lookup"><span data-stu-id="d9959-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="d9959-129">Maksymalna ogłaszana wartość protokołu IPv6</span><span class="sxs-lookup"><span data-stu-id="d9959-129">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="d9959-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="d9959-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="d9959-131">Klucz uwierzytelniania MD5 dla sesji.</span><span class="sxs-lookup"><span data-stu-id="d9959-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="d9959-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="d9959-132">-SessionPrefixV4</span></span>
<span data-ttu-id="d9959-133">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="d9959-133">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="d9959-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="d9959-134">-SessionPrefixV6</span></span>
<span data-ttu-id="d9959-135">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="d9959-135">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="d9959-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="d9959-136">-UseForPeeringService</span></span>
<span data-ttu-id="d9959-137">Włącz możliwość używania z usługą komunikacji równorzędnej firmy Microsoft (MPS).</span><span class="sxs-lookup"><span data-stu-id="d9959-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="d9959-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9959-138">CommonParameters</span></span>
<span data-ttu-id="d9959-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9959-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9959-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9959-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9959-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9959-141">INPUTS</span></span>

### <span data-ttu-id="d9959-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="d9959-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="d9959-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9959-143">OUTPUTS</span></span>

### <span data-ttu-id="d9959-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="d9959-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="d9959-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9959-145">NOTES</span></span>

## <span data-ttu-id="d9959-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9959-146">RELATED LINKS</span></span>
