---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490585"
---
# <span data-ttu-id="12eb5-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="12eb5-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="12eb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="12eb5-103">Wyświetla listę odrzuconych przydziałów usługi Azure RBAC w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="12eb5-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="12eb5-104">Domyślnie lista wszystkich Odmów przydziałów w wybranej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12eb5-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="12eb5-105">Użyj odpowiednich parametrów, aby wyświetlić listę odrzuconych przydziałów dla określonego użytkownika lub listę odrzuconych przydziałów w określonej grupie zasobów lub zasobie.</span><span class="sxs-lookup"><span data-stu-id="12eb5-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="12eb5-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12eb5-106">SYNTAX</span></span>

### <span data-ttu-id="12eb5-107">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12eb5-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12eb5-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12eb5-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12eb5-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12eb5-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12eb5-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12eb5-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12eb5-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12eb5-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12eb5-125">Opis</span><span class="sxs-lookup"><span data-stu-id="12eb5-125">DESCRIPTION</span></span>
<span data-ttu-id="12eb5-126">Użyj polecenia Get-AzDenyAssignment, aby wyświetlić listę wszystkich odrzuconych przydziałów, które są efektywne dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="12eb5-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="12eb5-127">Bez żadnych parametrów to polecenie zwraca wszystkie przydziały odmowy wprowadzone w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="12eb5-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="12eb5-128">Ta lista może być filtrowana za pomocą parametrów filtrowania dla podmiotu zabezpieczeń, odmawianie nazwy i zakresu przydziału.</span><span class="sxs-lookup"><span data-stu-id="12eb5-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="12eb5-129">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="12eb5-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="12eb5-130">Aby określić grupę zabezpieczeń, użyj parametru ObjectId usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="12eb5-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="12eb5-131">Aby określić aplikację Azure AD, użyj parametrów ServicePrincipalName lub ObjectId.</span><span class="sxs-lookup"><span data-stu-id="12eb5-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="12eb5-132">Zakres, w którym jest zabroniony dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="12eb5-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="12eb5-133">Domyślna wybrana subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="12eb5-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="12eb5-134">Zakres przydziału Odmów można określić przy użyciu jednej z następujących kombinacji parametrów a.</span><span class="sxs-lookup"><span data-stu-id="12eb5-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="12eb5-135">Zakres — to jest w pełni kwalifikowany zakres rozpoczynający się od/subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="12eb5-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="12eb5-136">Spowoduje to odfiltrowanie przydziałów, które działają w tym konkretnym zakresie, czyli wszystkich Odmów przydziałów w tym zakresie.</span><span class="sxs-lookup"><span data-stu-id="12eb5-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="12eb5-137">b.</span><span class="sxs-lookup"><span data-stu-id="12eb5-137">b.</span></span>
<span data-ttu-id="12eb5-138">ResourceGroupName — nazwa dowolnej grupy zasobów w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="12eb5-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="12eb5-139">Spowoduje to filtrowanie przydziałów, które są efektywne w określonej grupie zasobów, czyli wszystkich Odmów przydziałów w tym zakresie.</span><span class="sxs-lookup"><span data-stu-id="12eb5-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="12eb5-140">s.</span><span class="sxs-lookup"><span data-stu-id="12eb5-140">c.</span></span>
<span data-ttu-id="12eb5-141">ResourceName, ResourceType, ResourceGroupName oraz (opcjonalnie) ParentResource-identyfikuje konkretny zasób w ramach abonamentu i filtruje odmowę przydziały, które są efektywne w tym zakresie zasobów.</span><span class="sxs-lookup"><span data-stu-id="12eb5-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="12eb5-142">Aby określić odmowę dostępu dla konkretnego użytkownika w subskrypcji, użyj przełącznika ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="12eb5-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="12eb5-143">Spowoduje to wyświetlenie wszystkich zarzuconych przypisań przypisanych do użytkownika oraz do grup, do których należy dany użytkownik.</span><span class="sxs-lookup"><span data-stu-id="12eb5-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="12eb5-144">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12eb5-144">EXAMPLES</span></span>

### <span data-ttu-id="12eb5-145">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12eb5-145">Example 1</span></span>

<span data-ttu-id="12eb5-146">Lista wszystkich odrzuconych przydziałów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12eb5-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="12eb5-147">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="12eb5-147">Example 2</span></span>

<span data-ttu-id="12eb5-148">Pobiera wszystkie przydziały Odmów, które zostały wprowadzone do użytkownika john.doe@contoso.com w zakresie testRG lub wyższym.</span><span class="sxs-lookup"><span data-stu-id="12eb5-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="12eb5-149">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="12eb5-149">Example 3</span></span>

<span data-ttu-id="12eb5-150">Pobiera wszystkie przydziały Odmów określonego podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="12eb5-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="12eb5-151">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="12eb5-151">Example 4</span></span>

<span data-ttu-id="12eb5-152">Umożliwia odmowę przydziałów w zakresie witryn internetowych "site1".</span><span class="sxs-lookup"><span data-stu-id="12eb5-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

## <span data-ttu-id="12eb5-153">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12eb5-153">PARAMETERS</span></span>

