---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: cd82db28fbf9902b0dedf9415290d769db3ea231
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251595"
---
# <span data-ttu-id="d777c-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d777c-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="d777c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d777c-102">SYNOPSIS</span></span>
<span data-ttu-id="d777c-103">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d777c-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="d777c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d777c-104">SYNTAX</span></span>

### <span data-ttu-id="d777c-105">SimpleParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d777c-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d777c-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d777c-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d777c-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777c-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d777c-121">OPIS</span><span class="sxs-lookup"><span data-stu-id="d777c-121">DESCRIPTION</span></span>
<span data-ttu-id="d777c-122">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d777c-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="d777c-123">Domyślny zestaw parametrów używa wartości domyślnych dla parametrów, jeśli użytkownik ich nie poda.</span><span class="sxs-lookup"><span data-stu-id="d777c-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="d777c-124">Aby uzyskać więcej informacji na temat używanych wartości domyślnych, zobacz opis podanych parametrów poniżej.</span><span class="sxs-lookup"><span data-stu-id="d777c-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="d777c-125">To polecenie cmdlet umożliwia przypisanie roli do podmiotu zabezpieczeń usługi wraz z parametrami. Jeśli żaden z tych parametrów nie zostanie podany, do podmiotu zabezpieczeń usługi nie zostanie przypisana `Role` `Scope` żadna rola.</span><span class="sxs-lookup"><span data-stu-id="d777c-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="d777c-126">Wartością domyślną parametrów i parametrów są odpowiednio "Współautor" i bieżąca subskrypcja (uwaga: wartości domyślne są używane tylko wtedy, gdy użytkownik dostarcza wartość dla jednego z dwóch parametrów, ale nie `Role` `Scope` drugi).</span><span class="sxs-lookup"><span data-stu-id="d777c-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="d777c-127">Polecenie cmdlet niejawnie tworzy również aplikację i ustawia jej właściwości (jeśli wartość ApplicationId nie jest podano).</span><span class="sxs-lookup"><span data-stu-id="d777c-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="d777c-128">Aby zaktualizować konkretne parametry aplikacji, użyj Set-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d777c-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="d777c-129">Po utworzeniu podmiotu zabezpieczeń usługi za pomocą **polecenia New-AzADServicePrincipal** dane wyjściowe zawierają poświadczenia, które należy chronić.</span><span class="sxs-lookup"><span data-stu-id="d777c-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="d777c-130">Rozważ użycie tożsamości [zarządzanych,](/azure/active-directory/managed-identities-azure-resources/overview) aby uniknąć konieczności używania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="d777c-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="d777c-131">Domyślnie **new-AzADServicePrincipal** przypisuje rolę [](/azure/role-based-access-control/built-in-roles#contributor) współautora podmiotowi usługi w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d777c-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="d777c-132">Aby zmniejszyć ryzyko wystąpienia naruszonego podmiotu zabezpieczeń usługi, przypisz bardziej konkretną rolę i zawęzij zakres do grupy zasobów lub zasobu.</span><span class="sxs-lookup"><span data-stu-id="d777c-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="d777c-133">Zobacz [Kroki, aby dodać przypisanie roli,](/azure/role-based-access-control/role-assignments-steps) aby uzyskać więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="d777c-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="d777c-134">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d777c-134">EXAMPLES</span></span>

