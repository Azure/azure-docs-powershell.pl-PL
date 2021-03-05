---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 8d5567d99d7ba7470fb44738bed128d8a438c733
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989353"
---
# <span data-ttu-id="13411-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="13411-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="13411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13411-102">SYNOPSIS</span></span>
<span data-ttu-id="13411-103">Tworzenie zarejestrowanej asn do komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="13411-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="13411-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13411-104">SYNTAX</span></span>

### <span data-ttu-id="13411-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="13411-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13411-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="13411-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13411-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13411-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13411-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="13411-108">DESCRIPTION</span></span>
<span data-ttu-id="13411-109">Tworzenie zarejestrowanych sieci ASN dla obiektów komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="13411-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="13411-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13411-110">EXAMPLES</span></span>

### <span data-ttu-id="13411-111">Uzyskiwanie komunikacji równorzędnej i tworzenie zarejestrowanej asn</span><span class="sxs-lookup"><span data-stu-id="13411-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="13411-112">Pobierz komunikacji równorzędnej, którą chcesz dodać zarejestrowaną asn.</span><span class="sxs-lookup"><span data-stu-id="13411-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="13411-113">Następnie przekaż je do polecenia polecenia.</span><span class="sxs-lookup"><span data-stu-id="13411-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="13411-114">Tworzenie zarejestrowanego asn przy użyciu elementu resourceId komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="13411-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="13411-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13411-115">PARAMETERS</span></span>

### <span data-ttu-id="13411-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="13411-116">-AsJob</span></span>
<span data-ttu-id="13411-117">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="13411-117">Run in the background.</span></span>

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

### <span data-ttu-id="13411-118">— Asn</span><span class="sxs-lookup"><span data-stu-id="13411-118">-Asn</span></span>
<span data-ttu-id="13411-119">Asn do zarejestrowania</span><span class="sxs-lookup"><span data-stu-id="13411-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="13411-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13411-120">-DefaultProfile</span></span>
<span data-ttu-id="13411-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13411-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13411-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13411-122">-InputObject</span></span>
<span data-ttu-id="13411-123">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="13411-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="13411-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="13411-124">-Name</span></span>
<span data-ttu-id="13411-125">Asn do zarejestrowania</span><span class="sxs-lookup"><span data-stu-id="13411-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="13411-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="13411-126">-PeeringName</span></span>
<span data-ttu-id="13411-127">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="13411-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="13411-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13411-128">-ResourceGroupName</span></span>
<span data-ttu-id="13411-129">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13411-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="13411-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13411-130">-ResourceId</span></span>
<span data-ttu-id="13411-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="13411-131">The resource id string name.</span></span>

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

### <span data-ttu-id="13411-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13411-132">-Confirm</span></span>
<span data-ttu-id="13411-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13411-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13411-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13411-134">-WhatIf</span></span>
<span data-ttu-id="13411-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13411-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13411-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="13411-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13411-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13411-137">CommonParameters</span></span>
<span data-ttu-id="13411-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13411-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13411-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13411-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13411-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13411-140">INPUTS</span></span>

### <span data-ttu-id="13411-141">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="13411-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="13411-142">System.String</span><span class="sxs-lookup"><span data-stu-id="13411-142">System.String</span></span>

## <span data-ttu-id="13411-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13411-143">OUTPUTS</span></span>

### <span data-ttu-id="13411-144">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="13411-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="13411-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13411-145">NOTES</span></span>

## <span data-ttu-id="13411-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13411-146">RELATED LINKS</span></span>
