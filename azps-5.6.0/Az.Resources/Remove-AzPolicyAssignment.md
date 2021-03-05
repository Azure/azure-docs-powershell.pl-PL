---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 83c6cc2ba8103b95aed6d6d365c700e656ac16a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005809"
---
# <span data-ttu-id="c59eb-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c59eb-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="c59eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c59eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c59eb-103">Usuwa przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="c59eb-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="c59eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c59eb-104">SYNTAX</span></span>

### <span data-ttu-id="c59eb-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c59eb-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59eb-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c59eb-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59eb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c59eb-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c59eb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c59eb-108">DESCRIPTION</span></span>
<span data-ttu-id="c59eb-109">Polecenie **cmdlet Remove-AzPolicyAssignment** usuwa przypisanie określonych zasad.</span><span class="sxs-lookup"><span data-stu-id="c59eb-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="c59eb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c59eb-110">EXAMPLES</span></span>

### <span data-ttu-id="c59eb-111">Przykład 1. Usuwanie przypisania zasad według nazwy i zakresu</span><span class="sxs-lookup"><span data-stu-id="c59eb-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="c59eb-112">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59eb-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c59eb-113">Polecenie przechowuje ten obiekt w $ResourceGroup zmienną.</span><span class="sxs-lookup"><span data-stu-id="c59eb-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c59eb-114">Drugie polecenie usuwa przypisanie zasad o nazwie PolicyAssignment07, które zostało przypisane na poziomie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c59eb-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="c59eb-115">Właściwość **ResourceId** właściwości $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c59eb-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c59eb-116">Przykład 2. Usuwanie przypisania zasad według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="c59eb-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="c59eb-117">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11, a następnie przechowuje ten obiekt w $ResourceGroup zmienną.</span><span class="sxs-lookup"><span data-stu-id="c59eb-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c59eb-118">Drugie polecenie pobiera przydział zasad na poziomie grupy zasobów, a następnie przechowuje je w $PolicyAssignment zmienną.</span><span class="sxs-lookup"><span data-stu-id="c59eb-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="c59eb-119">Właściwość **ResourceId** właściwości $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c59eb-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="c59eb-120">Ostatnie polecenie usuwa przypisanie zasad, które określa $PolicyAssignment **ResourceId.**</span><span class="sxs-lookup"><span data-stu-id="c59eb-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="c59eb-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c59eb-121">PARAMETERS</span></span>

### <span data-ttu-id="c59eb-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c59eb-122">-ApiVersion</span></span>
<span data-ttu-id="c59eb-123">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="c59eb-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c59eb-124">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="c59eb-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59eb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59eb-125">-DefaultProfile</span></span>
<span data-ttu-id="c59eb-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c59eb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c59eb-127">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="c59eb-127">-Id</span></span>
<span data-ttu-id="c59eb-128">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59eb-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59eb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c59eb-129">-InputObject</span></span>
<span data-ttu-id="c59eb-130">Obiekt przypisywania zasad do usunięcia, który był wyprowadzony z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59eb-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c59eb-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c59eb-131">-Name</span></span>
<span data-ttu-id="c59eb-132">Określa nazwę przydziału zasad, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59eb-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59eb-133">— Przed</span><span class="sxs-lookup"><span data-stu-id="c59eb-133">-Pre</span></span>
<span data-ttu-id="c59eb-134">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="c59eb-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c59eb-135">— Zakres</span><span class="sxs-lookup"><span data-stu-id="c59eb-135">-Scope</span></span>
<span data-ttu-id="c59eb-136">Określa zakres stosowania zasad.</span><span class="sxs-lookup"><span data-stu-id="c59eb-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59eb-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c59eb-137">-Confirm</span></span>
<span data-ttu-id="c59eb-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c59eb-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59eb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59eb-139">-WhatIf</span></span>
<span data-ttu-id="c59eb-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59eb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59eb-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c59eb-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59eb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59eb-142">CommonParameters</span></span>
<span data-ttu-id="c59eb-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59eb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59eb-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c59eb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59eb-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c59eb-145">INPUTS</span></span>

### <span data-ttu-id="c59eb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c59eb-146">System.String</span></span>

## <span data-ttu-id="c59eb-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c59eb-147">OUTPUTS</span></span>

### <span data-ttu-id="c59eb-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c59eb-148">System.Boolean</span></span>

## <span data-ttu-id="c59eb-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c59eb-149">NOTES</span></span>

## <span data-ttu-id="c59eb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c59eb-150">RELATED LINKS</span></span>

[<span data-ttu-id="c59eb-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c59eb-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c59eb-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c59eb-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="c59eb-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c59eb-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


