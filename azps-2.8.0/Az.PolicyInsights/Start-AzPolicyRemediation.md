---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: df7b0803952a7a972d2c68ef2d8e7ec61d42c5e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872311"
---
# <span data-ttu-id="81e40-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="81e40-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="81e40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81e40-102">SYNOPSIS</span></span>
<span data-ttu-id="81e40-103">Umożliwia utworzenie i rozpoczęcie korygowania zasad dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="81e40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81e40-104">SYNTAX</span></span>

### <span data-ttu-id="81e40-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="81e40-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81e40-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81e40-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e40-107">Opis</span><span class="sxs-lookup"><span data-stu-id="81e40-107">DESCRIPTION</span></span>
<span data-ttu-id="81e40-108">Polecenie cmdlet **Start-AzPolicyRemediation** tworzy korygowanie zasad dla określonego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="81e40-109">Wszystkie niezgodne zasoby na poziomie lub poniżej zakresu korygowania zostaną skorygowane.</span><span class="sxs-lookup"><span data-stu-id="81e40-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="81e40-110">Korygowanie jest obsługiwane tylko w przypadku zasad z efektem "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="81e40-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="81e40-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81e40-111">EXAMPLES</span></span>

### <span data-ttu-id="81e40-112">Przykład 1. Rozpocznij korygowanie w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="81e40-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="81e40-113">To polecenie tworzy nowe korygowanie zasad w subskrypcji "Moja subskrypcja" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="81e40-114">Przykład 2: Rozpoczynanie korygowania w zakresie grupy zarządzania za pomocą filtrów opcjonalnych</span><span class="sxs-lookup"><span data-stu-id="81e40-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="81e40-115">To polecenie tworzy nowe korygowanie zasad w grupie zarządzania "MG1" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="81e40-116">Korygowane będą tylko zasoby w lokalizacjach "Zachodnia" lub "Wschód".</span><span class="sxs-lookup"><span data-stu-id="81e40-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="81e40-117">Przykład 3: Rozpoczynanie korygowania w zakresie grupy zasobów dla zadania definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="81e40-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="81e40-118">To polecenie tworzy nowe korygowanie zasad w grupie zasobów "myRG" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="81e40-119">Przypisanie zasady powoduje przypisanie definicji zestawu zasad (zwanej też inicjatywą).</span><span class="sxs-lookup"><span data-stu-id="81e40-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="81e40-120">Identyfikator odwołania do definicji zasad wskazuje, którą zasadę należy skorygować w ramach inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="81e40-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="81e40-121">Przykład 4: Rozpoczynanie korygowania i oczekiwanie na ukończenie działania w tle</span><span class="sxs-lookup"><span data-stu-id="81e40-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="81e40-122">To polecenie rozpoczyna nowe korygowanie zasad w subskrypcji "Moja subskrypcja" dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="81e40-123">Przed zwróceniem ostatecznego stanu korygowania będzie czekał na ukończenie korygowania.</span><span class="sxs-lookup"><span data-stu-id="81e40-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="81e40-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81e40-124">PARAMETERS</span></span>

### <span data-ttu-id="81e40-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81e40-125">-AsJob</span></span>
<span data-ttu-id="81e40-126">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="81e40-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="81e40-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e40-127">-DefaultProfile</span></span>
<span data-ttu-id="81e40-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81e40-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81e40-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="81e40-129">-LocationFilter</span></span>
<span data-ttu-id="81e40-130">Lokalizacje zasobów, które powinny zostać uwzględnione w korygowaniu.</span><span class="sxs-lookup"><span data-stu-id="81e40-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="81e40-131">Zasoby, które nie znajdują się w tych lokalizacjach, nie będą korygowane.</span><span class="sxs-lookup"><span data-stu-id="81e40-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="81e40-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="81e40-132">-ManagementGroupName</span></span>
<span data-ttu-id="81e40-133">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="81e40-133">Management group ID.</span></span>

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

### <span data-ttu-id="81e40-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81e40-134">-Name</span></span>
<span data-ttu-id="81e40-135">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="81e40-135">Resource name.</span></span>

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

### <span data-ttu-id="81e40-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="81e40-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="81e40-137">Identyfikator przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-137">Policy assignment ID.</span></span>
<span data-ttu-id="81e40-138">Przykład.</span><span class="sxs-lookup"><span data-stu-id="81e40-138">E.g.</span></span>
<span data-ttu-id="81e40-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="81e40-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="81e40-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="81e40-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="81e40-141">Pobiera identyfikator odwołania do definicji zasad dla indywidualnej definicji, która jest korygowana.</span><span class="sxs-lookup"><span data-stu-id="81e40-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="81e40-142">Wymagany, gdy przypisanie zasad powoduje przypisanie definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="81e40-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="81e40-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e40-143">-ResourceGroupName</span></span>
<span data-ttu-id="81e40-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81e40-144">Resource group name.</span></span>

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

### <span data-ttu-id="81e40-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e40-145">-ResourceId</span></span>
<span data-ttu-id="81e40-146">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="81e40-146">Resource ID.</span></span>

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

### <span data-ttu-id="81e40-147">-Zakres</span><span class="sxs-lookup"><span data-stu-id="81e40-147">-Scope</span></span>
<span data-ttu-id="81e40-148">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="81e40-148">Scope of the resource.</span></span>
<span data-ttu-id="81e40-149">Przykład.</span><span class="sxs-lookup"><span data-stu-id="81e40-149">E.g.</span></span>
<span data-ttu-id="81e40-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="81e40-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="81e40-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81e40-151">-Confirm</span></span>
<span data-ttu-id="81e40-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e40-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e40-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e40-153">-WhatIf</span></span>
<span data-ttu-id="81e40-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e40-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e40-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81e40-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e40-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e40-156">CommonParameters</span></span>
<span data-ttu-id="81e40-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e40-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e40-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e40-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e40-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81e40-159">INPUTS</span></span>

### <span data-ttu-id="81e40-160">System. String</span><span class="sxs-lookup"><span data-stu-id="81e40-160">System.String</span></span>

### <span data-ttu-id="81e40-161">System. String []</span><span class="sxs-lookup"><span data-stu-id="81e40-161">System.String[]</span></span>

## <span data-ttu-id="81e40-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81e40-162">OUTPUTS</span></span>

### <span data-ttu-id="81e40-163">Microsoft. Azure. Commands. PolicyInsights. MODELES. remediacja. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="81e40-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="81e40-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81e40-164">NOTES</span></span>

## <span data-ttu-id="81e40-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81e40-165">RELATED LINKS</span></span>
