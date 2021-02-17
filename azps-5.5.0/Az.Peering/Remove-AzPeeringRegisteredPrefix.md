---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240347"
---
# <span data-ttu-id="62ff5-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="62ff5-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="62ff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="62ff5-103">Usuwanie zarejestrowanego prefiksu z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="62ff5-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="62ff5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62ff5-104">SYNTAX</span></span>

### <span data-ttu-id="62ff5-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="62ff5-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62ff5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="62ff5-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ff5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="62ff5-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ff5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="62ff5-108">DESCRIPTION</span></span>
<span data-ttu-id="62ff5-109">Umożliwia usunięcie zarejestrowanego prefiksu z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="62ff5-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="62ff5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62ff5-110">EXAMPLES</span></span>

### <span data-ttu-id="62ff5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62ff5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="62ff5-112">Usuwanie zarejestrowanego prefiksu według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="62ff5-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="62ff5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62ff5-113">PARAMETERS</span></span>

### <span data-ttu-id="62ff5-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="62ff5-114">-AsJob</span></span>
<span data-ttu-id="62ff5-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="62ff5-115">Run in the background.</span></span>

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

### <span data-ttu-id="62ff5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ff5-116">-DefaultProfile</span></span>
<span data-ttu-id="62ff5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62ff5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62ff5-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="62ff5-118">-Force</span></span>
<span data-ttu-id="62ff5-119">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="62ff5-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="62ff5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62ff5-120">-InputObject</span></span>
<span data-ttu-id="62ff5-121">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="62ff5-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="62ff5-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="62ff5-122">-Name</span></span>
<span data-ttu-id="62ff5-123">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="62ff5-123">The name of prefix.</span></span>

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

### <span data-ttu-id="62ff5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62ff5-124">-PassThru</span></span>
<span data-ttu-id="62ff5-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="62ff5-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="62ff5-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="62ff5-126">-PeeringName</span></span>
<span data-ttu-id="62ff5-127">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="62ff5-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="62ff5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ff5-128">-ResourceGroupName</span></span>
<span data-ttu-id="62ff5-129">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62ff5-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="62ff5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62ff5-130">-ResourceId</span></span>
<span data-ttu-id="62ff5-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="62ff5-131">The resource id string name.</span></span>

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

### <span data-ttu-id="62ff5-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62ff5-132">-Confirm</span></span>
<span data-ttu-id="62ff5-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62ff5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ff5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ff5-134">-WhatIf</span></span>
<span data-ttu-id="62ff5-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ff5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ff5-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62ff5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ff5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ff5-137">CommonParameters</span></span>
<span data-ttu-id="62ff5-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ff5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ff5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62ff5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ff5-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ff5-140">INPUTS</span></span>

### <span data-ttu-id="62ff5-141">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="62ff5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="62ff5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="62ff5-142">System.String</span></span>

## <span data-ttu-id="62ff5-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62ff5-143">OUTPUTS</span></span>

### <span data-ttu-id="62ff5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62ff5-144">System.Boolean</span></span>

## <span data-ttu-id="62ff5-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62ff5-145">NOTES</span></span>

## <span data-ttu-id="62ff5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62ff5-146">RELATED LINKS</span></span>
