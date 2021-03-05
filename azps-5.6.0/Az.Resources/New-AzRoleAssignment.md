---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: b21d265d507c1ff508c5db68094a65b54257931a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973521"
---
# <span data-ttu-id="66d75-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66d75-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="66d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d75-102">SYNOPSIS</span></span>
<span data-ttu-id="66d75-103">Przypisuje określoną rolę RBAC do określonego podmiotu zabezpieczeń w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="66d75-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="66d75-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66d75-104">SYNTAX</span></span>

### <span data-ttu-id="66d75-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="66d75-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d75-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d75-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66d75-116">OPIS</span><span class="sxs-lookup"><span data-stu-id="66d75-116">DESCRIPTION</span></span>
<span data-ttu-id="66d75-117">Użyj polecenia New-AzRoleAssignment, aby udzielić dostępu.</span><span class="sxs-lookup"><span data-stu-id="66d75-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="66d75-118">Dostęp jest udzielany przez przypisanie do nich odpowiedniej roli RBAC w odpowiednim zakresie.</span><span class="sxs-lookup"><span data-stu-id="66d75-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="66d75-119">Aby udzielić dostępu do całej subskrypcji, przypisz rolę w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="66d75-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="66d75-120">Aby udzielić dostępu określonej grupie zasobów w ramach subskrypcji, przypisz rolę w zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66d75-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="66d75-121">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="66d75-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="66d75-122">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="66d75-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="66d75-123">Aby określić grupę zabezpieczeń, użyj parametru Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="66d75-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="66d75-124">Aby określić aplikację usługi Azure AD, użyj parametrów ApplicationId lub ObjectId.</span><span class="sxs-lookup"><span data-stu-id="66d75-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="66d75-125">Przypisaną rolę należy określić przy użyciu parametru RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="66d75-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="66d75-126">Zakres, w którym udzielany jest dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="66d75-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="66d75-127">Domyślnie wybrana subskrypcja jest zaznaczona.</span><span class="sxs-lookup"><span data-stu-id="66d75-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="66d75-128">Zakres przydziału można określić przy użyciu jednej z następujących kombinacji parametrów a.</span><span class="sxs-lookup"><span data-stu-id="66d75-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="66d75-129">Zakres — jest to w pełni kwalifikowany zakres zaczynający się od \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="66d75-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="66d75-130">ResourceGroupName — aby udzielić dostępu określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="66d75-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="66d75-131">c.</span><span class="sxs-lookup"><span data-stu-id="66d75-131">c.</span></span>
<span data-ttu-id="66d75-132">ResourceName, ResourceType, ResourceGroupName i (opcjonalnie) ParentResource — aby określić określony zasób w grupie zasobów w celu udzielenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="66d75-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="66d75-133">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66d75-133">EXAMPLES</span></span>

### <span data-ttu-id="66d75-134">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="66d75-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="66d75-135">Udzielanie użytkownikowi roli czytnika dostępu w zakresie grupy zasobów, gdy przypisanie roli jest dostępne do delegowania</span><span class="sxs-lookup"><span data-stu-id="66d75-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="66d75-136">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="66d75-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="66d75-137">Udzielanie dostępu grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="66d75-137">Grant access to a security group</span></span>

### <span data-ttu-id="66d75-138">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="66d75-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="66d75-139">Udzielanie dostępu użytkownikowi w zasobie (witrynie sieci Web)</span><span class="sxs-lookup"><span data-stu-id="66d75-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="66d75-140">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="66d75-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="66d75-141">Udzielanie dostępu grupie w zasobie zagnieżdżonych (podsieci)</span><span class="sxs-lookup"><span data-stu-id="66d75-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="66d75-142">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="66d75-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="66d75-143">Udzielanie czytnikowi dostępu do podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="66d75-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="66d75-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66d75-144">PARAMETERS</span></span>

