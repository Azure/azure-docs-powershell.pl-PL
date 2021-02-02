---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3a410dfb43cc767b0a73086147042425d42764d1
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251628"
---
# <span data-ttu-id="48ef1-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="48ef1-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="48ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="48ef1-103">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="48ef1-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="48ef1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48ef1-104">SYNTAX</span></span>

### <span data-ttu-id="48ef1-105">SimpleParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="48ef1-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48ef1-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48ef1-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ef1-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ef1-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48ef1-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="48ef1-120">DESCRIPTION</span></span>
<span data-ttu-id="48ef1-121">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="48ef1-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="48ef1-122">Domyślny zestaw parametrów używa wartości domyślnych dla parametrów, jeśli użytkownik ich nie poda.</span><span class="sxs-lookup"><span data-stu-id="48ef1-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="48ef1-123">Aby uzyskać więcej informacji na temat używanych wartości domyślnych, zobacz opis podanych parametrów poniżej.</span><span class="sxs-lookup"><span data-stu-id="48ef1-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="48ef1-124">To polecenie cmdlet umożliwia przypisanie roli do podmiotu zabezpieczeń usługi wraz z parametrami. Jeśli żaden z tych parametrów nie zostanie podany, do podmiotu zabezpieczeń usługi nie zostanie przypisana `Role` `Scope` żadna rola.</span><span class="sxs-lookup"><span data-stu-id="48ef1-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="48ef1-125">Wartością domyślną parametrów i parametrów są odpowiednio "Współautor" i bieżąca subskrypcja (uwaga: wartości domyślne są używane tylko wtedy, gdy użytkownik dostarcza wartość dla jednego z dwóch parametrów, ale nie `Role` `Scope` drugi).</span><span class="sxs-lookup"><span data-stu-id="48ef1-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="48ef1-126">Polecenie cmdlet niejawnie tworzy również aplikację i ustawia jej właściwości (jeśli wartość ApplicationId nie jest podano).</span><span class="sxs-lookup"><span data-stu-id="48ef1-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="48ef1-127">Aby zaktualizować konkretne parametry aplikacji, użyj Set-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48ef1-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="48ef1-128">Po utworzeniu podmiotu zabezpieczeń usługi za pomocą **polecenia New-AzADServicePrincipal** dane wyjściowe zawierają poświadczenia, które należy chronić.</span><span class="sxs-lookup"><span data-stu-id="48ef1-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="48ef1-129">Rozważ użycie tożsamości [zarządzanych,](/azure/active-directory/managed-identities-azure-resources/overview) aby uniknąć konieczności używania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="48ef1-129">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="48ef1-130">Domyślnie **new-AzADServicePrincipal** przypisuje rolę [](/azure/role-based-access-control/built-in-roles#contributor) współautora podmiotowi usługi w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="48ef1-130">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="48ef1-131">Aby zmniejszyć ryzyko wystąpienia naruszonego podmiotu zabezpieczeń usługi, przypisz bardziej konkretną rolę i zawęzij zakres do grupy zasobów lub zasobu.</span><span class="sxs-lookup"><span data-stu-id="48ef1-131">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="48ef1-132">Zobacz [Kroki, aby dodać przypisanie roli,](/azure/role-based-access-control/role-assignments-steps) aby uzyskać więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="48ef1-132">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="48ef1-133">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48ef1-133">EXAMPLES</span></span>

