---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242578"
---
# <span data-ttu-id="a5668-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a5668-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="a5668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5668-102">SYNOPSIS</span></span>
<span data-ttu-id="a5668-103">Lista przypisań ról RBAC platformy Azure w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="a5668-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="a5668-104">Domyślnie lista zawiera wszystkie przypisania ról w wybranej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5668-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="a5668-105">Użyj odpowiednich parametrów, aby wyświetlić listę przydziałów dla określonego użytkownika lub listę przydziałów dla określonej grupy zasobów lub zasobu.</span><span class="sxs-lookup"><span data-stu-id="a5668-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="a5668-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a5668-106">SYNTAX</span></span>

### <span data-ttu-id="a5668-107">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a5668-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5668-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5668-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5668-124">OPIS</span><span class="sxs-lookup"><span data-stu-id="a5668-124">DESCRIPTION</span></span>
<span data-ttu-id="a5668-125">Użyj tego Get-AzRoleAssignment, aby wyświetlić listę wszystkich przydziałów ról, które mają zastosowanie w zakresie.</span><span class="sxs-lookup"><span data-stu-id="a5668-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="a5668-126">Bez żadnych parametrów to polecenie zwraca wszystkie przypisania ról w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a5668-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="a5668-127">Tę listę można filtrować przy użyciu parametrów filtrowania dla podmiotu głównego, roli i zakresu.</span><span class="sxs-lookup"><span data-stu-id="a5668-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="a5668-128">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="a5668-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="a5668-129">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="a5668-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="a5668-130">Aby określić grupę zabezpieczeń, użyj parametru ObjectId usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a5668-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="a5668-131">Aby określić aplikację usługi Azure AD, użyj parametrów ServicePrincipalName lub ObjectId.</span><span class="sxs-lookup"><span data-stu-id="a5668-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="a5668-132">Przypisaną rolę należy określić przy użyciu parametru RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="a5668-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="a5668-133">Zakres, w którym udzielany jest dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="a5668-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="a5668-134">Domyślnie wybrana subskrypcja jest zaznaczona.</span><span class="sxs-lookup"><span data-stu-id="a5668-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="a5668-135">Zakres przydziału można określić przy użyciu jednej z następujących kombinacji parametrów a.</span><span class="sxs-lookup"><span data-stu-id="a5668-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="a5668-136">Zakres — jest to w pełni kwalifikowany zakres zaczynający się od /subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="a5668-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="a5668-137">Spowoduje to filtrowanie przydziałów, które są efektywne w tym konkretnym zakresie, czyli wszystkich przydziałów w tym zakresie lub powyżej.</span><span class="sxs-lookup"><span data-stu-id="a5668-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="a5668-138">b.</span><span class="sxs-lookup"><span data-stu-id="a5668-138">b.</span></span>
<span data-ttu-id="a5668-139">ResourceGroupName — nazwa dowolnej grupy zasobów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a5668-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="a5668-140">Spowoduje to filtrowanie przydziałów obowiązuje w określonej grupie zasobów c.</span><span class="sxs-lookup"><span data-stu-id="a5668-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="a5668-141">ResourceName, ResourceType, ResourceGroupName i (opcjonalnie) ParentResource — identyfikuje określony zasób w ramach subskrypcji i filtruje przydziały efektywne w tym zakresie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5668-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="a5668-142">Aby określić, jaki dostęp ma dany użytkownik w subskrypcji, użyj przełącznika ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="a5668-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="a5668-143">Spowoduje to listę wszystkich ról przypisanych do użytkownika i grup, do których należy użytkownik.</span><span class="sxs-lookup"><span data-stu-id="a5668-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="a5668-144">Użyj przełącznika IncludeClassicAdministrators, aby wyświetlić również administratorów subskrypcji i współadministratorów.</span><span class="sxs-lookup"><span data-stu-id="a5668-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="a5668-145">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a5668-145">EXAMPLES</span></span>

### <span data-ttu-id="a5668-146">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5668-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="a5668-147">Lista wszystkich przypisań ról w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a5668-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="a5668-148">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a5668-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="a5668-149">Pobiera wszystkie przypisania ról użytkownika i grupy, których jest członkiem, w john.doe@contoso.com zakresie testRG lub powyżej.</span><span class="sxs-lookup"><span data-stu-id="a5668-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="a5668-150">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a5668-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="a5668-151">Pobiera wszystkie przypisania ról określonego podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a5668-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="a5668-152">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a5668-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="a5668-153">Pobiera przypisania ról w zakresie witryny internetowej "witryna1".</span><span class="sxs-lookup"><span data-stu-id="a5668-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="a5668-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5668-154">PARAMETERS</span></span>

