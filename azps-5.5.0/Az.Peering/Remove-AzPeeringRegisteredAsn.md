---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240354"
---
# <span data-ttu-id="2ba08-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="2ba08-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="2ba08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba08-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba08-103">Usuwanie zarejestrowanej asn z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="2ba08-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="2ba08-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ba08-104">SYNTAX</span></span>

### <span data-ttu-id="2ba08-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="2ba08-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba08-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba08-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba08-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba08-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba08-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ba08-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba08-109">Umożliwia usunięcie zarejestrowanej asn z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="2ba08-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="2ba08-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ba08-110">EXAMPLES</span></span>

### <span data-ttu-id="2ba08-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ba08-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="2ba08-112">Usuwanie zarejestrowanej asn według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="2ba08-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="2ba08-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ba08-113">PARAMETERS</span></span>

### <span data-ttu-id="2ba08-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2ba08-114">-AsJob</span></span>
<span data-ttu-id="2ba08-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="2ba08-115">Run in the background.</span></span>

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

### <span data-ttu-id="2ba08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba08-116">-DefaultProfile</span></span>
<span data-ttu-id="2ba08-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ba08-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2ba08-118">-Force</span></span>
<span data-ttu-id="2ba08-119">Wymusz ukończenie operacji</span><span class="sxs-lookup"><span data-stu-id="2ba08-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="2ba08-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba08-120">-InputObject</span></span>
<span data-ttu-id="2ba08-121">Używanie Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="2ba08-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="2ba08-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ba08-122">-Name</span></span>
<span data-ttu-id="2ba08-123">Nazwa zarejestrowanego asn</span><span class="sxs-lookup"><span data-stu-id="2ba08-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="2ba08-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ba08-124">-PassThru</span></span>
<span data-ttu-id="2ba08-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2ba08-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2ba08-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="2ba08-126">-PeeringName</span></span>
<span data-ttu-id="2ba08-127">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2ba08-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2ba08-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba08-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ba08-129">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ba08-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="2ba08-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba08-130">-ResourceId</span></span>
<span data-ttu-id="2ba08-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="2ba08-131">The resource id string name.</span></span>

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

### <span data-ttu-id="2ba08-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ba08-132">-Confirm</span></span>
<span data-ttu-id="2ba08-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ba08-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba08-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba08-134">-WhatIf</span></span>
<span data-ttu-id="2ba08-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba08-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba08-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ba08-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba08-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba08-137">CommonParameters</span></span>
<span data-ttu-id="2ba08-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba08-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba08-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ba08-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba08-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ba08-140">INPUTS</span></span>

### <span data-ttu-id="2ba08-141">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="2ba08-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="2ba08-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2ba08-142">System.String</span></span>

## <span data-ttu-id="2ba08-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ba08-143">OUTPUTS</span></span>

### <span data-ttu-id="2ba08-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ba08-144">System.Boolean</span></span>

## <span data-ttu-id="2ba08-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ba08-145">NOTES</span></span>

## <span data-ttu-id="2ba08-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ba08-146">RELATED LINKS</span></span>
