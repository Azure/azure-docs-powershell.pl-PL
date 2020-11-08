---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223677"
---
# <span data-ttu-id="e16b5-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="e16b5-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="e16b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e16b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e16b5-103">Umożliwia utworzenie i rozpoczęcie korygowania zasad dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="e16b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e16b5-104">SYNTAX</span></span>

### <span data-ttu-id="e16b5-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e16b5-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e16b5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e16b5-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e16b5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e16b5-107">DESCRIPTION</span></span>
<span data-ttu-id="e16b5-108">Polecenie cmdlet **Start-AzPolicyRemediation** tworzy korygowanie zasad dla określonego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="e16b5-109">Wszystkie niezgodne zasoby na poziomie lub poniżej zakresu korygowania zostaną skorygowane.</span><span class="sxs-lookup"><span data-stu-id="e16b5-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="e16b5-110">Korygowanie jest obsługiwane tylko w przypadku zasad z efektem "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="e16b5-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="e16b5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e16b5-111">EXAMPLES</span></span>

### <span data-ttu-id="e16b5-112">Przykład 1. Rozpocznij korygowanie w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e16b5-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="e16b5-113">To polecenie tworzy nowe korygowanie zasad w subskrypcji "Moja subskrypcja" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="e16b5-114">Przykład 2: Rozpoczynanie korygowania w zakresie grupy zarządzania za pomocą filtrów opcjonalnych</span><span class="sxs-lookup"><span data-stu-id="e16b5-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="e16b5-115">To polecenie tworzy nowe korygowanie zasad w grupie zarządzania "MG1" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="e16b5-116">Korygowane będą tylko zasoby w lokalizacjach "Zachodnia" lub "Wschód".</span><span class="sxs-lookup"><span data-stu-id="e16b5-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="e16b5-117">Przykład 3: Rozpoczynanie korygowania w zakresie grupy zasobów dla zadania definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="e16b5-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="e16b5-118">To polecenie tworzy nowe korygowanie zasad w grupie zasobów "myRG" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="e16b5-119">Przypisanie zasady powoduje przypisanie definicji zestawu zasad (zwanej też inicjatywą).</span><span class="sxs-lookup"><span data-stu-id="e16b5-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="e16b5-120">Identyfikator odwołania do definicji zasad wskazuje, którą zasadę należy skorygować w ramach inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="e16b5-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="e16b5-121">Przykład 4: Rozpoczynanie korygowania i oczekiwanie na ukończenie działania w tle</span><span class="sxs-lookup"><span data-stu-id="e16b5-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="e16b5-122">To polecenie rozpoczyna nowe korygowanie zasad w subskrypcji "Moja subskrypcja" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="e16b5-123">Przed zwróceniem ostatecznego stanu korygowania będzie czekał na ukończenie korygowania.</span><span class="sxs-lookup"><span data-stu-id="e16b5-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="e16b5-124">Przykład 5: Rozpoczynanie korygowania, które odnajdzie niezgodne zasoby przed remediating</span><span class="sxs-lookup"><span data-stu-id="e16b5-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="e16b5-125">To polecenie tworzy nowe korygowanie zasad w subskrypcji "Moja subskrypcja" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="e16b5-126">Stan zgodności zasobów w subskrypcji zostanie ponownie oceniony na podstawie przydziału zasad, a niezgodne zasoby zostaną skorygowane.</span><span class="sxs-lookup"><span data-stu-id="e16b5-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="e16b5-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e16b5-127">PARAMETERS</span></span>

### <span data-ttu-id="e16b5-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e16b5-128">-AsJob</span></span>
<span data-ttu-id="e16b5-129">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="e16b5-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e16b5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16b5-130">-DefaultProfile</span></span>
<span data-ttu-id="e16b5-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e16b5-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e16b5-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="e16b5-132">-LocationFilter</span></span>
<span data-ttu-id="e16b5-133">Lokalizacje zasobów, które powinny zostać uwzględnione w korygowaniu.</span><span class="sxs-lookup"><span data-stu-id="e16b5-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="e16b5-134">Zasoby, które nie znajdują się w tych lokalizacjach, nie będą korygowane.</span><span class="sxs-lookup"><span data-stu-id="e16b5-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="e16b5-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e16b5-135">-ManagementGroupName</span></span>
<span data-ttu-id="e16b5-136">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e16b5-136">Management group ID.</span></span>

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

### <span data-ttu-id="e16b5-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e16b5-137">-Name</span></span>
<span data-ttu-id="e16b5-138">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e16b5-138">Resource name.</span></span>

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

### <span data-ttu-id="e16b5-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="e16b5-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="e16b5-140">Identyfikator przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-140">Policy assignment ID.</span></span>
<span data-ttu-id="e16b5-141">Przykład.</span><span class="sxs-lookup"><span data-stu-id="e16b5-141">E.g.</span></span>
<span data-ttu-id="e16b5-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="e16b5-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="e16b5-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="e16b5-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="e16b5-144">Pobiera identyfikator odwołania do definicji zasad dla indywidualnej definicji, która jest korygowana.</span><span class="sxs-lookup"><span data-stu-id="e16b5-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="e16b5-145">Wymagany, gdy przypisanie zasad powoduje przypisanie definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="e16b5-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="e16b5-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="e16b5-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="e16b5-147">W tym artykule opisano, jak zadanie korygowania odnajdzie zasoby, które należy skorygować.</span><span class="sxs-lookup"><span data-stu-id="e16b5-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="e16b5-148">ReEvaluateCompliance nie jest obsługiwany w przypadku remediating zakresów grup zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e16b5-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="e16b5-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16b5-149">-ResourceGroupName</span></span>
<span data-ttu-id="e16b5-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e16b5-150">Resource group name.</span></span>

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

### <span data-ttu-id="e16b5-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e16b5-151">-ResourceId</span></span>
<span data-ttu-id="e16b5-152">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e16b5-152">Resource ID.</span></span>

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

### <span data-ttu-id="e16b5-153">-Zakres</span><span class="sxs-lookup"><span data-stu-id="e16b5-153">-Scope</span></span>
<span data-ttu-id="e16b5-154">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="e16b5-154">Scope of the resource.</span></span>
<span data-ttu-id="e16b5-155">Przykład.</span><span class="sxs-lookup"><span data-stu-id="e16b5-155">E.g.</span></span>
<span data-ttu-id="e16b5-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="e16b5-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="e16b5-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e16b5-157">-Confirm</span></span>
<span data-ttu-id="e16b5-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e16b5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16b5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16b5-159">-WhatIf</span></span>
<span data-ttu-id="e16b5-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e16b5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16b5-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e16b5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16b5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16b5-162">CommonParameters</span></span>
<span data-ttu-id="e16b5-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e16b5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16b5-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e16b5-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16b5-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e16b5-165">INPUTS</span></span>

### <span data-ttu-id="e16b5-166">System. String</span><span class="sxs-lookup"><span data-stu-id="e16b5-166">System.String</span></span>

### <span data-ttu-id="e16b5-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="e16b5-167">System.String[]</span></span>

## <span data-ttu-id="e16b5-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e16b5-168">OUTPUTS</span></span>

### <span data-ttu-id="e16b5-169">Microsoft. Azure. Commands. PolicyInsights. MODELES. remediacja. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="e16b5-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="e16b5-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e16b5-170">NOTES</span></span>

## <span data-ttu-id="e16b5-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e16b5-171">RELATED LINKS</span></span>
