---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c4e57d3d7945f4ae06fc2461e660945bf7edfd6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989360"
---
# <span data-ttu-id="60822-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="60822-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="60822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60822-102">SYNOPSIS</span></span>
<span data-ttu-id="60822-103">Tworzy w pamięci plik PSObject, który ma być używany do tworzenia lub modyfikowania komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="60822-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="60822-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="60822-104">SYNTAX</span></span>

### <span data-ttu-id="60822-105">IPv4Address (domyślna)</span><span class="sxs-lookup"><span data-stu-id="60822-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60822-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="60822-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60822-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="60822-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60822-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="60822-108">DESCRIPTION</span></span>
<span data-ttu-id="60822-109">Tworzy w pamięci element PSObject</span><span class="sxs-lookup"><span data-stu-id="60822-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="60822-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="60822-110">EXAMPLES</span></span>

### <span data-ttu-id="60822-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60822-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="60822-112">Obiekt połączenia lokalnego</span><span class="sxs-lookup"><span data-stu-id="60822-112">Local connection object</span></span>

## <span data-ttu-id="60822-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60822-113">PARAMETERS</span></span>

### <span data-ttu-id="60822-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60822-114">-DefaultProfile</span></span>
<span data-ttu-id="60822-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="60822-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60822-116">-MaxPrefixesAdvertvertpv4</span><span class="sxs-lookup"><span data-stu-id="60822-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="60822-117">Maksymalna anonsowana wartość IPv4</span><span class="sxs-lookup"><span data-stu-id="60822-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="60822-118">-MaxPrefixesAdvertpv6</span><span class="sxs-lookup"><span data-stu-id="60822-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="60822-119">Maksymalna ogłaszana wartość protokołu IPv6</span><span class="sxs-lookup"><span data-stu-id="60822-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="60822-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="60822-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="60822-121">Klucz uwierzytelniania MD5 dla sesji.</span><span class="sxs-lookup"><span data-stu-id="60822-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="60822-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="60822-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="60822-123">Identyfikator obiektu komunikacji równorzędnej znaleziony w dniu https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="60822-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="60822-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="60822-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="60822-125">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="60822-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="60822-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="60822-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="60822-127">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="60822-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="60822-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60822-128">CommonParameters</span></span>
<span data-ttu-id="60822-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60822-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60822-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60822-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60822-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60822-131">INPUTS</span></span>

### <span data-ttu-id="60822-132">Brak</span><span class="sxs-lookup"><span data-stu-id="60822-132">None</span></span>

## <span data-ttu-id="60822-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60822-133">OUTPUTS</span></span>

### <span data-ttu-id="60822-134">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="60822-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="60822-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="60822-135">NOTES</span></span>

## <span data-ttu-id="60822-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60822-136">RELATED LINKS</span></span>
