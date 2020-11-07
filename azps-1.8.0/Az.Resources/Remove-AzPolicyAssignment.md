---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 18ca6ad068c5478bdb7177a8f53742f90d555dee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708305"
---
# <span data-ttu-id="b55f0-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b55f0-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="b55f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b55f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b55f0-103">Usuwa przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="b55f0-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="b55f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b55f0-104">SYNTAX</span></span>

### <span data-ttu-id="b55f0-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b55f0-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b55f0-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b55f0-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b55f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b55f0-107">DESCRIPTION</span></span>
<span data-ttu-id="b55f0-108">Polecenie cmdlet **Remove-AzPolicyAssignment** usuwa określone przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="b55f0-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="b55f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b55f0-109">EXAMPLES</span></span>

### <span data-ttu-id="b55f0-110">Przykład 1. Usuń przypisanie zasad według nazw i zakresów</span><span class="sxs-lookup"><span data-stu-id="b55f0-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="b55f0-111">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b55f0-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b55f0-112">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b55f0-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b55f0-113">Drugie polecenie usuwa przypisanie zasad o nazwie PolicyAssignment07, które zostało przydzielone na poziomie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b55f0-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="b55f0-114">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="b55f0-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="b55f0-115">Przykład 2: usuwanie przydziału zasad według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="b55f0-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="b55f0-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b55f0-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b55f0-117">Drugie polecenie uzyskuje przypisanie zasad na poziomie grupy zasobów, a następnie zapisuje je w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b55f0-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b55f0-118">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="b55f0-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="b55f0-119">Polecenie ostatnie Usuwa przypisanie zasad, które identyfikuje właściwość **ResourceId** $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b55f0-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="b55f0-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b55f0-120">PARAMETERS</span></span>

### <span data-ttu-id="b55f0-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b55f0-121">-ApiVersion</span></span>
<span data-ttu-id="b55f0-122">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="b55f0-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b55f0-123">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="b55f0-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b55f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55f0-124">-DefaultProfile</span></span>
<span data-ttu-id="b55f0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b55f0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b55f0-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b55f0-126">-Id</span></span>
<span data-ttu-id="b55f0-127">Określa w pełni kwalifikowany identyfikator zasobu dla zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f0-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b55f0-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b55f0-128">-Name</span></span>
<span data-ttu-id="b55f0-129">Określa nazwę przypisania zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f0-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b55f0-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="b55f0-130">-Pre</span></span>
<span data-ttu-id="b55f0-131">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="b55f0-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b55f0-132">-Zakres</span><span class="sxs-lookup"><span data-stu-id="b55f0-132">-Scope</span></span>
<span data-ttu-id="b55f0-133">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="b55f0-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="b55f0-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b55f0-134">-Confirm</span></span>
<span data-ttu-id="b55f0-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b55f0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b55f0-136">-WhatIf</span></span>
<span data-ttu-id="b55f0-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b55f0-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b55f0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b55f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55f0-139">CommonParameters</span></span>
<span data-ttu-id="b55f0-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b55f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55f0-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b55f0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55f0-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b55f0-142">INPUTS</span></span>

### <span data-ttu-id="b55f0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b55f0-143">System.String</span></span>

## <span data-ttu-id="b55f0-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b55f0-144">OUTPUTS</span></span>

### <span data-ttu-id="b55f0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b55f0-145">System.Boolean</span></span>

## <span data-ttu-id="b55f0-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b55f0-146">NOTES</span></span>

## <span data-ttu-id="b55f0-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b55f0-147">RELATED LINKS</span></span>

[<span data-ttu-id="b55f0-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b55f0-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="b55f0-149">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b55f0-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="b55f0-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b55f0-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)

