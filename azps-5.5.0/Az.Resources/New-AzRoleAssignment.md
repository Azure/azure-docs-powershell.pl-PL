---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183659"
---
# <span data-ttu-id="7b777-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7b777-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="7b777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b777-102">SYNOPSIS</span></span>
<span data-ttu-id="7b777-103">Przypisuje określoną rolę RBAC do określonego podmiotu zabezpieczeń w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="7b777-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="7b777-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7b777-104">SYNTAX</span></span>

### <span data-ttu-id="7b777-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7b777-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b777-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b777-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b777-116">OPIS</span><span class="sxs-lookup"><span data-stu-id="7b777-116">DESCRIPTION</span></span>
<span data-ttu-id="7b777-117">Użyj polecenia New-AzRoleAssignment, aby udzielić dostępu.</span><span class="sxs-lookup"><span data-stu-id="7b777-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="7b777-118">Dostęp jest udzielany przez przypisanie do nich odpowiedniej roli RBAC w odpowiednim zakresie.</span><span class="sxs-lookup"><span data-stu-id="7b777-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="7b777-119">Aby udzielić dostępu do całej subskrypcji, przypisz rolę w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7b777-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="7b777-120">Aby udzielić dostępu określonej grupie zasobów w ramach subskrypcji, przypisz rolę w zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b777-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="7b777-121">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="7b777-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="7b777-122">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="7b777-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="7b777-123">Aby określić grupę zabezpieczeń, użyj parametru Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="7b777-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="7b777-124">Aby określić aplikację usługi Azure AD, użyj parametrów ApplicationId lub ObjectId.</span><span class="sxs-lookup"><span data-stu-id="7b777-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="7b777-125">Przypisaną rolę należy określić przy użyciu parametru RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="7b777-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="7b777-126">Zakres, w którym udzielany jest dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="7b777-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="7b777-127">Domyślnie wybrana subskrypcja jest zaznaczona.</span><span class="sxs-lookup"><span data-stu-id="7b777-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="7b777-128">Zakres przydziału można określić przy użyciu jednej z następujących kombinacji parametrów a.</span><span class="sxs-lookup"><span data-stu-id="7b777-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="7b777-129">Zakres — jest to w pełni kwalifikowany zakres zaczynający się od \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="7b777-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="7b777-130">ResourceGroupName — aby udzielić dostępu określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b777-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="7b777-131">c.</span><span class="sxs-lookup"><span data-stu-id="7b777-131">c.</span></span>
<span data-ttu-id="7b777-132">ResourceName, ResourceType, ResourceGroupName i (opcjonalnie) ParentResource — aby określić określony zasób w grupie zasobów w celu udzielenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="7b777-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="7b777-133">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7b777-133">EXAMPLES</span></span>

### <span data-ttu-id="7b777-134">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b777-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="7b777-135">Udzielanie użytkownikowi roli czytnika dostępu w zakresie grupy zasobów z dostępnym przypisaniem roli do delegowania</span><span class="sxs-lookup"><span data-stu-id="7b777-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="7b777-136">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7b777-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="7b777-137">Udzielanie dostępu grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="7b777-137">Grant access to a security group</span></span>

### <span data-ttu-id="7b777-138">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7b777-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="7b777-139">Udzielanie dostępu użytkownikowi w zasobie (witrynie sieci Web)</span><span class="sxs-lookup"><span data-stu-id="7b777-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="7b777-140">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="7b777-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="7b777-141">Udzielanie dostępu grupie w zasobie zagnieżdżonych (podsieci)</span><span class="sxs-lookup"><span data-stu-id="7b777-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="7b777-142">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="7b777-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="7b777-143">Udzielanie czytnikowi dostępu do podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="7b777-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="7b777-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b777-144">PARAMETERS</span></span>

### <span data-ttu-id="7b777-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="7b777-145">-AllowDelegation</span></span>
<span data-ttu-id="7b777-146">Flaga delegowania podczas tworzenia przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="7b777-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="7b777-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7b777-147">-ApplicationId</span></span>
<span data-ttu-id="7b777-148">Identyfikator aplikacji usługi ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7b777-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="7b777-149">— Warunek</span><span class="sxs-lookup"><span data-stu-id="7b777-149">-Condition</span></span>
<span data-ttu-id="7b777-150">Warunek do zastosowania do przypisania ról.</span><span class="sxs-lookup"><span data-stu-id="7b777-150">Condition to be applied to the RoleAssignment.</span></span>

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

### <span data-ttu-id="7b777-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="7b777-151">-ConditionVersion</span></span>
<span data-ttu-id="7b777-152">Wersja warunku.</span><span class="sxs-lookup"><span data-stu-id="7b777-152">Version of the condition.</span></span>

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