### <span data-ttu-id="48ef1-134">Przykład 1. Tworzenie podmiotu zabezpieczeń prostej usługi AD</span><span class="sxs-lookup"><span data-stu-id="48ef1-134">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="48ef1-135">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="48ef1-135">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="48ef1-136">Ponieważ nie podano identyfikatora aplikacji, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-136">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="48ef1-137">Ponieważ nie podano żadnych wartości lub podmiot zabezpieczeń utworzonej usługi `Role` `Scope` nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="48ef1-137">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="48ef1-138">Przykład 2. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określoną rolą i zakresem domyślnym</span><span class="sxs-lookup"><span data-stu-id="48ef1-138">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="48ef1-139">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="48ef1-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="48ef1-140">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="48ef1-141">Podmiot zabezpieczeń usługi został utworzony przy użyciu uprawnień "Czytnik" dla bieżącej subskrypcji (ponieważ dla parametru nie podano żadnej `Scope` wartości).</span><span class="sxs-lookup"><span data-stu-id="48ef1-141">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="48ef1-142">Przykład 3. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określonym zakresem i rolą domyślną</span><span class="sxs-lookup"><span data-stu-id="48ef1-142">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="48ef1-143">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="48ef1-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="48ef1-144">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="48ef1-145">Podmiot zabezpieczeń usługi został utworzony przy użyciu uprawnień "Współautor" (ponieważ dla parametru nie podano żadnej wartości) w zakresie `Role` dostępnej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48ef1-145">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="48ef1-146">Przykład 4. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określonym zakresem i rolą</span><span class="sxs-lookup"><span data-stu-id="48ef1-146">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="48ef1-147">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="48ef1-147">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="48ef1-148">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-148">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="48ef1-149">Podmiot zabezpieczeń usługi został utworzony przy użyciu uprawnień "Czytnik" w zakresie dostępnej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48ef1-149">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="48ef1-150">Przykład 5. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu identyfikatora aplikacji z przypisaniem roli</span><span class="sxs-lookup"><span data-stu-id="48ef1-150">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="48ef1-151">Tworzy nowy podmiot zabezpieczeń usługi AD dla aplikacji o identyfikatorze aplikacji '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span><span class="sxs-lookup"><span data-stu-id="48ef1-151">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="48ef1-152">Ponieważ nie podano żadnych wartości lub podmiot zabezpieczeń utworzonej usługi `Role` `Scope` nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="48ef1-152">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="48ef1-153">Przykład 6. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="48ef1-153">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="48ef1-154">Pobiera aplikację z identyfikatorem obiektu "3ede3c26-b443-4e0b-9efc-b05e68338dc3" i potoki, które są do polecenia cmdlet programu New-AzADServicePrincipal, w celu utworzenia nowego podmiotu zabezpieczeń usługi AD dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="48ef1-154">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="48ef1-155">Przykład 7. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczeń displayname i hasła</span><span class="sxs-lookup"><span data-stu-id="48ef1-155">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="48ef1-156">Tworzy nową aplikację o nazwie "ServicePrincipalName" i hasłem "StrongPassworld!23" i tworzy podmiot zabezpieczeń usługi na podstawie właśnie utworzonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="48ef1-156">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="48ef1-157">Data rozpoczęcia i data zakończenia zostaną dodane do poświadczeń hasła.</span><span class="sxs-lookup"><span data-stu-id="48ef1-157">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="48ef1-158">Przykład 8. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczeń DisplayName i zwykłego klucza</span><span class="sxs-lookup"><span data-stu-id="48ef1-158">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="48ef1-159">Tworzy nową aplikację o nazwie "ServicePrincipalName" i certifcate "$cert" i tworzy podmiot zabezpieczeń usługi na podstawie właśnie utworzonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="48ef1-159">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="48ef1-160">Data zakończenia zostanie dodana do poświadczeń klucza.</span><span class="sxs-lookup"><span data-stu-id="48ef1-160">The end date is added to key credential.</span></span>

## <span data-ttu-id="48ef1-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48ef1-161">PARAMETERS</span></span>

