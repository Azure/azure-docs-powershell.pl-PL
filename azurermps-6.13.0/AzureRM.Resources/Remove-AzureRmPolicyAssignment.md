---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 63b88096200c5db55f9c40a4ba839ffbf25c681d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544827"
---
# <span data-ttu-id="8cf54-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8cf54-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="8cf54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cf54-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf54-103">Usuwa przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="8cf54-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cf54-104">SYNTAX</span></span>

### <span data-ttu-id="8cf54-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cf54-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf54-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf54-106">IdParameterSet</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf54-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8cf54-107">DESCRIPTION</span></span>
<span data-ttu-id="8cf54-108">Polecenie cmdlet **Remove-AzureRmPolicyAssignment** usuwa określone przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="8cf54-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="8cf54-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cf54-109">EXAMPLES</span></span>

### <span data-ttu-id="8cf54-110">Przykład 1. Usuń przypisanie zasad według nazw i zakresów</span><span class="sxs-lookup"><span data-stu-id="8cf54-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="8cf54-111">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8cf54-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="8cf54-112">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8cf54-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8cf54-113">Drugie polecenie usuwa przypisanie zasad o nazwie PolicyAssignment07, które zostało przydzielone na poziomie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8cf54-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="8cf54-114">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="8cf54-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="8cf54-115">Przykład 2: usuwanie przydziału zasad według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="8cf54-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="8cf54-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8cf54-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8cf54-117">Drugie polecenie uzyskuje przypisanie zasad na poziomie grupy zasobów, a następnie zapisuje je w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8cf54-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8cf54-118">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="8cf54-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="8cf54-119">Polecenie ostatnie Usuwa przypisanie zasad, które identyfikuje właściwość **ResourceId** $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8cf54-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="8cf54-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cf54-120">PARAMETERS</span></span>

### <span data-ttu-id="8cf54-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8cf54-121">-ApiVersion</span></span>
<span data-ttu-id="8cf54-122">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="8cf54-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8cf54-123">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="8cf54-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8cf54-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf54-124">-DefaultProfile</span></span>
<span data-ttu-id="8cf54-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8cf54-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-126">-ID</span><span class="sxs-lookup"><span data-stu-id="8cf54-126">-Id</span></span>
<span data-ttu-id="8cf54-127">Określa w pełni kwalifikowany identyfikator zasobu dla zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf54-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8cf54-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8cf54-128">-InformationAction</span></span>
<span data-ttu-id="8cf54-129">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="8cf54-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8cf54-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8cf54-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cf54-131">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="8cf54-131">Continue</span></span>
- <span data-ttu-id="8cf54-132">Ignorować</span><span class="sxs-lookup"><span data-stu-id="8cf54-132">Ignore</span></span>
- <span data-ttu-id="8cf54-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="8cf54-133">Inquire</span></span>
- <span data-ttu-id="8cf54-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8cf54-134">SilentlyContinue</span></span>
- <span data-ttu-id="8cf54-135">Przestaw</span><span class="sxs-lookup"><span data-stu-id="8cf54-135">Stop</span></span>
- <span data-ttu-id="8cf54-136">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="8cf54-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8cf54-137">-InformationVariable</span></span>
<span data-ttu-id="8cf54-138">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="8cf54-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8cf54-139">-Name</span></span>
<span data-ttu-id="8cf54-140">Określa nazwę przypisania zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf54-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8cf54-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8cf54-141">-Pre</span></span>
<span data-ttu-id="8cf54-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="8cf54-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8cf54-143">-Zakres</span><span class="sxs-lookup"><span data-stu-id="8cf54-143">-Scope</span></span>
<span data-ttu-id="8cf54-144">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="8cf54-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="8cf54-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8cf54-145">-Confirm</span></span>
<span data-ttu-id="8cf54-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf54-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf54-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf54-147">-WhatIf</span></span>
<span data-ttu-id="8cf54-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf54-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf54-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8cf54-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf54-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf54-150">CommonParameters</span></span>
<span data-ttu-id="8cf54-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf54-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf54-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf54-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf54-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cf54-153">INPUTS</span></span>

## <span data-ttu-id="8cf54-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cf54-154">OUTPUTS</span></span>

## <span data-ttu-id="8cf54-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cf54-155">NOTES</span></span>

## <span data-ttu-id="8cf54-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cf54-156">RELATED LINKS</span></span>

[<span data-ttu-id="8cf54-157">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8cf54-157">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8cf54-158">Nowe — AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8cf54-158">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8cf54-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8cf54-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