### <span data-ttu-id="a5668-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5668-155">-DefaultProfile</span></span>
<span data-ttu-id="a5668-156">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a5668-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5668-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="a5668-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="a5668-158">Jeśli jest to określone, zwraca role bezpośrednio przypisane do użytkownika i do grup, których członkiem jest użytkownik (przechodnie).</span><span class="sxs-lookup"><span data-stu-id="a5668-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="a5668-159">Obsługiwane tylko przez głównego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a5668-159">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="a5668-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="a5668-161">Jeśli jest to określone, są również wymienione przypisania ról administratorów klasycznych subskrypcji (współadministracyjnym, administratorów usług itp.).</span><span class="sxs-lookup"><span data-stu-id="a5668-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a5668-162">-ObjectId</span></span>
<span data-ttu-id="a5668-163">Identyfikator ObjectId usługi Azure AD użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a5668-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="a5668-164">Filtruje wszystkie przydziały dokonywane dla określonego podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="a5668-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="a5668-165">-ParentResource</span></span>
<span data-ttu-id="a5668-166">Zasób nadrzędny w hierarchii zasobu określonego za pomocą parametru ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a5668-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="a5668-167">Musi być używany w połączeniu z parametrami ResourceGroupName, ResourceType i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a5668-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5668-168">-ResourceGroupName</span></span>
<span data-ttu-id="a5668-169">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5668-169">The resource group name.</span></span>
<span data-ttu-id="a5668-170">Zawiera listę przydziałów ról, które są skuteczne w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5668-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="a5668-171">W połączeniu z parametrami ResourceName (NazwaZasób), ResourceType (Typ Zasobów) i ParentResource (ŹródłoZasób) polecenie zawiera listę przydziałów stosowanych w zasobach w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5668-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a5668-172">-ResourceName</span></span>
<span data-ttu-id="a5668-173">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a5668-173">The resource name.</span></span>
<span data-ttu-id="a5668-174">Np. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="a5668-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="a5668-175">Musi być używany w połączeniu z parametrami ResourceGroupName, ResourceType i (opcjonalnie)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="a5668-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a5668-176">-ResourceType</span></span>
<span data-ttu-id="a5668-177">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="a5668-177">The resource type.</span></span>
<span data-ttu-id="a5668-178">Na przykład Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="a5668-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="a5668-179">Musi być używany w połączeniu z parametrami ResourceGroupName, ResourceName i (opcjonalnie)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="a5668-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a5668-180">-RoleDefinitionId</span></span>
<span data-ttu-id="a5668-181">Identyfikator roli przypisanej do podmiotu głównego.</span><span class="sxs-lookup"><span data-stu-id="a5668-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="a5668-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a5668-182">-RoleDefinitionName</span></span>
<span data-ttu-id="a5668-183">Rola przypisana dyrektorowi, czyli Czytelnik, Współautor, Administrator sieci wirtualnej itp.</span><span class="sxs-lookup"><span data-stu-id="a5668-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-184">— Zakres</span><span class="sxs-lookup"><span data-stu-id="a5668-184">-Scope</span></span>
<span data-ttu-id="a5668-185">Zakres przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="a5668-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="a5668-186">W formacie względnego URI.</span><span class="sxs-lookup"><span data-stu-id="a5668-186">In the format of relative URI.</span></span>
<span data-ttu-id="a5668-187">Na przykład /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="a5668-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="a5668-188">Musi zaczynać się od "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="a5668-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="a5668-189">Polecenie filtruje wszystkie przydziały, które są efektywne w tym zakresie.</span><span class="sxs-lookup"><span data-stu-id="a5668-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5668-190">-ServicePrincipalName</span></span>
<span data-ttu-id="a5668-191">ServicePrincipalName podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a5668-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="a5668-192">Umożliwia filtrowanie wszystkich zadań wykonanych w określonej aplikacji usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a5668-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="a5668-193">-SignInName</span></span>
<span data-ttu-id="a5668-194">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a5668-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="a5668-195">Filtruje wszystkie przypisania dokonywane dla określonego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a5668-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5668-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5668-196">CommonParameters</span></span>
<span data-ttu-id="a5668-197">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5668-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5668-198">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5668-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5668-199">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5668-199">INPUTS</span></span>

### <span data-ttu-id="a5668-200">System.String</span><span class="sxs-lookup"><span data-stu-id="a5668-200">System.String</span></span>

### <span data-ttu-id="a5668-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a5668-201">System.Guid</span></span>

## <span data-ttu-id="a5668-202">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5668-202">OUTPUTS</span></span>

### <span data-ttu-id="a5668-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a5668-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="a5668-204">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a5668-204">NOTES</span></span>
<span data-ttu-id="a5668-205">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="a5668-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a5668-206">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5668-206">RELATED LINKS</span></span>

[<span data-ttu-id="a5668-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a5668-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="a5668-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a5668-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="a5668-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a5668-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

