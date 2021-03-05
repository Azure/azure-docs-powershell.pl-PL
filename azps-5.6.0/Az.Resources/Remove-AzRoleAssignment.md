---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: d941e5cc3bf4a3f2363aa8369a7f5b0518ba2e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005802"
---
# <span data-ttu-id="a9504-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9504-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="a9504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9504-102">SYNOPSIS</span></span>
<span data-ttu-id="a9504-103">Usuwa przypisanie roli do określonego podmiotu zabezpieczeń, który jest przypisany do określonej roli w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="a9504-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="a9504-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9504-104">SYNTAX</span></span>

### <span data-ttu-id="a9504-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a9504-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9504-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9504-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9504-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9504-117">DESCRIPTION</span></span>
<span data-ttu-id="a9504-118">Użyj Remove-AzRoleAssignment commandlet, aby odwołać dostęp do dowolnego podmiotu głównego w danym zakresie i przy danej roli.</span><span class="sxs-lookup"><span data-stu-id="a9504-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="a9504-119">Obiekt przydziału, czyli musi zostać określony główny podmiot.</span><span class="sxs-lookup"><span data-stu-id="a9504-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="a9504-120">Podmiot zabezpieczeń może być użytkownikiem (za pomocą parametrów SignInName lub ObjectId identyfikuje użytkownika), grupą zabezpieczeń (identyfikując grupę za pomocą parametru ObjectId) lub podmiotem zabezpieczeń usługi (w celu zidentyfikowania parametru ServicePrincipal należy użyć parametrów ServicePrincipalName lub ObjectId).</span><span class="sxs-lookup"><span data-stu-id="a9504-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="a9504-121">Rola przypisana do podmiotu zabezpieczeń MUSI zostać określona za pomocą parametru RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="a9504-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="a9504-122">Zakres przydziału MOŻE zostać określony, a jeśli nie zostanie określony, domyślnie zostanie określony zakres subskrypcji, czyli spróbuje usunąć przypisanie do określonego dyrektora i roli w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a9504-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="a9504-123">Zakres przydziału można określić przy użyciu jednego z poniższych parametrów.</span><span class="sxs-lookup"><span data-stu-id="a9504-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="a9504-124">a.</span><span class="sxs-lookup"><span data-stu-id="a9504-124">a.</span></span>
<span data-ttu-id="a9504-125">Zakres — jest to w pełni kwalifikowany zakres zaczynający się od \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="a9504-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="a9504-126">ResourceGroupName — nazwa dowolnej grupy zasobów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a9504-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="a9504-127">c.</span><span class="sxs-lookup"><span data-stu-id="a9504-127">c.</span></span>
<span data-ttu-id="a9504-128">ResourceName, ResourceType, ResourceGroupName i (opcjonalnie) ParentResource — identyfikuje określony zasób w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a9504-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="a9504-129">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9504-129">EXAMPLES</span></span>

### <span data-ttu-id="a9504-130">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9504-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="a9504-131">Usuwa przypisanie roli do osoby, która jest przypisana do roli Czytelnika w john.doe@contoso.com zakresie grupy zasobów rg1.</span><span class="sxs-lookup"><span data-stu-id="a9504-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="a9504-132">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a9504-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="a9504-133">Usuwa przypisanie roli do podmiotu zabezpieczeń grupy wskazanego przez identyfikator ObjectId i przypisanego do roli czytnika.</span><span class="sxs-lookup"><span data-stu-id="a9504-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="a9504-134">Domyślnie używa bieżącej subskrypcji jako zakresu w celu znalezienia zadania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a9504-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="a9504-135">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a9504-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="a9504-136">Usuwa pierwszy obiekt przydziału roli, który jest pobierany z Get-AzRoleAssignment wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="a9504-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="a9504-137">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9504-137">PARAMETERS</span></span>

