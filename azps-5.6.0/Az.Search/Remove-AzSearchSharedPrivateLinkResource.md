---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ed5c5bf502e1d19b0ba095e5db68f1f116a71137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955658"
---
# <span data-ttu-id="38c0d-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="38c0d-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="38c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="38c0d-103">Usuń udostępniony prywatny zasób linków z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="38c0d-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="38c0d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38c0d-104">SYNTAX</span></span>

### <span data-ttu-id="38c0d-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="38c0d-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38c0d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38c0d-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c0d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38c0d-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c0d-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38c0d-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c0d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="38c0d-109">DESCRIPTION</span></span>
<span data-ttu-id="38c0d-110">Polecenie **cmdlet Remove-AzSearchSharedPrivateLinkResource** usuwa udostępniony zasób linku prywatnego z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="38c0d-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="38c0d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38c0d-111">EXAMPLES</span></span>

### <span data-ttu-id="38c0d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38c0d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="38c0d-113">W tym przykładzie udostępniony prywatny zasób linku jest usuwany według nazwy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="38c0d-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="38c0d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38c0d-114">PARAMETERS</span></span>

### <span data-ttu-id="38c0d-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="38c0d-115">-AsJob</span></span>
<span data-ttu-id="38c0d-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="38c0d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38c0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c0d-117">-DefaultProfile</span></span>
<span data-ttu-id="38c0d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="38c0d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38c0d-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="38c0d-119">-Force</span></span>
<span data-ttu-id="38c0d-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38c0d-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="38c0d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38c0d-121">-InputObject</span></span>
<span data-ttu-id="38c0d-122">Udostępniony obiekt wejściowy zasobu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="38c0d-122">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c0d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="38c0d-123">-Name</span></span>
<span data-ttu-id="38c0d-124">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="38c0d-124">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0d-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="38c0d-125">-ParentObject</span></span>
<span data-ttu-id="38c0d-126">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="38c0d-126">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c0d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38c0d-127">-PassThru</span></span>
<span data-ttu-id="38c0d-128">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="38c0d-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="38c0d-129">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="38c0d-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="38c0d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c0d-130">-ResourceGroupName</span></span>
<span data-ttu-id="38c0d-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="38c0d-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38c0d-132">-ResourceId</span></span>
<span data-ttu-id="38c0d-133">Udostępniony identyfikator zasobu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="38c0d-133">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0d-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="38c0d-134">-ServiceName</span></span>
<span data-ttu-id="38c0d-135">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="38c0d-135">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0d-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38c0d-136">-Confirm</span></span>
<span data-ttu-id="38c0d-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38c0d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c0d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c0d-138">-WhatIf</span></span>
<span data-ttu-id="38c0d-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c0d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c0d-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="38c0d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c0d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c0d-141">CommonParameters</span></span>
<span data-ttu-id="38c0d-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c0d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c0d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38c0d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c0d-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38c0d-144">INPUTS</span></span>

### <span data-ttu-id="38c0d-145">Brak</span><span class="sxs-lookup"><span data-stu-id="38c0d-145">None</span></span>

## <span data-ttu-id="38c0d-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38c0d-146">OUTPUTS</span></span>

### <span data-ttu-id="38c0d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38c0d-147">System.Boolean</span></span>

## <span data-ttu-id="38c0d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38c0d-148">NOTES</span></span>

## <span data-ttu-id="38c0d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38c0d-149">RELATED LINKS</span></span>

[<span data-ttu-id="38c0d-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="38c0d-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="38c0d-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="38c0d-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="38c0d-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="38c0d-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)