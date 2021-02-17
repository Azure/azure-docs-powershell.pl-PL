---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186659"
---
# <span data-ttu-id="f02bd-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f02bd-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="f02bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f02bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f02bd-103">Tworzy i uruchamia działania naprawcze dotyczące zasad dla przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="f02bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f02bd-104">SYNTAX</span></span>

### <span data-ttu-id="f02bd-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="f02bd-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f02bd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f02bd-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f02bd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f02bd-107">DESCRIPTION</span></span>
<span data-ttu-id="f02bd-108">Polecenie **cmdlet Start-AzPolicyRemediation** tworzy działania naprawcze dotyczące zasad dla określonego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="f02bd-109">Działania naprawcze zostaną rozwiązane we wszystkich niezgodnych zasobach w zakresie rozwiązywania problemów lub poniżej tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="f02bd-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="f02bd-110">Działania naprawcze są obsługiwane tylko w przypadku zasad z efektem "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="f02bd-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="f02bd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f02bd-111">EXAMPLES</span></span>

### <span data-ttu-id="f02bd-112">Przykład 1. Rozpoczynanie rozwiązywania problemów w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f02bd-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="f02bd-113">To polecenie tworzy nowe działania naprawcze zasad w ramach subskrypcji "Moja subskrypcja" dla danego przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="f02bd-114">Przykład 2. Rozpoczynanie działań naprawczych w zakresie grupy zarządzania przy użyciu filtrów opcjonalnych</span><span class="sxs-lookup"><span data-stu-id="f02bd-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="f02bd-115">To polecenie tworzy nowe działania naprawcze zasad w grupie zarządzania "mg1" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="f02bd-116">Działania naprawcze zostaną rozwiązane tylko w przypadku zasobów w regionach "zachód" i "wschódus".</span><span class="sxs-lookup"><span data-stu-id="f02bd-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="f02bd-117">Przykład 3. Rozpoczynanie rozwiązywania problemów w zakresie grupy zasobów dla przydziału definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="f02bd-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="f02bd-118">To polecenie tworzy nowe działania naprawcze zasad w grupie zasobów "myRG" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="f02bd-119">Przydział zasad przypisuje definicję zestawu zasad (znaną również jako inicjatywa).</span><span class="sxs-lookup"><span data-stu-id="f02bd-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="f02bd-120">Identyfikator odwołania do definicji zasad wskazuje, które zasady w ramach inicjatywy należy rozwiązać.</span><span class="sxs-lookup"><span data-stu-id="f02bd-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="f02bd-121">Przykład 4. Rozpoczynanie działania naprawczego i oczekiwanie na jego ukończenie w tle</span><span class="sxs-lookup"><span data-stu-id="f02bd-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="f02bd-122">To polecenie uruchamia nowe działania naprawcze zasad w subskrypcji "Moja subskrypcja" dla danego przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="f02bd-123">Będzie ona czekać na ukończenie działania naprawczego przed zwróceniem ostatecznego stanu rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="f02bd-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="f02bd-124">Przykład 5. Rozpoczęcie działań naprawczych w celu odnajdowania niezgodnych zasobów przed podjęciem działań naprawczych</span><span class="sxs-lookup"><span data-stu-id="f02bd-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="f02bd-125">To polecenie tworzy nowe działania naprawcze zasad w ramach subskrypcji "Moja subskrypcja" dla danego przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="f02bd-126">Stan zgodności zasobów w subskrypcji zostanie ponownie oceniony pod względem przydziału zasad, a niezgodne zasoby zostaną rozwiązane.</span><span class="sxs-lookup"><span data-stu-id="f02bd-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="f02bd-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f02bd-127">PARAMETERS</span></span>

### <span data-ttu-id="f02bd-128">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f02bd-128">-AsJob</span></span>
<span data-ttu-id="f02bd-129">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="f02bd-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f02bd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02bd-130">-DefaultProfile</span></span>
<span data-ttu-id="f02bd-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f02bd-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f02bd-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="f02bd-132">-LocationFilter</span></span>
<span data-ttu-id="f02bd-133">Lokalizacje zasobów, które powinny zostać uwzględnione w działaniach naprawczych.</span><span class="sxs-lookup"><span data-stu-id="f02bd-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="f02bd-134">Zasoby, które nie znajdują się w tych lokalizacjach, nie zostaną rozwiązane.</span><span class="sxs-lookup"><span data-stu-id="f02bd-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f02bd-135">-ManagementGroupName</span></span>
<span data-ttu-id="f02bd-136">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="f02bd-136">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f02bd-137">-Name</span></span>
<span data-ttu-id="f02bd-138">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f02bd-138">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="f02bd-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="f02bd-140">Identyfikator przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-140">Policy assignment ID.</span></span>
<span data-ttu-id="f02bd-141">Np.</span><span class="sxs-lookup"><span data-stu-id="f02bd-141">E.g.</span></span>
<span data-ttu-id="f02bd-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="f02bd-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="f02bd-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="f02bd-144">Pobiera identyfikator odwołania do definicji zasad dla poszczególnych definicji, które są naprawiane.</span><span class="sxs-lookup"><span data-stu-id="f02bd-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="f02bd-145">Wymagane, gdy przydział zasad przypisuje definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f02bd-145">Required when the policy assignment assigns a policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="f02bd-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="f02bd-147">W tym artykule opisano, w jaki sposób zadanie rozwiązywania problemów znajdzie zasoby, których działania naprawcze należy rozwiązać.</span><span class="sxs-lookup"><span data-stu-id="f02bd-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="f02bd-148">ReEvaluateCompliance nie jest obsługiwana podczas rozwiązywania problemów z zakresami grup zarządzania.</span><span class="sxs-lookup"><span data-stu-id="f02bd-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f02bd-149">-ResourceGroupName</span></span>
<span data-ttu-id="f02bd-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f02bd-150">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f02bd-151">-ResourceId</span></span>
<span data-ttu-id="f02bd-152">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f02bd-152">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-153">— Zakres</span><span class="sxs-lookup"><span data-stu-id="f02bd-153">-Scope</span></span>
<span data-ttu-id="f02bd-154">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="f02bd-154">Scope of the resource.</span></span>
<span data-ttu-id="f02bd-155">Np.</span><span class="sxs-lookup"><span data-stu-id="f02bd-155">E.g.</span></span>
<span data-ttu-id="f02bd-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="f02bd-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02bd-157">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f02bd-157">-Confirm</span></span>
<span data-ttu-id="f02bd-158">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f02bd-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f02bd-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f02bd-159">-WhatIf</span></span>
<span data-ttu-id="f02bd-160">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f02bd-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f02bd-161">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f02bd-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f02bd-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02bd-162">CommonParameters</span></span>
<span data-ttu-id="f02bd-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02bd-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02bd-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f02bd-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02bd-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f02bd-165">INPUTS</span></span>

### <span data-ttu-id="f02bd-166">System.String</span><span class="sxs-lookup"><span data-stu-id="f02bd-166">System.String</span></span>

### <span data-ttu-id="f02bd-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f02bd-167">System.String[]</span></span>

## <span data-ttu-id="f02bd-168">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f02bd-168">OUTPUTS</span></span>

### <span data-ttu-id="f02bd-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="f02bd-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="f02bd-170">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f02bd-170">NOTES</span></span>

## <span data-ttu-id="f02bd-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f02bd-171">RELATED LINKS</span></span>