### <span data-ttu-id="48ef1-162">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="48ef1-162">-ApplicationId</span></span>
<span data-ttu-id="48ef1-163">Unikatowy identyfikator aplikacji podmiotu zabezpieczeń usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="48ef1-163">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="48ef1-164">Po utworzeniu tej właściwości nie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="48ef1-164">Once created this property cannot be changed.</span></span>
<span data-ttu-id="48ef1-165">Jeśli nie zostanie określony identyfikator aplikacji, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="48ef1-165">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="48ef1-166">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="48ef1-166">-ApplicationObject</span></span>
<span data-ttu-id="48ef1-167">Obiekt reprezentujący aplikację, dla której jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-167">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48ef1-168">-CertValue</span><span class="sxs-lookup"><span data-stu-id="48ef1-168">-CertValue</span></span>
<span data-ttu-id="48ef1-169">Wartość typu poświadczeń "asymetrycznego".</span><span class="sxs-lookup"><span data-stu-id="48ef1-169">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="48ef1-170">Reprezentuje certyfikat zakodowany na podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="48ef1-170">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="48ef1-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ef1-171">-DefaultProfile</span></span>
<span data-ttu-id="48ef1-172">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="48ef1-172">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48ef1-173">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="48ef1-173">-DisplayName</span></span>
<span data-ttu-id="48ef1-174">Przyjazna nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-174">The friendly name of the service principal.</span></span> <span data-ttu-id="48ef1-175">Jeśli nazwa wyświetlana nie zostanie podany, ta wartość będzie domyślnie wyświetlana jako "azure-powershell-MM-dd-yyyy-HH-mm-ss", gdzie sufiks jest czasem tworzenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="48ef1-175">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="48ef1-176">-EndDate</span><span class="sxs-lookup"><span data-stu-id="48ef1-176">-EndDate</span></span>
<span data-ttu-id="48ef1-177">Data zakończenia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="48ef1-177">The effective end date of the credential usage.</span></span>
<span data-ttu-id="48ef1-178">Domyślna wartość daty końcowej wynosi jeden rok od dnia dzisiejszego.</span><span class="sxs-lookup"><span data-stu-id="48ef1-178">The default end date value is one year from today.</span></span> <span data-ttu-id="48ef1-179">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę ważności certyfikatu X509 lub wcześniejszą.</span><span class="sxs-lookup"><span data-stu-id="48ef1-179">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="48ef1-180">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="48ef1-180">-KeyCredential</span></span>
<span data-ttu-id="48ef1-181">Zbiór poświadczeń klucza skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="48ef1-181">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48ef1-182">- PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="48ef1-182">-PasswordCredential</span></span>
<span data-ttu-id="48ef1-183">Zbiór poświadczeń hasła skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="48ef1-183">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48ef1-184">— Rola</span><span class="sxs-lookup"><span data-stu-id="48ef1-184">-Role</span></span>
<span data-ttu-id="48ef1-185">Rola podmiotu zabezpieczeń usługi w zakresie.</span><span class="sxs-lookup"><span data-stu-id="48ef1-185">The role that the service principal has over the scope.</span></span> <span data-ttu-id="48ef1-186">Jeśli podano wartość, ale nie podano żadnej wartości, zostanie ona domyślnie dodana do roli `Scope` `Role` `Role` "Współautor".</span><span class="sxs-lookup"><span data-stu-id="48ef1-186">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="48ef1-187">— Zakres</span><span class="sxs-lookup"><span data-stu-id="48ef1-187">-Scope</span></span>
<span data-ttu-id="48ef1-188">Zakres uprawnień podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-188">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="48ef1-189">Jeśli podano wartość, ale nie podano żadnej wartości, zostanie ona domyślnie dodana `Role` `Scope` do `Scope` bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="48ef1-189">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="48ef1-190">- SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="48ef1-190">-SkipAssignment</span></span>
<span data-ttu-id="48ef1-191">Jeśli zostanie ustawiony, pominiesz tworzenie domyślnego przydziału ról dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="48ef1-191">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="48ef1-192">- StartDate</span><span class="sxs-lookup"><span data-stu-id="48ef1-192">-StartDate</span></span>
<span data-ttu-id="48ef1-193">Data rozpoczęcia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="48ef1-193">The effective start date of the credential usage.</span></span>
<span data-ttu-id="48ef1-194">Domyślna wartość daty rozpoczęcia to dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="48ef1-194">The default start date value is today.</span></span> <span data-ttu-id="48ef1-195">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę, od kiedy certyfikat X509 jest prawidłowy, lub później.</span><span class="sxs-lookup"><span data-stu-id="48ef1-195">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="48ef1-196">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48ef1-196">-Confirm</span></span>
<span data-ttu-id="48ef1-197">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48ef1-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48ef1-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ef1-198">-WhatIf</span></span>
<span data-ttu-id="48ef1-199">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48ef1-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48ef1-200">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="48ef1-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48ef1-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ef1-201">CommonParameters</span></span>
<span data-ttu-id="48ef1-202">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ef1-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ef1-203">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48ef1-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ef1-204">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48ef1-204">INPUTS</span></span>

### <span data-ttu-id="48ef1-205">System.Guid</span><span class="sxs-lookup"><span data-stu-id="48ef1-205">System.Guid</span></span>

### <span data-ttu-id="48ef1-206">System.String</span><span class="sxs-lookup"><span data-stu-id="48ef1-206">System.String</span></span>

### <span data-ttu-id="48ef1-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="48ef1-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="48ef1-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="48ef1-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="48ef1-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="48ef1-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="48ef1-210">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="48ef1-210">System.DateTime</span></span>

## <span data-ttu-id="48ef1-211">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="48ef1-211">OUTPUTS</span></span>

### <span data-ttu-id="48ef1-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="48ef1-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="48ef1-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="48ef1-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="48ef1-214">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48ef1-214">NOTES</span></span>
<span data-ttu-id="48ef1-215">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="48ef1-215">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="48ef1-216">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48ef1-216">RELATED LINKS</span></span>

[<span data-ttu-id="48ef1-217">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="48ef1-217">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="48ef1-218">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="48ef1-218">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="48ef1-219">New-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="48ef1-219">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="48ef1-220">Remove-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="48ef1-220">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="48ef1-221">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="48ef1-221">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="48ef1-222">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="48ef1-222">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="48ef1-223">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="48ef1-223">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

