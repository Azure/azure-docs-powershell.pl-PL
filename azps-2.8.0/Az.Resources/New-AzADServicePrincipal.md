---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9db3e3d0fcb52869a53b4bd2b76603d2935c4dd0
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/05/2020
ms.locfileid: "93899484"
---
# <span data-ttu-id="b1d02-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b1d02-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="b1d02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1d02-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d02-103">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1d02-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="b1d02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1d02-104">SYNTAX</span></span>

### <span data-ttu-id="b1d02-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b1d02-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1d02-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1d02-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d02-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d02-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1d02-121">Opis</span><span class="sxs-lookup"><span data-stu-id="b1d02-121">DESCRIPTION</span></span>
<span data-ttu-id="b1d02-122">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1d02-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="b1d02-123">W przypadku domyślnego zestawu parametrów są używane wartości domyślne parametrów, jeśli użytkownik nie udostępnił tego parametru.</span><span class="sxs-lookup"><span data-stu-id="b1d02-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="b1d02-124">Aby uzyskać więcej informacji na temat używanych wartości domyślnych, zapoznaj się z opisem podanych niżej parametrów.</span><span class="sxs-lookup"><span data-stu-id="b1d02-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="b1d02-125">To polecenie cmdlet umożliwia przypisywanie roli do podmiotu zabezpieczeń usługi z `Role` `Scope` parametrami i parametrami. Jeśli nie podano żadnego z tych parametrów, żadna rola nie zostanie przypisana do podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="b1d02-126">Domyślne wartości `Role` parametrów and są następujące `Scope` : "Współautor" oraz bieżący abonament ( _Uwaga_ : wartości domyślne są używane tylko wtedy, gdy użytkownik podaje wartość dla jednego z dwóch parametrów, ale nie z drugiej).</span><span class="sxs-lookup"><span data-stu-id="b1d02-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="b1d02-127">Polecenie cmdlet powoduje również niejawne utworzenie aplikacji i ustawienie jej właściwości (Jeśli identyfikator aplikacji nie jest dostarczany).</span><span class="sxs-lookup"><span data-stu-id="b1d02-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="b1d02-128">W celu zaktualizowania parametrów specyficznych dla aplikacji użyj polecenia cmdlet Set-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="b1d02-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="b1d02-129">Podczas tworzenia podmiotu usługi za pomocą polecenia **New-AzADServicePrincipal** dane wyjściowe będą zawierały poświadczenia, które należy chronić.</span><span class="sxs-lookup"><span data-stu-id="b1d02-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="b1d02-130">Upewnij się, że nie są uwzględniane te poświadczenia w kodzie, lub sprawdź poświadczenia w kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="b1d02-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="b1d02-131">Alternatywne rozwiązanie polega na użyciu [tożsamości zarządzanych](/azure/active-directory/managed-identities-azure-resources/overview) , aby uniknąć konieczności korzystania z poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b1d02-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="b1d02-132">Domyślnie polecenie **New-AzADServicePrincipal** przypisuje rolę [współautora](/azure/role-based-access-control/built-in-roles#contributor) głównemu usługi w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b1d02-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="b1d02-133">Aby zmniejszyć ryzyko naruszenia zabezpieczeń usługi, należy przypisać bardziej określoną rolę i zawęzić jej zakres do zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1d02-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="b1d02-134">Aby uzyskać więcej informacji [, zobacz instrukcje dodawania zadania roli](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="b1d02-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="b1d02-135">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1d02-135">EXAMPLES</span></span>