### <span data-ttu-id="66d75-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="66d75-145">-AllowDelegation</span></span>
<span data-ttu-id="66d75-146">Flaga delegowania podczas tworzenia przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="66d75-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="66d75-147">-ApplicationId</span></span>
<span data-ttu-id="66d75-148">Identyfikator aplikacji usługi ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="66d75-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-149">— Warunek</span><span class="sxs-lookup"><span data-stu-id="66d75-149">-Condition</span></span>
<span data-ttu-id="66d75-150">Warunek do zastosowania do przypisania ról.</span><span class="sxs-lookup"><span data-stu-id="66d75-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="66d75-151">-ConditionVersion</span></span>
<span data-ttu-id="66d75-152">Wersja warunku.</span><span class="sxs-lookup"><span data-stu-id="66d75-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d75-153">-DefaultProfile</span></span>
<span data-ttu-id="66d75-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="66d75-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66d75-155">— Opis</span><span class="sxs-lookup"><span data-stu-id="66d75-155">-Description</span></span>
<span data-ttu-id="66d75-156">Krótki opis przydziału ról.</span><span class="sxs-lookup"><span data-stu-id="66d75-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="66d75-157">-InputFile</span></span>
<span data-ttu-id="66d75-158">Ścieżka do przypisań ról</span><span class="sxs-lookup"><span data-stu-id="66d75-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="66d75-159">-ObjectId</span></span>
<span data-ttu-id="66d75-160">Identyfikator obiektowy usługi Azure AD użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="66d75-160">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="66d75-161">-ParentResource</span></span>
<span data-ttu-id="66d75-162">Zasób nadrzędny w hierarchii(zasobu określonego przy użyciu parametru ResourceName).</span><span class="sxs-lookup"><span data-stu-id="66d75-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="66d75-163">Należy używać tylko w połączeniu z parametrami ResourceGroupName, ResourceType i ResourceName w celu skonstruowania zakresu hierarchicznego w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="66d75-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="66d75-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66d75-164">-ResourceGroupName</span></span>
<span data-ttu-id="66d75-165">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66d75-165">The resource group name.</span></span>
<span data-ttu-id="66d75-166">Tworzy przydział, który jest skuteczny w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="66d75-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="66d75-167">W połączeniu z parametrami ResourceName, ResourceType i (opcjonalnie)ParentResource polecenie konstruuje zakres hierarchiczny w postaci względnego identyfikatoru URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="66d75-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="66d75-168">-ResourceName</span></span>
<span data-ttu-id="66d75-169">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="66d75-169">The resource name.</span></span>
<span data-ttu-id="66d75-170">Np. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="66d75-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="66d75-171">Należy używać tylko w połączeniu z parametrami ResourceGroupName, ResourceType i (opcjonalnie)ParentResource w celu skonstruowania hierarchicznego zakresu w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="66d75-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="66d75-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="66d75-172">-ResourceType</span></span>
<span data-ttu-id="66d75-173">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="66d75-173">The resource type.</span></span>
<span data-ttu-id="66d75-174">Na przykład Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="66d75-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="66d75-175">Należy używać tylko w połączeniu z parametrami ResourceGroupName, ResourceName i (opcjonalnie)ParentResource w celu skonstruowania hierarchicznego zakresu w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="66d75-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="66d75-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="66d75-176">-RoleDefinitionId</span></span>
<span data-ttu-id="66d75-177">Identyfikator roli RBAC, który musi zostać przypisany do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="66d75-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="66d75-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="66d75-178">-RoleDefinitionName</span></span>
<span data-ttu-id="66d75-179">Nazwa roli RBAC, która musi zostać przypisana do podmiotu głównego, na przykład: Czytelnik, Współautor, Administrator sieci wirtualnej itp.</span><span class="sxs-lookup"><span data-stu-id="66d75-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-180">— Zakres</span><span class="sxs-lookup"><span data-stu-id="66d75-180">-Scope</span></span>
<span data-ttu-id="66d75-181">Zakres przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="66d75-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="66d75-182">W formacie względnego URI.</span><span class="sxs-lookup"><span data-stu-id="66d75-182">In the format of relative URI.</span></span>
<span data-ttu-id="66d75-183">Na przykład:"/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="66d75-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="66d75-184">Jeśli nie zostanie określone, utworzy przypisanie roli na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="66d75-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="66d75-185">Jeśli jest określona, powinna zaczynać się od "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="66d75-185">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="66d75-186">-SignInName</span></span>
<span data-ttu-id="66d75-187">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="66d75-187">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d75-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d75-188">CommonParameters</span></span>
<span data-ttu-id="66d75-189">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d75-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d75-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66d75-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d75-191">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66d75-191">INPUTS</span></span>

### <span data-ttu-id="66d75-192">System.String</span><span class="sxs-lookup"><span data-stu-id="66d75-192">System.String</span></span>

### <span data-ttu-id="66d75-193">System.Guid</span><span class="sxs-lookup"><span data-stu-id="66d75-193">System.Guid</span></span>

## <span data-ttu-id="66d75-194">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66d75-194">OUTPUTS</span></span>

### <span data-ttu-id="66d75-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66d75-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="66d75-196">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66d75-196">NOTES</span></span>
<span data-ttu-id="66d75-197">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="66d75-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="66d75-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66d75-198">RELATED LINKS</span></span>

[<span data-ttu-id="66d75-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66d75-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="66d75-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66d75-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="66d75-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66d75-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