### <span data-ttu-id="d777c-135">Przykład 1. Tworzenie podmiotu zabezpieczeń prostej usługi AD</span><span class="sxs-lookup"><span data-stu-id="d777c-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="d777c-136">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="d777c-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="d777c-137">Ponieważ nie podano identyfikatora aplikacji, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d777c-138">Ponieważ nie podano żadnych wartości lub podmiot zabezpieczeń utworzonej usługi `Role` `Scope` nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="d777c-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="d777c-139">Przykład 2. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określoną rolą i zakresem domyślnym</span><span class="sxs-lookup"><span data-stu-id="d777c-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="d777c-140">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="d777c-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d777c-141">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d777c-142">Podmiot zabezpieczeń usługi został utworzony przy użyciu uprawnień "Czytnik" dla bieżącej subskrypcji (ponieważ dla parametru nie podano żadnej `Scope` wartości).</span><span class="sxs-lookup"><span data-stu-id="d777c-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="d777c-143">Przykład 3. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określonym zakresem i rolą domyślną</span><span class="sxs-lookup"><span data-stu-id="d777c-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="d777c-144">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="d777c-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d777c-145">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d777c-146">Podmiot zabezpieczeń usługi został utworzony przy użyciu uprawnień "Współautor" (ponieważ dla parametru nie podano żadnej wartości) w zakresie `Role` dostępnej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d777c-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="d777c-147">Przykład 4. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określonym zakresem i rolą</span><span class="sxs-lookup"><span data-stu-id="d777c-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="d777c-148">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="d777c-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d777c-149">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d777c-150">Podmiot zabezpieczeń usługi został utworzony przy użyciu uprawnień "Czytnik" w zakresie dostępnej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d777c-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="d777c-151">Przykład 5. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu identyfikatora aplikacji z przypisaniem roli</span><span class="sxs-lookup"><span data-stu-id="d777c-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="d777c-152">Tworzy nowy podmiot zabezpieczeń usługi AD dla aplikacji o identyfikatorze aplikacji '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span><span class="sxs-lookup"><span data-stu-id="d777c-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="d777c-153">Ponieważ nie podano żadnych wartości lub podmiot zabezpieczeń utworzonej usługi `Role` `Scope` nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="d777c-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="d777c-154">Przykład 6. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="d777c-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="d777c-155">Pobiera aplikację z identyfikatorem obiektu "3ede3c26-b443-4e0b-9efc-b05e68338dc3" i potoki, które są do polecenia cmdlet programu New-AzADServicePrincipal, w celu utworzenia nowego podmiotu zabezpieczeń usługi AD dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d777c-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="d777c-156">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d777c-156">PARAMETERS</span></span>

