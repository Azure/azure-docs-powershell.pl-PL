---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219915"
---
# <span data-ttu-id="61874-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61874-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="61874-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61874-102">SYNOPSIS</span></span>
<span data-ttu-id="61874-103">Usuwa przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="61874-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="61874-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61874-104">SYNTAX</span></span>

### <span data-ttu-id="61874-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61874-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61874-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61874-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61874-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61874-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61874-108">Opis</span><span class="sxs-lookup"><span data-stu-id="61874-108">DESCRIPTION</span></span>
<span data-ttu-id="61874-109">Polecenie cmdlet **Remove-AzPolicyAssignment** usuwa określone przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="61874-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="61874-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61874-110">EXAMPLES</span></span>

### <span data-ttu-id="61874-111">Przykład 1. Usuń przypisanie zasad według nazw i zakresów</span><span class="sxs-lookup"><span data-stu-id="61874-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="61874-112">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="61874-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="61874-113">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="61874-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="61874-114">Drugie polecenie usuwa przypisanie zasad o nazwie PolicyAssignment07, które zostało przydzielone na poziomie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61874-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="61874-115">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="61874-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="61874-116">Przykład 2: usuwanie przydziału zasad według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="61874-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="61874-117">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="61874-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="61874-118">Drugie polecenie uzyskuje przypisanie zasad na poziomie grupy zasobów, a następnie zapisuje je w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="61874-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="61874-119">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="61874-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="61874-120">Polecenie ostatnie Usuwa przypisanie zasad, które identyfikuje właściwość **ResourceId** $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="61874-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="61874-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61874-121">PARAMETERS</span></span>

### <span data-ttu-id="61874-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="61874-122">-ApiVersion</span></span>
<span data-ttu-id="61874-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="61874-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="61874-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="61874-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="61874-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61874-125">-DefaultProfile</span></span>
<span data-ttu-id="61874-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="61874-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61874-127">-ID</span><span class="sxs-lookup"><span data-stu-id="61874-127">-Id</span></span>
<span data-ttu-id="61874-128">Określa w pełni kwalifikowany identyfikator zasobu dla zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61874-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61874-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="61874-129">-InputObject</span></span>
<span data-ttu-id="61874-130">Obiekt przydziału zasad, który ma zostać usunięty, był wyprowadzany z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61874-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="61874-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61874-131">-Name</span></span>
<span data-ttu-id="61874-132">Określa nazwę przypisania zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61874-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61874-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="61874-133">-Pre</span></span>
<span data-ttu-id="61874-134">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="61874-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="61874-135">-Zakres</span><span class="sxs-lookup"><span data-stu-id="61874-135">-Scope</span></span>
<span data-ttu-id="61874-136">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="61874-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="61874-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61874-137">-Confirm</span></span>
<span data-ttu-id="61874-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61874-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61874-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61874-139">-WhatIf</span></span>
<span data-ttu-id="61874-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61874-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61874-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61874-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61874-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61874-142">CommonParameters</span></span>
<span data-ttu-id="61874-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61874-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61874-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61874-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61874-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61874-145">INPUTS</span></span>

### <span data-ttu-id="61874-146">System. String</span><span class="sxs-lookup"><span data-stu-id="61874-146">System.String</span></span>

## <span data-ttu-id="61874-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61874-147">OUTPUTS</span></span>

### <span data-ttu-id="61874-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61874-148">System.Boolean</span></span>

## <span data-ttu-id="61874-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61874-149">NOTES</span></span>

## <span data-ttu-id="61874-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61874-150">RELATED LINKS</span></span>

[<span data-ttu-id="61874-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61874-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="61874-152">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61874-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="61874-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61874-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


