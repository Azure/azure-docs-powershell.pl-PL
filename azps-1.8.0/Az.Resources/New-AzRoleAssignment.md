---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 748f0396199753a13c8a977fc5d58f3986896a86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708341"
---
# <span data-ttu-id="808b7-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="808b7-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="808b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="808b7-102">SYNOPSIS</span></span>
<span data-ttu-id="808b7-103">Umożliwia przypisanie określonej roli RBAC do określonego podmiotu zabezpieczeń w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="808b7-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="808b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="808b7-104">SYNTAX</span></span>

### <span data-ttu-id="808b7-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="808b7-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-114">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b7-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="808b7-115">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="808b7-116">Opis</span><span class="sxs-lookup"><span data-stu-id="808b7-116">DESCRIPTION</span></span>
<span data-ttu-id="808b7-117">Aby udzielić dostępu, użyj polecenia New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="808b7-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="808b7-118">Dostęp jest udzielany przez przypisanie odpowiedniej roli RBAC do odpowiednich zakresów.</span><span class="sxs-lookup"><span data-stu-id="808b7-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="808b7-119">Aby udzielić dostępu do całej subskrypcji, przypisz rolę w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="808b7-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="808b7-120">Aby udzielić dostępu do określonej grupy zasobów w ramach abonamentu, przypisz rolę w zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="808b7-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="808b7-121">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="808b7-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="808b7-122">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="808b7-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="808b7-123">Aby określić grupę zabezpieczeń, użyj parametru ObjectId usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="808b7-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="808b7-124">Aby określić aplikację Azure AD, użyj parametrów identyfikatora aplikacji lub obiektu ObjectId.</span><span class="sxs-lookup"><span data-stu-id="808b7-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="808b7-125">Rola, która jest przypisywana, musi być określona przy użyciu parametru RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="808b7-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="808b7-126">Zakres, w którym jest udzielany dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="808b7-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="808b7-127">Domyślna wybrana subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="808b7-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="808b7-128">Zakres przydziału można określić przy użyciu jednej z następujących kombinacji parametrów a.</span><span class="sxs-lookup"><span data-stu-id="808b7-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="808b7-129">Zakres — to jest w pełni kwalifikowany zakres rozpoczynający się od/subscriptions/- \< subskrypcji \> b.</span><span class="sxs-lookup"><span data-stu-id="808b7-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="808b7-130">ResourceGroupName, aby udzielić dostępu do określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="808b7-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="808b7-131">s.</span><span class="sxs-lookup"><span data-stu-id="808b7-131">c.</span></span>
<span data-ttu-id="808b7-132">ResourceName, ResourceType, ResourceGroupName oraz (opcjonalnie) ParentResource-aby określić konkretny zasób w grupie zasobów, do którego ma być udzielany dostęp.</span><span class="sxs-lookup"><span data-stu-id="808b7-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="808b7-133">Przykłady</span><span class="sxs-lookup"><span data-stu-id="808b7-133">EXAMPLES</span></span>

### <span data-ttu-id="808b7-134">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="808b7-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="808b7-135">Udzielanie dostępu do roli czytelnika użytkownikowi w zakresie grupy zasobów z przydziałem roli dostępnym dla delegowania</span><span class="sxs-lookup"><span data-stu-id="808b7-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="808b7-136">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="808b7-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="808b7-137">Udzielanie dostępu do grupy zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="808b7-137">Grant access to a security group</span></span>

### <span data-ttu-id="808b7-138">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="808b7-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="808b7-139">Udzielanie dostępu użytkownikowi w ramach zasobu (witryny sieci Web)</span><span class="sxs-lookup"><span data-stu-id="808b7-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="808b7-140">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="808b7-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="808b7-141">Udzielanie dostępu do grupy w ramach zasobów zagnieżdżonych (podsieci)</span><span class="sxs-lookup"><span data-stu-id="808b7-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="808b7-142">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="808b7-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="808b7-143">Udzielanie dostępu czytelnikowi głównemu usługi</span><span class="sxs-lookup"><span data-stu-id="808b7-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="808b7-144">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="808b7-144">PARAMETERS</span></span>