### <span data-ttu-id="d777c-157">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d777c-157">-ApplicationId</span></span>
<span data-ttu-id="d777c-158">Unikatowy identyfikator aplikacji podmiotu zabezpieczeń usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="d777c-158">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="d777c-159">Po utworzeniu tej właściwości nie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="d777c-159">Once created this property cannot be changed.</span></span>
<span data-ttu-id="d777c-160">Jeśli nie zostanie określony identyfikator aplikacji, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="d777c-160">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-161">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d777c-161">-ApplicationObject</span></span>
<span data-ttu-id="d777c-162">Obiekt reprezentujący aplikację, dla której jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-162">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-163">-CertValue</span><span class="sxs-lookup"><span data-stu-id="d777c-163">-CertValue</span></span>
<span data-ttu-id="d777c-164">Wartość typu poświadczeń "asymetrycznego".</span><span class="sxs-lookup"><span data-stu-id="d777c-164">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="d777c-165">Reprezentuje certyfikat zakodowany na podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="d777c-165">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d777c-166">-DefaultProfile</span></span>
<span data-ttu-id="d777c-167">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d777c-167">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-168">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="d777c-168">-DisplayName</span></span>
<span data-ttu-id="d777c-169">Przyjazna nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-169">The friendly name of the service principal.</span></span> <span data-ttu-id="d777c-170">Jeśli nazwa wyświetlana nie zostanie podany, ta wartość będzie domyślnie wyświetlana jako "azure-powershell-MM-dd-yyyy-HH-mm-ss", gdzie sufiks jest czasem tworzenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d777c-170">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-171">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d777c-171">-EndDate</span></span>
<span data-ttu-id="d777c-172">Data zakończenia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="d777c-172">The effective end date of the credential usage.</span></span>
<span data-ttu-id="d777c-173">Domyślna wartość daty końcowej wynosi jeden rok od dnia dzisiejszego.</span><span class="sxs-lookup"><span data-stu-id="d777c-173">The default end date value is one year from today.</span></span> <span data-ttu-id="d777c-174">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę ważności certyfikatu X509 lub wcześniejszą.</span><span class="sxs-lookup"><span data-stu-id="d777c-174">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-175">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="d777c-175">-KeyCredential</span></span>
<span data-ttu-id="d777c-176">Zbiór poświadczeń klucza skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="d777c-176">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-177">— Hasło</span><span class="sxs-lookup"><span data-stu-id="d777c-177">-Password</span></span>
<span data-ttu-id="d777c-178">Hasło, które ma być skojarzone z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-178">The password to be associated with the service principal.</span></span> <span data-ttu-id="d777c-179">Jeśli hasło nie zostanie podane, zostanie wygenerowany losowy identyfikator GUID, który będzie używany jako hasło.</span><span class="sxs-lookup"><span data-stu-id="d777c-179">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-180">- PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="d777c-180">-PasswordCredential</span></span>
<span data-ttu-id="d777c-181">Zbiór poświadczeń hasła skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="d777c-181">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-182">— Rola</span><span class="sxs-lookup"><span data-stu-id="d777c-182">-Role</span></span>
<span data-ttu-id="d777c-183">Rola podmiotu zabezpieczeń usługi w zakresie.</span><span class="sxs-lookup"><span data-stu-id="d777c-183">The role that the service principal has over the scope.</span></span> <span data-ttu-id="d777c-184">Jeśli podano wartość, ale nie podano żadnej wartości, zostanie ona domyślnie dodana do roli `Scope` `Role` `Role` "Współautor".</span><span class="sxs-lookup"><span data-stu-id="d777c-184">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-185">— Zakres</span><span class="sxs-lookup"><span data-stu-id="d777c-185">-Scope</span></span>
<span data-ttu-id="d777c-186">Zakres uprawnień podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-186">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="d777c-187">Jeśli podano wartość, ale nie podano żadnej wartości, zostanie ona domyślnie dodana `Role` `Scope` do `Scope` bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d777c-187">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-188">- SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="d777c-188">-SkipAssignment</span></span>
<span data-ttu-id="d777c-189">Jeśli zostanie ustawiony, pominiesz tworzenie domyślnego przydziału ról dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d777c-189">If set, will skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-190">- StartDate</span><span class="sxs-lookup"><span data-stu-id="d777c-190">-StartDate</span></span>
<span data-ttu-id="d777c-191">Data rozpoczęcia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="d777c-191">The effective start date of the credential usage.</span></span>
<span data-ttu-id="d777c-192">Domyślna wartość daty rozpoczęcia to dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="d777c-192">The default start date value is today.</span></span> <span data-ttu-id="d777c-193">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę, od kiedy certyfikat X509 jest prawidłowy, lub później.</span><span class="sxs-lookup"><span data-stu-id="d777c-193">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d777c-194">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d777c-194">-Confirm</span></span>
<span data-ttu-id="d777c-195">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d777c-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d777c-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d777c-196">-WhatIf</span></span>
<span data-ttu-id="d777c-197">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d777c-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d777c-198">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d777c-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d777c-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d777c-199">CommonParameters</span></span>
<span data-ttu-id="d777c-200">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d777c-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d777c-201">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d777c-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d777c-202">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d777c-202">INPUTS</span></span>

### <span data-ttu-id="d777c-203">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d777c-203">System.Guid</span></span>

### <span data-ttu-id="d777c-204">System.String</span><span class="sxs-lookup"><span data-stu-id="d777c-204">System.String</span></span>

### <span data-ttu-id="d777c-205">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d777c-205">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="d777c-206">Parametry: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d777c-206">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="d777c-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="d777c-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="d777c-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="d777c-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="d777c-209">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d777c-209">System.Security.SecureString</span></span>

### <span data-ttu-id="d777c-210">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d777c-210">System.DateTime</span></span>

## <span data-ttu-id="d777c-211">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d777c-211">OUTPUTS</span></span>

### <span data-ttu-id="d777c-212">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d777c-212">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="d777c-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="d777c-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="d777c-214">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d777c-214">NOTES</span></span>
<span data-ttu-id="d777c-215">Słowa kluczowe: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="d777c-215">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d777c-216">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d777c-216">RELATED LINKS</span></span>

[<span data-ttu-id="d777c-217">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d777c-217">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="d777c-218">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d777c-218">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="d777c-219">New-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="d777c-219">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="d777c-220">Remove-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="d777c-220">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d777c-221">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d777c-221">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="d777c-222">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d777c-222">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="d777c-223">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d777c-223">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

