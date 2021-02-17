---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189371"
---
# <span data-ttu-id="22829-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="22829-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="22829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22829-102">SYNOPSIS</span></span>
<span data-ttu-id="22829-103">Ustawia lub aktualizuje informacje o połączeniu programu Exchange.</span><span class="sxs-lookup"><span data-stu-id="22829-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="22829-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22829-104">SYNTAX</span></span>

### <span data-ttu-id="22829-105">IPv4Address (domyślna)</span><span class="sxs-lookup"><span data-stu-id="22829-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22829-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="22829-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22829-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="22829-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22829-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="22829-108">DESCRIPTION</span></span>
<span data-ttu-id="22829-109">W połączeniu z funkcją Update-AzPeering jest to operacja w pamięci, która będzie trwała tylko `Update-AzPeering` przez.</span><span class="sxs-lookup"><span data-stu-id="22829-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="22829-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22829-110">EXAMPLES</span></span>

### <span data-ttu-id="22829-111">Aktualizacja skrótu Md5</span><span class="sxs-lookup"><span data-stu-id="22829-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="22829-112">Aktualizuje skrót Md5 dla pierwszego połączenia w obiekcie komunikacji równorzędnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="22829-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="22829-113">Aktualizowanie adresu sesji Bgp</span><span class="sxs-lookup"><span data-stu-id="22829-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="22829-114">Aktualizuje adres komunikacji równorzędnej dla pierwszego połączenia w obiekcie komunikacji równorzędnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="22829-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="22829-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22829-115">PARAMETERS</span></span>

### <span data-ttu-id="22829-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22829-116">-DefaultProfile</span></span>
<span data-ttu-id="22829-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22829-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22829-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22829-118">-InputObject</span></span>
<span data-ttu-id="22829-119">Obiekt połączenia programu Exchange</span><span class="sxs-lookup"><span data-stu-id="22829-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22829-120">-MaxPrefixesAdvertpv4</span><span class="sxs-lookup"><span data-stu-id="22829-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="22829-121">Maksymalna anonsowana wartość protokołu IPv4</span><span class="sxs-lookup"><span data-stu-id="22829-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22829-122">-MaxPrefixesAdvertpv6</span><span class="sxs-lookup"><span data-stu-id="22829-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="22829-123">Maksymalna ogłaszana wartość protokołu IPv6</span><span class="sxs-lookup"><span data-stu-id="22829-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22829-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="22829-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="22829-125">Klucz uwierzytelniania MD5 dla sesji.</span><span class="sxs-lookup"><span data-stu-id="22829-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="22829-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="22829-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="22829-127">Adres IPv4 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="22829-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22829-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="22829-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="22829-129">Adres IPv6 sesji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="22829-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22829-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22829-130">CommonParameters</span></span>
<span data-ttu-id="22829-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22829-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22829-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22829-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22829-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22829-133">INPUTS</span></span>

### <span data-ttu-id="22829-134">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="22829-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="22829-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22829-135">OUTPUTS</span></span>

### <span data-ttu-id="22829-136">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="22829-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="22829-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22829-137">NOTES</span></span>

## <span data-ttu-id="22829-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22829-138">RELATED LINKS</span></span>
