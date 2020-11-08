---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221900"
---
# <span data-ttu-id="92d0f-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="92d0f-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="92d0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="92d0f-103">Tworzy PSObject pamięci w celu użycia do tworzenia lub modyfikowania komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="92d0f-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="92d0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92d0f-104">SYNTAX</span></span>

### <span data-ttu-id="92d0f-105">IPv4Address (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92d0f-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92d0f-106">Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="92d0f-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92d0f-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="92d0f-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d0f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="92d0f-108">DESCRIPTION</span></span>
<span data-ttu-id="92d0f-109">Tworzy w pamięci PSObject</span><span class="sxs-lookup"><span data-stu-id="92d0f-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="92d0f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92d0f-110">EXAMPLES</span></span>

### <span data-ttu-id="92d0f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92d0f-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="92d0f-112">Obiekt połączenie lokalne</span><span class="sxs-lookup"><span data-stu-id="92d0f-112">Local connection object</span></span>

## <span data-ttu-id="92d0f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92d0f-113">PARAMETERS</span></span>

### <span data-ttu-id="92d0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d0f-114">-DefaultProfile</span></span>
<span data-ttu-id="92d0f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92d0f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d0f-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="92d0f-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="92d0f-117">Maksymalny anonsowany protokół IPv4</span><span class="sxs-lookup"><span data-stu-id="92d0f-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d0f-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="92d0f-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="92d0f-119">Maksymalny anonsowany protokół IPv6</span><span class="sxs-lookup"><span data-stu-id="92d0f-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d0f-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="92d0f-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="92d0f-121">Klucz uwierzytelniania MD5 sesji.</span><span class="sxs-lookup"><span data-stu-id="92d0f-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="92d0f-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="92d0f-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="92d0f-123">Znaleziono identyfikator funkcji komunikacji równorzędnej w witrynie https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="92d0f-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="92d0f-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="92d0f-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="92d0f-125">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="92d0f-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d0f-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="92d0f-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="92d0f-127">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="92d0f-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d0f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d0f-128">CommonParameters</span></span>
<span data-ttu-id="92d0f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d0f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d0f-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92d0f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d0f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92d0f-131">INPUTS</span></span>

### <span data-ttu-id="92d0f-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="92d0f-132">None</span></span>

## <span data-ttu-id="92d0f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92d0f-133">OUTPUTS</span></span>

### <span data-ttu-id="92d0f-134">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="92d0f-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="92d0f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92d0f-135">NOTES</span></span>

## <span data-ttu-id="92d0f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92d0f-136">RELATED LINKS</span></span>
