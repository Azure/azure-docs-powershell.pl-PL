---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
ms.openlocfilehash: adf6147db102ee834f7e12e19409a95734fae7e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899183"
---
# <span data-ttu-id="a51e9-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a51e9-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="a51e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a51e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a51e9-103">Usuwa przypisanie roli do określonego podmiotu zabezpieczeń, który jest przypisany do określonej roli w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="a51e9-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a51e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a51e9-104">SYNTAX</span></span>

### <span data-ttu-id="a51e9-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a51e9-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a51e9-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51e9-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="a51e9-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a51e9-117">Opis</span><span class="sxs-lookup"><span data-stu-id="a51e9-117">DESCRIPTION</span></span>
<span data-ttu-id="a51e9-118">Użyj Remove-AzureRmRoleAssignment unifiedgroup, aby odebrać dostęp każdemu podmiotowi zabezpieczeń w danym zakresie i danej roli.</span><span class="sxs-lookup"><span data-stu-id="a51e9-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="a51e9-119">NALEŻY określić obiekt główny zadania.</span><span class="sxs-lookup"><span data-stu-id="a51e9-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="a51e9-120">Głównym użytkownikiem może być użytkownik (SignInName lub identyfikator obiektu ObjectId), Grupa zabezpieczeń (parametr ObjectId służy do identyfikowania grupy) lub podmiot zabezpieczeń (Użyj parametrów ServicePrincipalName lub ObjectId w celu zidentyfikowania elementu serviceprincipal.</span><span class="sxs-lookup"><span data-stu-id="a51e9-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="a51e9-121">Rola, do której jest przypisany podmiot zabezpieczeń, musi być określona przy użyciu parametru RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="a51e9-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="a51e9-122">Zakres przypisania może zostać określony, a jeśli nie jest określony, domyślnie jest używany zakres abonamentu, czyli próba usunięcia zadania określonego podmiotu zabezpieczeń i roli w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a51e9-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="a51e9-123">Zakres zadania można określić przy użyciu jednego z następujących parametrów.</span><span class="sxs-lookup"><span data-stu-id="a51e9-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="a51e9-124">sieci.</span><span class="sxs-lookup"><span data-stu-id="a51e9-124">a.</span></span>
<span data-ttu-id="a51e9-125">Zakres — to jest w pełni kwalifikowany zakres rozpoczynający się od/subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="a51e9-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="a51e9-126">ResourceGroupName — nazwa dowolnej grupy zasobów w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a51e9-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="a51e9-127">s.</span><span class="sxs-lookup"><span data-stu-id="a51e9-127">c.</span></span>
<span data-ttu-id="a51e9-128">ResourceName, ResourceType, ResourceGroupName oraz (opcjonalnie) ParentResource-identyfikuje konkretny zasób w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a51e9-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="a51e9-129">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a51e9-129">EXAMPLES</span></span>

### <span data-ttu-id="a51e9-130">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a51e9-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="a51e9-131">Usuwa przypisanie roli, john.doe@contoso.com które jest przypisane do roli czytelnika w zakresie zasobów RG1.</span><span class="sxs-lookup"><span data-stu-id="a51e9-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="a51e9-132">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a51e9-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="a51e9-133">Usuwa przypisanie roli do podmiotu zabezpieczeń grupy określonego przez identyfikator obiektu ObjectId i przypisany do roli czytelnik.</span><span class="sxs-lookup"><span data-stu-id="a51e9-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="a51e9-134">Domyślnie jest używana bieżąca subskrypcja jako zakres do odnalezienia zadania, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="a51e9-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="a51e9-135">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a51e9-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="a51e9-136">Usuwa pierwszy obiekt przydziału roli, który jest pobierany z Get-AzureRmRoleAssignment unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="a51e9-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="a51e9-137">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a51e9-137">PARAMETERS</span></span>

### <span data-ttu-id="a51e9-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51e9-138">-DefaultProfile</span></span>
<span data-ttu-id="a51e9-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a51e9-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a51e9-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a51e9-140">-InputObject</span></span>
<span data-ttu-id="a51e9-141">Obiekt przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="a51e9-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="a51e9-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a51e9-142">-ObjectId</span></span>
<span data-ttu-id="a51e9-143">Identyfikator ObjectId usługi Azure AD dla użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a51e9-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a51e9-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="a51e9-144">-ParentResource</span></span>
<span data-ttu-id="a51e9-145">Zasób nadrzędny w hierarchii (zasobu określonego przy użyciu parametru ResourceName), jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="a51e9-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="a51e9-146">Do konstruowania zakresu hierarchicznego w formie względnego identyfikatora URI identyfikującego zasób należy użyć w połączeniu z parametrami ResourceGroupName, ResourceType i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a51e9-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="a51e9-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a51e9-147">-PassThru</span></span>
<span data-ttu-id="a51e9-148">Jeśli jest określona, wyświetla usunięte przypisanie roli</span><span class="sxs-lookup"><span data-stu-id="a51e9-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="a51e9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a51e9-149">-ResourceGroupName</span></span>
<span data-ttu-id="a51e9-150">Nazwa grupy zasobów, do której rola jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="a51e9-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="a51e9-151">Próba usunięcia zadania w określonym zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a51e9-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="a51e9-152">Gdy jest używana w połączeniu z parametrami resourceName, ResourceType i (opcjonalnie) ParentResource parametry, polecenie konstruuje zakres hierarchiczny w formie względnego identyfikatora URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="a51e9-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="a51e9-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a51e9-153">-ResourceName</span></span>
<span data-ttu-id="a51e9-154">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a51e9-154">The resource name.</span></span>
<span data-ttu-id="a51e9-155">Na przykład storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="a51e9-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="a51e9-156">Do konstruowania hierarchicznego zakresu w formie względnego identyfikatora URI identyfikującego zasób i usuwania zadania w tym zakresie musi być używane w połączeniu z ResourceGroupName, ResourceType i (opcjonalnie) ParentResource parametrami.</span><span class="sxs-lookup"><span data-stu-id="a51e9-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="a51e9-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a51e9-157">-ResourceType</span></span>
<span data-ttu-id="a51e9-158">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="a51e9-158">The resource type.</span></span>
<span data-ttu-id="a51e9-159">Na przykład Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="a51e9-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="a51e9-160">Należy użyć w połączeniu z parametrami ResourceGroupName, resourceName i (opcjonalnie) ParentResource parametry w celu skonstruowania zakresu hierarchicznego w formie względnego identyfikatora URI identyfikującego zasób i usuwania przydziału w tym zakresie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a51e9-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="a51e9-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a51e9-161">-RoleDefinitionId</span></span>
<span data-ttu-id="a51e9-162">Identyfikator roli RBAC, dla której należy usunąć przydział.</span><span class="sxs-lookup"><span data-stu-id="a51e9-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="a51e9-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a51e9-163">-RoleDefinitionName</span></span>
<span data-ttu-id="a51e9-164">Nazwa roli RBAC, dla której należy usunąć przypisanie, tzn. czytelnik, współautor, administrator sieci wirtualnej itd.</span><span class="sxs-lookup"><span data-stu-id="a51e9-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="a51e9-165">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a51e9-165">-Scope</span></span>
<span data-ttu-id="a51e9-166">Zakres przypisania roli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a51e9-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="a51e9-167">W formacie względnego identyfikatora URI.</span><span class="sxs-lookup"><span data-stu-id="a51e9-167">In the format of relative URI.</span></span>
<span data-ttu-id="a51e9-168">Na przykład "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="a51e9-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="a51e9-169">Jeśli nie zostanie określona, zostanie podjęta próba usunięcia roli na poziomie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a51e9-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="a51e9-170">Jeśli jest określona, powinna rozpoczynać się od "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="a51e9-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="a51e9-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a51e9-171">-ServicePrincipalName</span></span>
<span data-ttu-id="a51e9-172">Obiekt ServicePrincipalName aplikacji Azure AD</span><span class="sxs-lookup"><span data-stu-id="a51e9-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="a51e9-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="a51e9-173">-SignInName</span></span>
<span data-ttu-id="a51e9-174">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a51e9-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="a51e9-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a51e9-175">-Confirm</span></span>
<span data-ttu-id="a51e9-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a51e9-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a51e9-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a51e9-177">-WhatIf</span></span>
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

### <span data-ttu-id="a51e9-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51e9-178">CommonParameters</span></span>
<span data-ttu-id="a51e9-179">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a51e9-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51e9-180">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a51e9-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51e9-181">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a51e9-181">INPUTS</span></span>

### <span data-ttu-id="a51e9-182">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a51e9-182">System.Guid</span></span>

### <span data-ttu-id="a51e9-183">System. String</span><span class="sxs-lookup"><span data-stu-id="a51e9-183">System.String</span></span>

### <span data-ttu-id="a51e9-184">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a51e9-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>
<span data-ttu-id="a51e9-185">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a51e9-185">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a51e9-186">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a51e9-186">OUTPUTS</span></span>

### <span data-ttu-id="a51e9-187">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a51e9-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="a51e9-188">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a51e9-188">NOTES</span></span>
<span data-ttu-id="a51e9-189">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="a51e9-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a51e9-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a51e9-190">RELATED LINKS</span></span>

[<span data-ttu-id="a51e9-191">Nowe — AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a51e9-191">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="a51e9-192">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a51e9-192">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="a51e9-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a51e9-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

