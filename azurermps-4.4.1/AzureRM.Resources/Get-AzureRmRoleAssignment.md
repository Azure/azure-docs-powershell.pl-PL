---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: 5cbf4f46d102188ff1db3becf66d3edffe426fae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549900"
---
# <span data-ttu-id="7a0b1-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7a0b1-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="7a0b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0b1-103">Wyświetla listę przypisań ról usługi Azure RBAC w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="7a0b1-104">Domyślnie lista wszystkich przypisań ról w wybranej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="7a0b1-105">Użyj odpowiednich parametrów, aby wyświetlić listę przydziałów dla określonego użytkownika lub wyświetlić zadania dotyczące określonej grupy zasobów lub zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a0b1-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a0b1-106">SYNTAX</span></span>

### <span data-ttu-id="7a0b1-107">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a0b1-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a0b1-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0b1-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a0b1-124">Opis</span><span class="sxs-lookup"><span data-stu-id="7a0b1-124">DESCRIPTION</span></span>
<span data-ttu-id="7a0b1-125">Użyj polecenia Get-AzureRMRoleAssignment, aby wyświetlić wszystkie przydziały ról, które obowiązują w zakresie.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>

<span data-ttu-id="7a0b1-126">Bez żadnych parametrów to polecenie zwraca wszystkie zadania ról wprowadzone w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="7a0b1-127">Ta lista może być filtrowana przy użyciu parametrów filtrowania podmiotu zabezpieczeń, roli i zakresu.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>

<span data-ttu-id="7a0b1-128">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="7a0b1-129">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="7a0b1-130">Aby określić grupę zabezpieczeń, użyj parametru ObjectId usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="7a0b1-131">Aby określić aplikację Azure AD, użyj parametrów ServicePrincipalName lub ObjectId.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="7a0b1-132">Rola, która jest przypisywana, musi być określona przy użyciu parametru RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="7a0b1-133">Zakres, w którym jest udzielany dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="7a0b1-134">Domyślna wybrana subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="7a0b1-135">Zakres przydziału można określić przy użyciu jednej z następujących kombinacji parametrów a.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="7a0b1-136">Zakres — to jest w pełni kwalifikowany zakres rozpoczynający się od/subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="7a0b1-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="7a0b1-137">Spowoduje to filtrowanie przydziałów, które są efektywne dla określonego zakresu, czyli wszystkich przydziałów w tym zakresie.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="7a0b1-138">b.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-138">b.</span></span>
<span data-ttu-id="7a0b1-139">ResourceGroupName — nazwa dowolnej grupy zasobów w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="7a0b1-140">Spowoduje to filtrowanie przydziałów, które obowiązują w określonej grupie zasobów c.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="7a0b1-141">ResourceName, ResourceType, ResourceGroupName oraz (opcjonalnie) ParentResource-identyfikuje konkretny zasób w ramach abonamentu i będzie filtrować zadania działające w tym zakresie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>

<span data-ttu-id="7a0b1-142">Aby określić, jaki dostęp dany użytkownik ma w subskrypcji, użyj przełącznika ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="7a0b1-143">Spowoduje to wyświetlenie listy wszystkich ról przypisanych do użytkownika oraz do grup, do których należy dany użytkownik.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>

<span data-ttu-id="7a0b1-144">Użyj przełącznika IncludeClassicAdministrators, aby wyświetlić także administratorów abonamentów i współadministratora.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="7a0b1-145">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a0b1-145">EXAMPLES</span></span>