### <span data-ttu-id="7b777-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b777-153">-DefaultProfile</span></span>
<span data-ttu-id="7b777-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7b777-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b777-155">— Opis</span><span class="sxs-lookup"><span data-stu-id="7b777-155">-Description</span></span>
<span data-ttu-id="7b777-156">Krótki opis przydziału ról.</span><span class="sxs-lookup"><span data-stu-id="7b777-156">Brief description of the role assignment.</span></span>

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

### <span data-ttu-id="7b777-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7b777-157">-InputFile</span></span>
<span data-ttu-id="7b777-158">Ścieżka do przypisań ról</span><span class="sxs-lookup"><span data-stu-id="7b777-158">Path to role assignment json</span></span>

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

### <span data-ttu-id="7b777-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7b777-159">-ObjectId</span></span>
<span data-ttu-id="7b777-160">Identyfikator objectid usługi Azure AD użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="7b777-160">Azure AD Objectid of the user, group or service principal.</span></span>

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

### <span data-ttu-id="7b777-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="7b777-161">-ParentResource</span></span>
<span data-ttu-id="7b777-162">Zasób nadrzędny w hierarchii(zasobu określonego przy użyciu parametru ResourceName).</span><span class="sxs-lookup"><span data-stu-id="7b777-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="7b777-163">Należy używać tylko w połączeniu z parametrami ResourceGroupName, ResourceType i ResourceName w celu skonstruowania zakresu hierarchicznego w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="7b777-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="7b777-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b777-164">-ResourceGroupName</span></span>
<span data-ttu-id="7b777-165">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b777-165">The resource group name.</span></span>
<span data-ttu-id="7b777-166">Tworzy przydział, który jest skuteczny w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b777-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="7b777-167">W połączeniu z parametrami ResourceName, ResourceType i (opcjonalnie)ParentResource polecenie konstruuje hierarchiczny zakres w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="7b777-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="7b777-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7b777-168">-ResourceName</span></span>
<span data-ttu-id="7b777-169">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7b777-169">The resource name.</span></span>
<span data-ttu-id="7b777-170">Np. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="7b777-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="7b777-171">Należy używać tylko w połączeniu z parametrami ResourceGroupName, ResourceType i (opcjonalnie)ParentResource w celu skonstruowania hierarchicznego zakresu w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="7b777-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="7b777-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7b777-172">-ResourceType</span></span>
<span data-ttu-id="7b777-173">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="7b777-173">The resource type.</span></span>
<span data-ttu-id="7b777-174">Na przykład Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="7b777-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="7b777-175">Należy używać tylko w połączeniu z parametrami ResourceGroupName, ResourceName i (opcjonalnie)ParentResource w celu skonstruowania zakresu hierarchicznego w postaci względnego URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="7b777-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="7b777-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7b777-176">-RoleDefinitionId</span></span>
<span data-ttu-id="7b777-177">Identyfikator roli RBAC, który musi zostać przypisany do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7b777-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="7b777-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7b777-178">-RoleDefinitionName</span></span>
<span data-ttu-id="7b777-179">Nazwa roli RBAC, która musi zostać przypisana do podmiotu głównego, na przykład: Czytelnik, Współautor, Administrator sieci wirtualnej itp.</span><span class="sxs-lookup"><span data-stu-id="7b777-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="7b777-180">— Zakres</span><span class="sxs-lookup"><span data-stu-id="7b777-180">-Scope</span></span>
<span data-ttu-id="7b777-181">Zakres przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="7b777-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="7b777-182">W formacie względnego URI.</span><span class="sxs-lookup"><span data-stu-id="7b777-182">In the format of relative URI.</span></span>
<span data-ttu-id="7b777-183">Na przykład: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="7b777-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="7b777-184">Jeśli nie zostanie określone, utworzy przypisanie roli na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7b777-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="7b777-185">Jeśli jest określona, powinna zaczynać się od "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="7b777-185">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="7b777-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7b777-186">-SignInName</span></span>
<span data-ttu-id="7b777-187">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7b777-187">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="7b777-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b777-188">CommonParameters</span></span>
<span data-ttu-id="7b777-189">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b777-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b777-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b777-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b777-191">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b777-191">INPUTS</span></span>

### <span data-ttu-id="7b777-192">System.String</span><span class="sxs-lookup"><span data-stu-id="7b777-192">System.String</span></span>

### <span data-ttu-id="7b777-193">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7b777-193">System.Guid</span></span>

## <span data-ttu-id="7b777-194">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b777-194">OUTPUTS</span></span>

### <span data-ttu-id="7b777-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7b777-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="7b777-196">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7b777-196">NOTES</span></span>
<span data-ttu-id="7b777-197">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="7b777-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7b777-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b777-198">RELATED LINKS</span></span>

[<span data-ttu-id="7b777-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7b777-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="7b777-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7b777-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="7b777-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7b777-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