### <span data-ttu-id="808b7-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="808b7-145">-AllowDelegation</span></span>
<span data-ttu-id="808b7-146">Flaga delegowania podczas tworzenia zadania roli.</span><span class="sxs-lookup"><span data-stu-id="808b7-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="808b7-147">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="808b7-147">-ApplicationId</span></span>
<span data-ttu-id="808b7-148">Identyfikator aplikacji serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="808b7-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="808b7-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808b7-149">-DefaultProfile</span></span>
<span data-ttu-id="808b7-150">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="808b7-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="808b7-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="808b7-151">-ObjectId</span></span>
<span data-ttu-id="808b7-152">Identyfikator objectid usługi Azure AD dla użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="808b7-152">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="808b7-153">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="808b7-153">-ParentResource</span></span>
<span data-ttu-id="808b7-154">Zasób nadrzędny w hierarchii (zasobu określonego za pomocą parametru ResourceName).</span><span class="sxs-lookup"><span data-stu-id="808b7-154">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="808b7-155">Należy użyć tylko w połączeniu z parametrami ResourceGroupName, ResourceType i resourceName w celu skonstruowania zakresu hierarchicznego w formie względnego identyfikatora URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="808b7-155">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="808b7-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808b7-156">-ResourceGroupName</span></span>
<span data-ttu-id="808b7-157">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="808b7-157">The resource group name.</span></span>
<span data-ttu-id="808b7-158">Umożliwia utworzenie przydziału efektywnego dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="808b7-158">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="808b7-159">Gdy jest używana w połączeniu z parametrami resourceName, ResourceType i (opcjonalnie) ParentResource parametry, polecenie konstruuje zakres hierarchiczny w formie względnego identyfikatora URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="808b7-159">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="808b7-160">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="808b7-160">-ResourceName</span></span>
<span data-ttu-id="808b7-161">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="808b7-161">The resource name.</span></span>
<span data-ttu-id="808b7-162">Na przykład storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="808b7-162">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="808b7-163">Należy użyć tylko w połączeniu z ResourceGroupName, ResourceType i (opcjonalnie) ParentResource parametrami w celu skonstruowania zakresu hierarchicznego w formie względnego identyfikatora URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="808b7-163">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="808b7-164">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="808b7-164">-ResourceType</span></span>
<span data-ttu-id="808b7-165">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="808b7-165">The resource type.</span></span>
<span data-ttu-id="808b7-166">Na przykład Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="808b7-166">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="808b7-167">Powinna być używana tylko w połączeniu z ResourceGroupName, resourceName i (opcjonalnie) ParentResource parametrami w celu skonstruowania zakresu hierarchicznego w formie względnego identyfikatora URI identyfikującego zasób.</span><span class="sxs-lookup"><span data-stu-id="808b7-167">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="808b7-168">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="808b7-168">-RoleDefinitionId</span></span>
<span data-ttu-id="808b7-169">Identyfikator roli RBAC, która musi zostać przypisana do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="808b7-169">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="808b7-170">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="808b7-170">-RoleDefinitionName</span></span>
<span data-ttu-id="808b7-171">Nazwa roli RBAC, która musi zostać przypisana do podmiotu zabezpieczeń, takiego jak czytelnik, współautor, administrator sieci wirtualnej itd.</span><span class="sxs-lookup"><span data-stu-id="808b7-171">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="808b7-172">-Zakres</span><span class="sxs-lookup"><span data-stu-id="808b7-172">-Scope</span></span>
<span data-ttu-id="808b7-173">Zakres przypisania roli.</span><span class="sxs-lookup"><span data-stu-id="808b7-173">The Scope of the role assignment.</span></span>
<span data-ttu-id="808b7-174">W formacie względnego identyfikatora URI.</span><span class="sxs-lookup"><span data-stu-id="808b7-174">In the format of relative URI.</span></span>
<span data-ttu-id="808b7-175">Na przykład "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="808b7-175">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="808b7-176">Jeśli nie zostanie określona, utworzy przypisanie roli na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="808b7-176">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="808b7-177">Jeśli jest określona, powinna rozpoczynać się od "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="808b7-177">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="808b7-178">-SignInName</span><span class="sxs-lookup"><span data-stu-id="808b7-178">-SignInName</span></span>
<span data-ttu-id="808b7-179">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="808b7-179">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="808b7-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808b7-180">CommonParameters</span></span>
<span data-ttu-id="808b7-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808b7-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808b7-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808b7-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808b7-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="808b7-183">INPUTS</span></span>

### <span data-ttu-id="808b7-184">System. String</span><span class="sxs-lookup"><span data-stu-id="808b7-184">System.String</span></span>

### <span data-ttu-id="808b7-185">System. GUID</span><span class="sxs-lookup"><span data-stu-id="808b7-185">System.Guid</span></span>

## <span data-ttu-id="808b7-186">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="808b7-186">OUTPUTS</span></span>

### <span data-ttu-id="808b7-187">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="808b7-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="808b7-188">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="808b7-188">NOTES</span></span>
<span data-ttu-id="808b7-189">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="808b7-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="808b7-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="808b7-190">RELATED LINKS</span></span>

[<span data-ttu-id="808b7-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="808b7-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="808b7-192">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="808b7-192">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="808b7-193">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="808b7-193">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)