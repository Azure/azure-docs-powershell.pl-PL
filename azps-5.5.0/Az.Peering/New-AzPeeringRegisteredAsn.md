---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202267"
---
# <span data-ttu-id="5a7fb-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="5a7fb-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="5a7fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7fb-103">Tworzenie zarejestrowanej asn do komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="5a7fb-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="5a7fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a7fb-104">SYNTAX</span></span>

### <span data-ttu-id="5a7fb-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5a7fb-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7fb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a7fb-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7fb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7fb-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7fb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a7fb-108">DESCRIPTION</span></span>
<span data-ttu-id="5a7fb-109">Tworzenie zarejestrowanych sieci ASN dla obiektów komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="5a7fb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a7fb-110">EXAMPLES</span></span>

### <span data-ttu-id="5a7fb-111">Uzyskiwanie komunikacji równorzędnej i tworzenie zarejestrowanej asn</span><span class="sxs-lookup"><span data-stu-id="5a7fb-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="5a7fb-112">Pobierz komunikacji równorzędnej, którą chcesz dodać zarejestrowaną asn.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="5a7fb-113">Następnie przekaż je do polecenia polecenia.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="5a7fb-114">Tworzenie zarejestrowanego asn przy użyciu elementu resourceId komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="5a7fb-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="5a7fb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a7fb-115">PARAMETERS</span></span>

### <span data-ttu-id="5a7fb-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5a7fb-116">-AsJob</span></span>
<span data-ttu-id="5a7fb-117">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-117">Run in the background.</span></span>

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

### <span data-ttu-id="5a7fb-118">— Asn</span><span class="sxs-lookup"><span data-stu-id="5a7fb-118">-Asn</span></span>
<span data-ttu-id="5a7fb-119">Asn do zarejestrowania</span><span class="sxs-lookup"><span data-stu-id="5a7fb-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="5a7fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7fb-120">-DefaultProfile</span></span>
<span data-ttu-id="5a7fb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a7fb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a7fb-122">-InputObject</span></span>
<span data-ttu-id="5a7fb-123">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="5a7fb-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fb-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a7fb-124">-Name</span></span>
<span data-ttu-id="5a7fb-125">Asn do zarejestrowania</span><span class="sxs-lookup"><span data-stu-id="5a7fb-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fb-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="5a7fb-126">-PeeringName</span></span>
<span data-ttu-id="5a7fb-127">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="5a7fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a7fb-129">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="5a7fb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7fb-130">-ResourceId</span></span>
<span data-ttu-id="5a7fb-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-131">The resource id string name.</span></span>

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

### <span data-ttu-id="5a7fb-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a7fb-132">-Confirm</span></span>
<span data-ttu-id="5a7fb-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7fb-134">-WhatIf</span></span>
<span data-ttu-id="5a7fb-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a7fb-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7fb-137">CommonParameters</span></span>
<span data-ttu-id="5a7fb-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7fb-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a7fb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7fb-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a7fb-140">INPUTS</span></span>

### <span data-ttu-id="5a7fb-141">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="5a7fb-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="5a7fb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5a7fb-142">System.String</span></span>

## <span data-ttu-id="5a7fb-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a7fb-143">OUTPUTS</span></span>

### <span data-ttu-id="5a7fb-144">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="5a7fb-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="5a7fb-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a7fb-145">NOTES</span></span>

## <span data-ttu-id="5a7fb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a7fb-146">RELATED LINKS</span></span>
