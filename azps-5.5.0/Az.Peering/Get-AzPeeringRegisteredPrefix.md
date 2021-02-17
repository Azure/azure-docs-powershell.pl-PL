---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191458"
---
# <span data-ttu-id="73f4a-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="73f4a-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="73f4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="73f4a-103">Pobiera lub wyświetla zarejestrowany prefiks dla komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="73f4a-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="73f4a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73f4a-104">SYNTAX</span></span>

### <span data-ttu-id="73f4a-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="73f4a-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73f4a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="73f4a-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73f4a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="73f4a-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73f4a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="73f4a-108">DESCRIPTION</span></span>
<span data-ttu-id="73f4a-109">Pobiera lub wyświetla zarejestrowany prefiks dla komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="73f4a-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="73f4a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73f4a-110">EXAMPLES</span></span>

### <span data-ttu-id="73f4a-111">Lista zarejestrowanych asnów komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="73f4a-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="73f4a-112">Listy zarejestrowane jako nie.</span><span class="sxs-lookup"><span data-stu-id="73f4a-112">Lists registered asn.</span></span>

### <span data-ttu-id="73f4a-113">Zostaje zarejestrowana nazwa ASN na celu komunikacji równorzędnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="73f4a-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="73f4a-114">Zostaje zarejestrowana asn komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="73f4a-114">Gets registered peering asn.</span></span>

<span data-ttu-id="73f4a-115">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="73f4a-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="73f4a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73f4a-116">PARAMETERS</span></span>

### <span data-ttu-id="73f4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f4a-117">-DefaultProfile</span></span>
<span data-ttu-id="73f4a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73f4a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f4a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73f4a-119">-InputObject</span></span>
<span data-ttu-id="73f4a-120">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="73f4a-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="73f4a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73f4a-121">-Name</span></span>
<span data-ttu-id="73f4a-122">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="73f4a-122">The name of prefix.</span></span>

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

### <span data-ttu-id="73f4a-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="73f4a-123">-PeeringName</span></span>
<span data-ttu-id="73f4a-124">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="73f4a-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="73f4a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f4a-125">-ResourceGroupName</span></span>
<span data-ttu-id="73f4a-126">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73f4a-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="73f4a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f4a-127">-ResourceId</span></span>
<span data-ttu-id="73f4a-128">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="73f4a-128">The resource id string name.</span></span>

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

### <span data-ttu-id="73f4a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f4a-129">CommonParameters</span></span>
<span data-ttu-id="73f4a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f4a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f4a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73f4a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f4a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73f4a-132">INPUTS</span></span>

### <span data-ttu-id="73f4a-133">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="73f4a-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="73f4a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="73f4a-134">System.String</span></span>

## <span data-ttu-id="73f4a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73f4a-135">OUTPUTS</span></span>

### <span data-ttu-id="73f4a-136">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="73f4a-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="73f4a-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73f4a-137">NOTES</span></span>

## <span data-ttu-id="73f4a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73f4a-138">RELATED LINKS</span></span>
