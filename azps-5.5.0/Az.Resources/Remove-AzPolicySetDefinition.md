---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201835"
---
# <span data-ttu-id="ea442-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ea442-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="ea442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea442-102">SYNOPSIS</span></span>
<span data-ttu-id="ea442-103">Usuwa definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ea442-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="ea442-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea442-104">SYNTAX</span></span>

### <span data-ttu-id="ea442-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea442-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea442-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea442-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea442-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea442-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea442-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea442-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea442-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea442-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea442-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea442-110">DESCRIPTION</span></span>
<span data-ttu-id="ea442-111">Polecenie **cmdlet Remove-AzPolicySetDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="ea442-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="ea442-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea442-112">EXAMPLES</span></span>

### <span data-ttu-id="ea442-113">Przykład 1. Usuwanie definicji zestawu zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="ea442-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="ea442-114">Pierwsze polecenie otrzymuje definicję zestawu zasad za pomocą Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea442-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ea442-115">Polecenie przechowuje je w $PolicySetDefinition zmienną.</span><span class="sxs-lookup"><span data-stu-id="ea442-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="ea442-116">Drugie polecenie usuwa definicję zestawu zasad identyfikowaną przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ea442-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="ea442-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea442-117">PARAMETERS</span></span>

### <span data-ttu-id="ea442-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ea442-118">-ApiVersion</span></span>
<span data-ttu-id="ea442-119">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="ea442-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ea442-120">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="ea442-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ea442-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea442-121">-DefaultProfile</span></span>
<span data-ttu-id="ea442-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ea442-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea442-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ea442-123">-Force</span></span>
<span data-ttu-id="ea442-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea442-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ea442-125">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="ea442-125">-Id</span></span>
<span data-ttu-id="ea442-126">W pełni kwalifikowany identyfikator definicji zestawu zasad, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="ea442-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="ea442-127">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ea442-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="ea442-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea442-128">-InputObject</span></span>
<span data-ttu-id="ea442-129">Zasady ustawiają obiekt definicji w celu usunięcia danych wyjściowych z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea442-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea442-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ea442-130">-ManagementGroupName</span></span>
<span data-ttu-id="ea442-131">Nazwa grupy zarządzania definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ea442-131">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea442-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ea442-132">-Name</span></span>
<span data-ttu-id="ea442-133">Nazwa definicji ustawiona przez zasady.</span><span class="sxs-lookup"><span data-stu-id="ea442-133">The policy set definition name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea442-134">— Przed</span><span class="sxs-lookup"><span data-stu-id="ea442-134">-Pre</span></span>
<span data-ttu-id="ea442-135">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ea442-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ea442-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea442-136">-SubscriptionId</span></span>
<span data-ttu-id="ea442-137">Identyfikator subskrypcji definicji zestawu zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ea442-137">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea442-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea442-138">-Confirm</span></span>
<span data-ttu-id="ea442-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea442-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea442-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea442-140">-WhatIf</span></span>
<span data-ttu-id="ea442-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea442-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea442-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ea442-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea442-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea442-143">CommonParameters</span></span>
<span data-ttu-id="ea442-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea442-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea442-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea442-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea442-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea442-146">INPUTS</span></span>

### <span data-ttu-id="ea442-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ea442-147">System.String</span></span>

### <span data-ttu-id="ea442-148">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ea442-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ea442-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea442-149">OUTPUTS</span></span>

### <span data-ttu-id="ea442-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea442-150">System.Boolean</span></span>

## <span data-ttu-id="ea442-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea442-151">NOTES</span></span>

## <span data-ttu-id="ea442-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea442-152">RELATED LINKS</span></span>