### <span data-ttu-id="b1d02-136">Przykład 1 — prosta operacja tworzenia podmiotu zabezpieczeń usługi REKLAMowej</span><span class="sxs-lookup"><span data-stu-id="b1d02-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="b1d02-137">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="b1d02-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="b1d02-138">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b1d02-139">Ponieważ nie zostały podane żadne wartości `Role` , ani też `Scope` utworzony podmiot zabezpieczeń usługi nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="b1d02-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="b1d02-140">Przykład 2 — proste tworzenie podmiotów głównych usługi REKLAMowej z określoną rolą i zakresem domyślnym</span><span class="sxs-lookup"><span data-stu-id="b1d02-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="b1d02-141">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="b1d02-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b1d02-142">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b1d02-143">Podmiot zabezpieczeń usługi został utworzony za pomocą uprawnień czytelnika w bieżącym abonamentzie (ponieważ nie podano wartości dla tego `Scope` parametru).</span><span class="sxs-lookup"><span data-stu-id="b1d02-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="b1d02-144">Przykład 3 — prosta główna usługa reklamy z określonym zakresem i rolą domyślną</span><span class="sxs-lookup"><span data-stu-id="b1d02-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="b1d02-145">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="b1d02-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b1d02-146">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b1d02-147">Podmiot zabezpieczeń usługi został utworzony za pomocą uprawnień "współautora" (ponieważ nie podano wartości `Role` parametru) w zakresie podanego zakresu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1d02-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="b1d02-148">Przykład 4 — prosta główna usługa reklamy z określonym zakresem i rolą</span><span class="sxs-lookup"><span data-stu-id="b1d02-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="b1d02-149">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="b1d02-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b1d02-150">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b1d02-151">Podmiot zabezpieczeń usługi został utworzony z uprawnieniami "czytelnik" w udostępnionym zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1d02-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="b1d02-152">Przykład 5 — Utwórz nowy podmiot zabezpieczeń usługi reklamy przy użyciu identyfikatora aplikacji z przypisaniem roli</span><span class="sxs-lookup"><span data-stu-id="b1d02-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="b1d02-153">Tworzy nowy podmiot zabezpieczeń usługi reklamy dla aplikacji z identyfikatorem aplikacji "34a28ad2-DEC4-4a41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="b1d02-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="b1d02-154">Ponieważ nie zostały podane żadne wartości `Role` , ani też `Scope` utworzony podmiot zabezpieczeń usługi nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="b1d02-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="b1d02-155">Przykład 6 — Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="b1d02-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="b1d02-156">Pobiera aplikację o identyfikatorze obiektu "3ede3c26-B443-4e0b-9efc-b05e68338dc3" i potokach, które są poleceniami cmdlet New-AzADServicePrincipal, aby utworzyć nowy podmiot zabezpieczeń usługi AD dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b1d02-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="b1d02-157">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1d02-157">PARAMETERS</span></span>

