---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: c878f7559d6e4dcfab79ae9daccaa2f82f548a62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989311"
---
# <span data-ttu-id="3c533-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="3c533-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="3c533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c533-102">SYNOPSIS</span></span>
<span data-ttu-id="3c533-103">Usuwanie zarejestrowanej asn z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="3c533-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="3c533-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c533-104">SYNTAX</span></span>

### <span data-ttu-id="3c533-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="3c533-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c533-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3c533-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c533-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c533-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c533-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c533-108">DESCRIPTION</span></span>
<span data-ttu-id="3c533-109">Umożliwia usunięcie zarejestrowanego asn z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="3c533-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="3c533-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c533-110">EXAMPLES</span></span>

### <span data-ttu-id="3c533-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c533-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="3c533-112">Usuwanie zarejestrowanej asn według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="3c533-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="3c533-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c533-113">PARAMETERS</span></span>

### <span data-ttu-id="3c533-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3c533-114">-AsJob</span></span>
<span data-ttu-id="3c533-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="3c533-115">Run in the background.</span></span>

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

### <span data-ttu-id="3c533-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c533-116">-DefaultProfile</span></span>
<span data-ttu-id="3c533-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c533-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c533-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3c533-118">-Force</span></span>
<span data-ttu-id="3c533-119">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="3c533-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="3c533-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c533-120">-InputObject</span></span>
<span data-ttu-id="3c533-121">Używanie Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3c533-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c533-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3c533-122">-Name</span></span>
<span data-ttu-id="3c533-123">Nazwa zarejestrowanego asn</span><span class="sxs-lookup"><span data-stu-id="3c533-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c533-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c533-124">-PassThru</span></span>
<span data-ttu-id="3c533-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="3c533-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3c533-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="3c533-126">-PeeringName</span></span>
<span data-ttu-id="3c533-127">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3c533-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c533-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c533-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c533-129">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c533-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c533-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c533-130">-ResourceId</span></span>
<span data-ttu-id="3c533-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="3c533-131">The resource id string name.</span></span>

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

### <span data-ttu-id="3c533-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c533-132">-Confirm</span></span>
<span data-ttu-id="3c533-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c533-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c533-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c533-134">-WhatIf</span></span>
<span data-ttu-id="3c533-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c533-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c533-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3c533-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c533-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c533-137">CommonParameters</span></span>
<span data-ttu-id="3c533-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c533-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c533-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c533-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c533-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c533-140">INPUTS</span></span>

### <span data-ttu-id="3c533-141">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3c533-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="3c533-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3c533-142">System.String</span></span>

## <span data-ttu-id="3c533-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c533-143">OUTPUTS</span></span>

### <span data-ttu-id="3c533-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c533-144">System.Boolean</span></span>

## <span data-ttu-id="3c533-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c533-145">NOTES</span></span>

## <span data-ttu-id="3c533-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c533-146">RELATED LINKS</span></span>