### <span data-ttu-id="12eb5-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12eb5-154">-DefaultProfile</span></span>
<span data-ttu-id="12eb5-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="12eb5-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12eb5-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="12eb5-156">-DenyAssignmentName</span></span>
<span data-ttu-id="12eb5-157">Nazwa przydziału Odmów.</span><span class="sxs-lookup"><span data-stu-id="12eb5-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12eb5-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="12eb5-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="12eb5-159">Jeśli ta funkcja jest określona, zwraca odmowę przydzielonych przydziałów bezpośrednio do użytkownika i do grup, których członkiem jest użytkownik (przechodnie).</span><span class="sxs-lookup"><span data-stu-id="12eb5-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="12eb5-160">Obsługiwane tylko dla głównego podmiotu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="12eb5-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="12eb5-161">-ID</span><span class="sxs-lookup"><span data-stu-id="12eb5-161">-Id</span></span>
<span data-ttu-id="12eb5-162">Odrzuć identyfikator przydziału.</span><span class="sxs-lookup"><span data-stu-id="12eb5-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12eb5-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="12eb5-163">-ObjectId</span></span>
<span data-ttu-id="12eb5-164">Identyfikator ObjectId usługi Azure AD dla użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="12eb5-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="12eb5-165">Filtruje wszystkie przydziały Odmów wprowadzone do określonego podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="12eb5-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12eb5-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="12eb5-166">-ParentResource</span></span>
<span data-ttu-id="12eb5-167">Zasób nadrzędny w hierarchii zasobu określony przy użyciu parametru ResourceName.</span><span class="sxs-lookup"><span data-stu-id="12eb5-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="12eb5-168">Należy użyć w połączeniu z parametrami ResourceGroupName, ResourceType i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="12eb5-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="12eb5-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12eb5-169">-ResourceGroupName</span></span>
<span data-ttu-id="12eb5-170">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12eb5-170">The resource group name.</span></span>
<span data-ttu-id="12eb5-171">Umożliwia wyświetlenie listy Odmów przydziałów, które są efektywne w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="12eb5-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="12eb5-172">Polecenie używane w połączeniu z parametrami resourceName, ResourceType i ParentResource powoduje wyświetlenie listy Odmów przydziałów efektywnych dla zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="12eb5-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="12eb5-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="12eb5-173">-ResourceName</span></span>
<span data-ttu-id="12eb5-174">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="12eb5-174">The resource name.</span></span>
<span data-ttu-id="12eb5-175">Na przykład storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="12eb5-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="12eb5-176">Musi być używana w połączeniu z ResourceGroupName, ResourceType i (opcjonalnie) ParentResource parametrami.</span><span class="sxs-lookup"><span data-stu-id="12eb5-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="12eb5-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="12eb5-177">-ResourceType</span></span>
<span data-ttu-id="12eb5-178">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="12eb5-178">The resource type.</span></span>
<span data-ttu-id="12eb5-179">Na przykład Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="12eb5-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="12eb5-180">Należy użyć w połączeniu z ResourceGroupName, resourceName i (opcjonalnie) ParentResource parametrami.</span><span class="sxs-lookup"><span data-stu-id="12eb5-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="12eb5-181">-Zakres</span><span class="sxs-lookup"><span data-stu-id="12eb5-181">-Scope</span></span>
<span data-ttu-id="12eb5-182">Zakres przypisania roli.</span><span class="sxs-lookup"><span data-stu-id="12eb5-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="12eb5-183">W formacie względnego identyfikatora URI.</span><span class="sxs-lookup"><span data-stu-id="12eb5-183">In the format of relative URI.</span></span>
<span data-ttu-id="12eb5-184">Na przykład/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="12eb5-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="12eb5-185">Musi zaczynać się od "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="12eb5-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="12eb5-186">Polecenie filtruje wszystkie przydziały Odmów, które obowiązują w tym zakresie.</span><span class="sxs-lookup"><span data-stu-id="12eb5-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="12eb5-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="12eb5-187">-ServicePrincipalName</span></span>
<span data-ttu-id="12eb5-188">Obiekt ServicePrincipalName głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="12eb5-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="12eb5-189">Filtruje wszystkie przydziały Odmów wprowadzone w określonej aplikacji usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="12eb5-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="12eb5-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="12eb5-190">-SignInName</span></span>
<span data-ttu-id="12eb5-191">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="12eb5-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="12eb5-192">Filtruje wszystkie przydziały Odmów wprowadzone do określonego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="12eb5-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="12eb5-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12eb5-193">CommonParameters</span></span>
<span data-ttu-id="12eb5-194">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12eb5-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12eb5-195">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12eb5-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12eb5-196">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12eb5-196">INPUTS</span></span>

### <span data-ttu-id="12eb5-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="12eb5-197">System.Guid</span></span>

### <span data-ttu-id="12eb5-198">System. String</span><span class="sxs-lookup"><span data-stu-id="12eb5-198">System.String</span></span>

## <span data-ttu-id="12eb5-199">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12eb5-199">OUTPUTS</span></span>

### <span data-ttu-id="12eb5-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="12eb5-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="12eb5-201">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12eb5-201">NOTES</span></span>
<span data-ttu-id="12eb5-202">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="12eb5-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="12eb5-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12eb5-203">RELATED LINKS</span></span>
