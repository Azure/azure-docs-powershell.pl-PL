---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193194"
---
# <span data-ttu-id="7cf53-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="7cf53-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="7cf53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf53-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf53-103">Ustawia lub aktualizuje zarejestrowaną asn z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="7cf53-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="7cf53-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7cf53-104">SYNTAX</span></span>

### <span data-ttu-id="7cf53-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7cf53-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf53-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf53-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf53-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf53-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf53-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7cf53-108">DESCRIPTION</span></span>
<span data-ttu-id="7cf53-109">Umożliwia aktualizowanie zarejestrowanej asn z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="7cf53-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="7cf53-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7cf53-110">EXAMPLES</span></span>

### <span data-ttu-id="7cf53-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7cf53-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="7cf53-112">Aktualizuje asn według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7cf53-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="7cf53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf53-113">PARAMETERS</span></span>

### <span data-ttu-id="7cf53-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf53-114">-AsJob</span></span>
<span data-ttu-id="7cf53-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="7cf53-115">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf53-116">— Asn</span><span class="sxs-lookup"><span data-stu-id="7cf53-116">-Asn</span></span>
<span data-ttu-id="7cf53-117">Asn do zarejestrowania</span><span class="sxs-lookup"><span data-stu-id="7cf53-117">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf53-118">-DefaultProfile</span></span>
<span data-ttu-id="7cf53-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf53-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf53-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf53-120">-InputObject</span></span>
<span data-ttu-id="7cf53-121">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="7cf53-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf53-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7cf53-122">-Name</span></span>
<span data-ttu-id="7cf53-123">Asn do zarejestrowania</span><span class="sxs-lookup"><span data-stu-id="7cf53-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf53-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="7cf53-124">-PeeringName</span></span>
<span data-ttu-id="7cf53-125">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7cf53-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7cf53-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf53-126">-ResourceGroupName</span></span>
<span data-ttu-id="7cf53-127">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7cf53-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7cf53-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf53-128">-ResourceId</span></span>
<span data-ttu-id="7cf53-129">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7cf53-129">The resource id string name.</span></span>

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

### <span data-ttu-id="7cf53-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cf53-130">-Confirm</span></span>
<span data-ttu-id="7cf53-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7cf53-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf53-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf53-132">-WhatIf</span></span>
<span data-ttu-id="7cf53-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf53-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf53-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7cf53-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf53-135">CommonParameters</span></span>
<span data-ttu-id="7cf53-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf53-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cf53-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf53-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf53-138">INPUTS</span></span>

### <span data-ttu-id="7cf53-139">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="7cf53-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="7cf53-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7cf53-140">System.String</span></span>

## <span data-ttu-id="7cf53-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf53-141">OUTPUTS</span></span>

### <span data-ttu-id="7cf53-142">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="7cf53-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="7cf53-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7cf53-143">NOTES</span></span>

## <span data-ttu-id="7cf53-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cf53-144">RELATED LINKS</span></span>