### <span data-ttu-id="b1d02-158">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="b1d02-158">-ApplicationId</span></span>
<span data-ttu-id="b1d02-159">Unikatowy identyfikator aplikacji dla podmiotu zabezpieczeń usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="b1d02-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="b1d02-160">Po utworzeniu tej właściwości nie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="b1d02-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="b1d02-161">Jeśli nie podano identyfikatora aplikacji, zostanie on wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="b1d02-161">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="b1d02-162">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="b1d02-162">-ApplicationObject</span></span>
<span data-ttu-id="b1d02-163">Obiekt reprezentujący aplikację, dla której jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-163">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d02-164">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b1d02-164">-CertValue</span></span>
<span data-ttu-id="b1d02-165">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b1d02-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b1d02-166">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="b1d02-166">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="b1d02-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d02-167">-DefaultProfile</span></span>
<span data-ttu-id="b1d02-168">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b1d02-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1d02-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b1d02-169">-DisplayName</span></span>
<span data-ttu-id="b1d02-170">Przyjazna nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-170">The friendly name of the service principal.</span></span> <span data-ttu-id="b1d02-171">Jeśli nie podano nazwy wyświetlanej, ta wartość będzie domyślnie równa "Azure-PowerShell-MM-DD-RRRR-HH-mm-SS", gdzie sufiks jest momentem utworzenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b1d02-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="b1d02-172">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b1d02-172">-EndDate</span></span>
<span data-ttu-id="b1d02-173">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b1d02-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b1d02-174">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="b1d02-174">The default end date value is one year from today.</span></span> <span data-ttu-id="b1d02-175">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="b1d02-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b1d02-176">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="b1d02-176">-KeyCredential</span></span>
<span data-ttu-id="b1d02-177">Kolekcja kluczowych poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="b1d02-177">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="b1d02-178">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="b1d02-178">-PasswordCredential</span></span>
<span data-ttu-id="b1d02-179">Kolekcja poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="b1d02-179">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="b1d02-180">-Rola</span><span class="sxs-lookup"><span data-stu-id="b1d02-180">-Role</span></span>
<span data-ttu-id="b1d02-181">Rola podmiotu zabezpieczeń usługi w zakresie.</span><span class="sxs-lookup"><span data-stu-id="b1d02-181">The role that the service principal has over the scope.</span></span> <span data-ttu-id="b1d02-182">Jeśli wartość `Scope` jest podana, ale nie jest podana wartość `Role` , domyślnie zostanie wykorzystana `Role` rola współautora.</span><span class="sxs-lookup"><span data-stu-id="b1d02-182">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="b1d02-183">-Zakres</span><span class="sxs-lookup"><span data-stu-id="b1d02-183">-Scope</span></span>
<span data-ttu-id="b1d02-184">Zakres, dla którego główna usługa ma uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="b1d02-184">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="b1d02-185">Jeśli wartość `Role` jest podana, ale nie jest podana wartość `Scope` , domyślnie zostanie wykorzystana `Scope` bieżąca subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="b1d02-185">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="b1d02-186">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="b1d02-186">-SkipAssignment</span></span>
<span data-ttu-id="b1d02-187">Jeśli zostanie ustawiona, spowoduje to Pominięcie tworzenia domyślnego zadania roli dla podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="b1d02-187">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="b1d02-188">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="b1d02-188">-StartDate</span></span>
<span data-ttu-id="b1d02-189">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b1d02-189">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b1d02-190">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="b1d02-190">The default start date value is today.</span></span> <span data-ttu-id="b1d02-191">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="b1d02-191">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b1d02-192">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1d02-192">-Confirm</span></span>
<span data-ttu-id="b1d02-193">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1d02-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1d02-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1d02-194">-WhatIf</span></span>
<span data-ttu-id="b1d02-195">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1d02-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1d02-196">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1d02-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1d02-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d02-197">CommonParameters</span></span>
<span data-ttu-id="b1d02-198">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d02-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d02-199">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d02-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d02-200">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1d02-200">INPUTS</span></span>

### <span data-ttu-id="b1d02-201">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b1d02-201">System.Guid</span></span>

### <span data-ttu-id="b1d02-202">System. String</span><span class="sxs-lookup"><span data-stu-id="b1d02-202">System.String</span></span>

### <span data-ttu-id="b1d02-203">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b1d02-203">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="b1d02-204">Microsoft. Azure. Commands. pozycji. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="b1d02-204">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="b1d02-205">Microsoft. Azure. Commands. pozycji. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="b1d02-205">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="b1d02-206">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="b1d02-206">System.DateTime</span></span>

## <span data-ttu-id="b1d02-207">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1d02-207">OUTPUTS</span></span>

### <span data-ttu-id="b1d02-208">Microsoft. Azure. Commands. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b1d02-208">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="b1d02-209">Microsoft. Azure. Commands. resources. models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="b1d02-209">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="b1d02-210">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1d02-210">NOTES</span></span>
<span data-ttu-id="b1d02-211">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="b1d02-211">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b1d02-212">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1d02-212">RELATED LINKS</span></span>

[<span data-ttu-id="b1d02-213">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b1d02-213">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="b1d02-214">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b1d02-214">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="b1d02-215">Nowe — AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b1d02-215">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="b1d02-216">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b1d02-216">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="b1d02-217">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b1d02-217">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="b1d02-218">Nowe — AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b1d02-218">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="b1d02-219">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b1d02-219">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

