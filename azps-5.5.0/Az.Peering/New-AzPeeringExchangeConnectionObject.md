---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202274"
---
# <span data-ttu-id="8b8fb-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8b8fb-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="8b8fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8fb-103">Tworzy w pamięci plik PSObject, który ma być używany do tworzenia lub modyfikowania komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8b8fb-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="8b8fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b8fb-104">SYNTAX</span></span>

### <span data-ttu-id="8b8fb-105">IPv4Address (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8b8fb-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b8fb-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="8b8fb-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b8fb-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="8b8fb-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b8fb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b8fb-108">DESCRIPTION</span></span>
<span data-ttu-id="8b8fb-109">Tworzy w pamięci element PSObject</span><span class="sxs-lookup"><span data-stu-id="8b8fb-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="8b8fb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b8fb-110">EXAMPLES</span></span>

### <span data-ttu-id="8b8fb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b8fb-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="8b8fb-112">Obiekt połączenia lokalnego</span><span class="sxs-lookup"><span data-stu-id="8b8fb-112">Local connection object</span></span>

## <span data-ttu-id="8b8fb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b8fb-113">PARAMETERS</span></span>

### <span data-ttu-id="8b8fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8fb-114">-DefaultProfile</span></span>
<span data-ttu-id="8b8fb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b8fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b8fb-116">-MaxPrefixesAdvertpv4</span><span class="sxs-lookup"><span data-stu-id="8b8fb-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="8b8fb-117">Maksymalna anonsowana wartość protokołu IPv4</span><span class="sxs-lookup"><span data-stu-id="8b8fb-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="8b8fb-118">-MaxPrefixesAdvertpv6</span><span class="sxs-lookup"><span data-stu-id="8b8fb-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="8b8fb-119">Maksymalna ogłaszana wartość protokołu IPv6</span><span class="sxs-lookup"><span data-stu-id="8b8fb-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="8b8fb-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="8b8fb-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="8b8fb-121">Klucz uwierzytelniania MD5 dla sesji.</span><span class="sxs-lookup"><span data-stu-id="8b8fb-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="8b8fb-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="8b8fb-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="8b8fb-123">Identyfikator obiektu komunikacji równorzędnej znaleziony w dniu https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="8b8fb-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="8b8fb-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="8b8fb-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="8b8fb-125">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="8b8fb-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="8b8fb-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="8b8fb-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="8b8fb-127">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="8b8fb-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="8b8fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8fb-128">CommonParameters</span></span>
<span data-ttu-id="8b8fb-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b8fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8fb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b8fb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8fb-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b8fb-131">INPUTS</span></span>

### <span data-ttu-id="8b8fb-132">Brak</span><span class="sxs-lookup"><span data-stu-id="8b8fb-132">None</span></span>

## <span data-ttu-id="8b8fb-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b8fb-133">OUTPUTS</span></span>

### <span data-ttu-id="8b8fb-134">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="8b8fb-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="8b8fb-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b8fb-135">NOTES</span></span>

## <span data-ttu-id="8b8fb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b8fb-136">RELATED LINKS</span></span>
