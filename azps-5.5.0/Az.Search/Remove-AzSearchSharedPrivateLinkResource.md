---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 922989583a071384de98343e12d48ce68cc32db8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239994"
---
# <span data-ttu-id="1840f-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1840f-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="1840f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1840f-102">SYNOPSIS</span></span>
<span data-ttu-id="1840f-103">Usuń udostępniony prywatny zasób linków z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1840f-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1840f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1840f-104">SYNTAX</span></span>

### <span data-ttu-id="1840f-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1840f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1840f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1840f-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1840f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1840f-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1840f-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1840f-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1840f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1840f-109">DESCRIPTION</span></span>
<span data-ttu-id="1840f-110">Polecenie **cmdlet Remove-AzSearchSharedPrivateLinkResource** usuwa udostępniony zasób linku prywatnego z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1840f-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1840f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1840f-111">EXAMPLES</span></span>

### <span data-ttu-id="1840f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1840f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="1840f-113">W tym przykładzie udostępniony prywatny zasób linku jest usuwany według nazwy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1840f-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1840f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1840f-114">PARAMETERS</span></span>

### <span data-ttu-id="1840f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1840f-115">-AsJob</span></span>
<span data-ttu-id="1840f-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1840f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1840f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1840f-117">-DefaultProfile</span></span>
<span data-ttu-id="1840f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1840f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1840f-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1840f-119">-Force</span></span>
<span data-ttu-id="1840f-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1840f-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1840f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1840f-121">-InputObject</span></span>
<span data-ttu-id="1840f-122">Udostępniony obiekt wejściowy zasobu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="1840f-122">Shared private link resource input object</span></span>

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

### <span data-ttu-id="1840f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1840f-123">-Name</span></span>
<span data-ttu-id="1840f-124">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="1840f-124">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="1840f-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="1840f-125">-ParentObject</span></span>
<span data-ttu-id="1840f-126">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1840f-126">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="1840f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1840f-127">-PassThru</span></span>
<span data-ttu-id="1840f-128">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="1840f-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1840f-129">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="1840f-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1840f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1840f-130">-ResourceGroupName</span></span>
<span data-ttu-id="1840f-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1840f-131">Resource Group name.</span></span>

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

### <span data-ttu-id="1840f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1840f-132">-ResourceId</span></span>
<span data-ttu-id="1840f-133">Udostępniony identyfikator zasobu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="1840f-133">Shared private link resource id</span></span>

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

### <span data-ttu-id="1840f-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1840f-134">-ServiceName</span></span>
<span data-ttu-id="1840f-135">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1840f-135">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="1840f-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1840f-136">-Confirm</span></span>
<span data-ttu-id="1840f-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1840f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1840f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1840f-138">-WhatIf</span></span>
<span data-ttu-id="1840f-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1840f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1840f-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1840f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1840f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1840f-141">CommonParameters</span></span>
<span data-ttu-id="1840f-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1840f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1840f-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1840f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1840f-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1840f-144">INPUTS</span></span>

### <span data-ttu-id="1840f-145">Brak</span><span class="sxs-lookup"><span data-stu-id="1840f-145">None</span></span>

## <span data-ttu-id="1840f-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1840f-146">OUTPUTS</span></span>

### <span data-ttu-id="1840f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1840f-147">System.Boolean</span></span>

## <span data-ttu-id="1840f-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1840f-148">NOTES</span></span>

## <span data-ttu-id="1840f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1840f-149">RELATED LINKS</span></span>

[<span data-ttu-id="1840f-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="1840f-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="1840f-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="1840f-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="1840f-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="1840f-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)