### <span data-ttu-id="7a0b1-146">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a0b1-146">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="7a0b1-147">Lista wszystkich przydziałów ról w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7a0b1-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="7a0b1-148">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a0b1-148">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com -ExpandPrincipalGroups
```

<span data-ttu-id="7a0b1-149">Pobiera wszystkie zadania ról wprowadzone do użytkownika john.doe@contoso.com , a także grupy, których jest członkiem, w zakresie testRG lub powyżej.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="7a0b1-150">--------------------------Przykład 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a0b1-150">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="7a0b1-151">Pobiera wszystkie zadania ról określonego podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="7a0b1-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="7a0b1-152">--------------------------Przykład 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a0b1-152">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="7a0b1-153">Pobiera przypisania ról w zakresie witryny internetowej "site1".</span><span class="sxs-lookup"><span data-stu-id="7a0b1-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="7a0b1-154">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a0b1-154">PARAMETERS</span></span>

### <span data-ttu-id="7a0b1-155">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="7a0b1-155">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="7a0b1-156">Jeśli ta funkcja jest określona, zwraca role bezpośrednio przypisane do użytkownika i grupy, których członkiem jest użytkownik (przechodnie).</span><span class="sxs-lookup"><span data-stu-id="7a0b1-156">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="7a0b1-157">Obsługiwane tylko dla głównego podmiotu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-157">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="7a0b1-158">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="7a0b1-158">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="7a0b1-159">Jeśli to pole jest określone, wyświetla również zadania ról z klasycznymi administratorami subskrypcji (współadministratora, Administratorzy usług itd.).</span><span class="sxs-lookup"><span data-stu-id="7a0b1-159">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="7a0b1-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7a0b1-160">-ObjectId</span></span>
<span data-ttu-id="7a0b1-161">Identyfikator ObjectId usługi Azure AD dla użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-161">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="7a0b1-162">Umożliwia filtrowanie wszystkich przydziałów, które zostały wprowadzone do określonego podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-162">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0b1-163">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="7a0b1-163">-ParentResource</span></span>
<span data-ttu-id="7a0b1-164">Zasób nadrzędny w hierarchii zasobu określony przy użyciu parametru ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-164">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="7a0b1-165">Należy użyć w połączeniu z parametrami ResourceGroupName, ResourceType i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-165">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="7a0b1-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0b1-166">-ResourceGroupName</span></span>
<span data-ttu-id="7a0b1-167">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-167">The resource group name.</span></span>
<span data-ttu-id="7a0b1-168">Wyświetla listę przydziałów ról, które obowiązują w odróżnieniu od określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-168">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="7a0b1-169">W przypadku użycia w połączeniu z parametrami resourceName, ResourceType i ParentResource polecenie wyświetla listę przydziałów efektywnych dla zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-169">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="7a0b1-170">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7a0b1-170">-ResourceName</span></span>
<span data-ttu-id="7a0b1-171">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-171">The resource name.</span></span>
<span data-ttu-id="7a0b1-172">Na przykład storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-172">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="7a0b1-173">Musi być używana w połączeniu z ResourceGroupName, ResourceType i (opcjonalnie) ParentResource parametrami.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-173">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="7a0b1-174">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7a0b1-174">-ResourceType</span></span>
<span data-ttu-id="7a0b1-175">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-175">The resource type.</span></span>
<span data-ttu-id="7a0b1-176">Na przykład Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-176">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="7a0b1-177">Należy użyć w połączeniu z ResourceGroupName, resourceName i (opcjonalnie) ParentResource parametrami.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-177">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="7a0b1-178">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7a0b1-178">-RoleDefinitionId</span></span>
<span data-ttu-id="7a0b1-179">Identyfikator roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-179">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="7a0b1-180">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7a0b1-180">-RoleDefinitionName</span></span>
<span data-ttu-id="7a0b1-181">Rola przypisana do podmiotu zabezpieczeń, czyli czytelnika, współpracownika, administratora sieci wirtualnej itd.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-181">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="7a0b1-182">-Zakres</span><span class="sxs-lookup"><span data-stu-id="7a0b1-182">-Scope</span></span>
<span data-ttu-id="7a0b1-183">Zakres przypisania roli.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-183">The Scope of the role assignment.</span></span>
<span data-ttu-id="7a0b1-184">W formacie względnego identyfikatora URI.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-184">In the format of relative URI.</span></span>
<span data-ttu-id="7a0b1-185">Na przykład/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-185">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="7a0b1-186">Musi zaczynać się od "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="7a0b1-186">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="7a0b1-187">Polecenie umożliwia filtrowanie wszystkich przydziałów, które są efektywne w tym zakresie.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-187">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="7a0b1-188">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7a0b1-188">-ServicePrincipalName</span></span>
<span data-ttu-id="7a0b1-189">Obiekt ServicePrincipalName głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-189">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="7a0b1-190">Filtruje wszystkie przydziały wprowadzone w określonej aplikacji usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-190">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="7a0b1-191">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7a0b1-191">-SignInName</span></span>
<span data-ttu-id="7a0b1-192">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-192">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="7a0b1-193">Umożliwia filtrowanie wszystkich przydziałów wprowadzonych do określonego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-193">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="7a0b1-194">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0b1-194">-DefaultProfile</span></span>
<span data-ttu-id="7a0b1-195">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-195">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a0b1-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0b1-196">CommonParameters</span></span>
<span data-ttu-id="7a0b1-197">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0b1-198">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0b1-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0b1-199">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a0b1-199">INPUTS</span></span>

## <span data-ttu-id="7a0b1-200">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a0b1-200">OUTPUTS</span></span>

### <span data-ttu-id="7a0b1-201">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. zasoby. MODELES autoryzacji. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="7a0b1-201">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="7a0b1-202">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a0b1-202">NOTES</span></span>
<span data-ttu-id="7a0b1-203">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="7a0b1-203">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7a0b1-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a0b1-204">RELATED LINKS</span></span>

[<span data-ttu-id="7a0b1-205">Nowe — AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7a0b1-205">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="7a0b1-206">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7a0b1-206">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="7a0b1-207">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7a0b1-207">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
