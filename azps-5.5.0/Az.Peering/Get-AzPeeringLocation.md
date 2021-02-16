---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: 233cf87eed682919df8ca0ae38fefaec5964942c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179218"
---
# <span data-ttu-id="b4a61-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b4a61-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="b4a61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a61-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a61-103">Pobiera lokalizacje komunikacji równorzędnej oferowane przez firmę Microsoft</span><span class="sxs-lookup"><span data-stu-id="b4a61-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="b4a61-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4a61-104">SYNTAX</span></span>

### <span data-ttu-id="b4a61-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b4a61-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a61-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="b4a61-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4a61-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="b4a61-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4a61-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4a61-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a61-109">Pobiera obiekty komunikacji równorzędnej, w których użytkownicy mogą łączyć się z ARM.</span><span class="sxs-lookup"><span data-stu-id="b4a61-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="b4a61-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4a61-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a61-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4a61-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="b4a61-112">Jest to długa lista lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b4a61-112">Its a long list of locations.</span></span> <span data-ttu-id="b4a61-113">Otrzymuje dostęp do wszystkich obiektów bezpośredniej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="b4a61-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="b4a61-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4a61-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="b4a61-115">Pobiera lokalizację komunikacji równorzędnej programu Exchange dla Honolulu.</span><span class="sxs-lookup"><span data-stu-id="b4a61-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="b4a61-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b4a61-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="b4a61-117">Pobiera lokalizację komunikacji równorzędnej programu Exchange dla obiektu komunikacji równorzędnej o identyfikatorze 71.</span><span class="sxs-lookup"><span data-stu-id="b4a61-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="b4a61-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4a61-118">PARAMETERS</span></span>

### <span data-ttu-id="b4a61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a61-119">-DefaultProfile</span></span>
<span data-ttu-id="b4a61-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a61-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a61-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="b4a61-121">-DirectPeeringType</span></span>
<span data-ttu-id="b4a61-122">Wybierz pozycję "Edge", "CDN" i "Transit".</span><span class="sxs-lookup"><span data-stu-id="b4a61-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a61-123">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="b4a61-123">-Kind</span></span>
<span data-ttu-id="b4a61-124">Pokazuje wszystkie zasoby komunikacji równorzędnej według typu.</span><span class="sxs-lookup"><span data-stu-id="b4a61-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a61-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="b4a61-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="b4a61-126">Identyfikator PeeringDB.com obiektu</span><span class="sxs-lookup"><span data-stu-id="b4a61-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a61-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b4a61-127">-PeeringLocation</span></span>
<span data-ttu-id="b4a61-128">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b4a61-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a61-129">CommonParameters</span></span>
<span data-ttu-id="b4a61-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a61-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4a61-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a61-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4a61-132">INPUTS</span></span>

### <span data-ttu-id="b4a61-133">Brak</span><span class="sxs-lookup"><span data-stu-id="b4a61-133">None</span></span>

## <span data-ttu-id="b4a61-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4a61-134">OUTPUTS</span></span>

### <span data-ttu-id="b4a61-135">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b4a61-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="b4a61-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4a61-136">NOTES</span></span>

## <span data-ttu-id="b4a61-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4a61-137">RELATED LINKS</span></span>
