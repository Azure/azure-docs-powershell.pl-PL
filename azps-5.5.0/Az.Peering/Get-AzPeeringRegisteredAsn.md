---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202290"
---
# <span data-ttu-id="472a8-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="472a8-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="472a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="472a8-102">SYNOPSIS</span></span>
<span data-ttu-id="472a8-103">Pobiera zarejestrowaną nazwę ASN dla komunikacji równorzędnej serwera internetowej trasy programu Exchange.</span><span class="sxs-lookup"><span data-stu-id="472a8-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="472a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="472a8-104">SYNTAX</span></span>

### <span data-ttu-id="472a8-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="472a8-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="472a8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="472a8-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="472a8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="472a8-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="472a8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="472a8-108">DESCRIPTION</span></span>
<span data-ttu-id="472a8-109">Pobierz zarejestrowaną asn lub wywszukaj jej listę.</span><span class="sxs-lookup"><span data-stu-id="472a8-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="472a8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="472a8-110">EXAMPLES</span></span>

### <span data-ttu-id="472a8-111">Lista zarejestrowanych sieci ASN do komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="472a8-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="472a8-112">Listy zarejestrowane jako nie.</span><span class="sxs-lookup"><span data-stu-id="472a8-112">Lists registered asn.</span></span>

### <span data-ttu-id="472a8-113">Zostaje zarejestrowana nazwa ASN na celu komunikacji równorzędnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="472a8-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="472a8-114">Zostaje zarejestrowana asn komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="472a8-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="472a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="472a8-115">PARAMETERS</span></span>

### <span data-ttu-id="472a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472a8-116">-DefaultProfile</span></span>
<span data-ttu-id="472a8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="472a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="472a8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="472a8-118">-InputObject</span></span>
<span data-ttu-id="472a8-119">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="472a8-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="472a8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="472a8-120">-Name</span></span>
<span data-ttu-id="472a8-121">Nazwa zarejestrowanego asn</span><span class="sxs-lookup"><span data-stu-id="472a8-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472a8-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="472a8-122">-PeeringName</span></span>
<span data-ttu-id="472a8-123">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="472a8-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="472a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="472a8-125">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="472a8-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472a8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="472a8-126">-ResourceId</span></span>
<span data-ttu-id="472a8-127">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="472a8-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="472a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472a8-128">CommonParameters</span></span>
<span data-ttu-id="472a8-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="472a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472a8-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="472a8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472a8-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="472a8-131">INPUTS</span></span>

### <span data-ttu-id="472a8-132">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="472a8-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="472a8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="472a8-133">System.String</span></span>

## <span data-ttu-id="472a8-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="472a8-134">OUTPUTS</span></span>

### <span data-ttu-id="472a8-135">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="472a8-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="472a8-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="472a8-136">NOTES</span></span>

## <span data-ttu-id="472a8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="472a8-137">RELATED LINKS</span></span>