### <span data-ttu-id="a9504-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9504-138">-DefaultProfile</span></span>
<span data-ttu-id="a9504-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a9504-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9504-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9504-140">-InputObject</span></span>
<span data-ttu-id="a9504-141">Obiekt Przypisywanie ról.</span><span class="sxs-lookup"><span data-stu-id="a9504-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a9504-142">-ObjectId</span></span>
<span data-ttu-id="a9504-143">Identyfikator ObjectId usługi Azure AD użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a9504-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="a9504-144">-ParentResource</span></span>
<span data-ttu-id="a9504-145">Zasób nadrzędny w hierarchii(zasobu określonego za pomocą parametru ResourceName), jeśli został określony.</span><span class="sxs-lookup"><span data-stu-id="a9504-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="a9504-146">Należy go używać w połączeniu z parametrami ResourceGroupName, ResourceType i ResourceName, aby skonstruować zakres hierarchiczny w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="a9504-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9504-147">-PassThru</span></span>
<span data-ttu-id="a9504-148">Jeśli jest to określone, wyświetla usunięte przypisanie roli.</span><span class="sxs-lookup"><span data-stu-id="a9504-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="a9504-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9504-149">-ResourceGroupName</span></span>
<span data-ttu-id="a9504-150">Nazwa grupy zasobów, do których przypisano rolę.</span><span class="sxs-lookup"><span data-stu-id="a9504-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="a9504-151">Próbuje usunąć przydział w określonym zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9504-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="a9504-152">W połączeniu z parametrami ResourceName, ResourceType i (opcjonalnie)ParentResource polecenie konstruuje zakres hierarchiczny w postaci względnego identyfikatoru URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="a9504-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a9504-153">-ResourceName</span></span>
<span data-ttu-id="a9504-154">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a9504-154">The resource name.</span></span>
<span data-ttu-id="a9504-155">Np. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="a9504-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="a9504-156">Należy używać w połączeniu z parametrami ResourceGroupName, ResourceType i (opcjonalnie)ParentResource, aby skonstruować zakres hierarchiczny w postaci względnego URI identyfikującego zasób i usunąć przydział w tym zakresie.</span><span class="sxs-lookup"><span data-stu-id="a9504-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a9504-157">-ResourceType</span></span>
<span data-ttu-id="a9504-158">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="a9504-158">The resource type.</span></span>
<span data-ttu-id="a9504-159">Na przykład Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="a9504-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="a9504-160">Należy go używać w połączeniu z parametrami ResourceGroupName, ResourceName i (opcjonalnie)ParentResource, aby skonstruować zakres hierarchiczny w postaci względnego URI identyfikującego zasób i usuwania przydziału w tym zakresie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9504-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a9504-161">-RoleDefinitionId</span></span>
<span data-ttu-id="a9504-162">Identyfikator roli RBAC, dla której należy usunąć przypisanie.</span><span class="sxs-lookup"><span data-stu-id="a9504-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a9504-163">-RoleDefinitionName</span></span>
<span data-ttu-id="a9504-164">Nazwa roli RBAC, dla której należy usunąć przypisanie, na przykład: Czytelnik, Współautor, Administrator sieci wirtualnej itp.</span><span class="sxs-lookup"><span data-stu-id="a9504-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-165">— Zakres</span><span class="sxs-lookup"><span data-stu-id="a9504-165">-Scope</span></span>
<span data-ttu-id="a9504-166">Zakres przydziału ról do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a9504-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="a9504-167">W formacie względnego URI.</span><span class="sxs-lookup"><span data-stu-id="a9504-167">In the format of relative URI.</span></span>
<span data-ttu-id="a9504-168">Na przykład:"/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="a9504-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="a9504-169">Jeśli nie zostanie określona, spróbuje usunąć rolę na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a9504-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="a9504-170">Jeśli jest określona, powinna zaczynać się od "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="a9504-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a9504-171">-ServicePrincipalName</span></span>
<span data-ttu-id="a9504-172">Nazwa ServicePrincipalName aplikacji usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="a9504-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="a9504-173">-SignInName</span></span>
<span data-ttu-id="a9504-174">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9504-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9504-175">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9504-175">-Confirm</span></span>
<span data-ttu-id="a9504-176">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9504-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9504-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9504-177">-WhatIf</span></span>
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

### <span data-ttu-id="a9504-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9504-178">CommonParameters</span></span>
<span data-ttu-id="a9504-179">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9504-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9504-180">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9504-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9504-181">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9504-181">INPUTS</span></span>

### <span data-ttu-id="a9504-182">System.String</span><span class="sxs-lookup"><span data-stu-id="a9504-182">System.String</span></span>

### <span data-ttu-id="a9504-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a9504-183">System.Guid</span></span>

### <span data-ttu-id="a9504-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9504-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="a9504-185">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9504-185">OUTPUTS</span></span>

### <span data-ttu-id="a9504-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9504-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="a9504-187">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9504-187">NOTES</span></span>
<span data-ttu-id="a9504-188">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="a9504-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a9504-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9504-189">RELATED LINKS</span></span>

[<span data-ttu-id="a9504-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9504-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="a9504-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9504-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="a9504-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9504-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

