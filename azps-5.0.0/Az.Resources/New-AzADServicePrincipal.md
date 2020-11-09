---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/05/2020
ms.locfileid: "94319471"
---
# <span data-ttu-id="6617f-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6617f-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="6617f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6617f-102">SYNOPSIS</span></span>
<span data-ttu-id="6617f-103">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6617f-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="6617f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6617f-104">SYNTAX</span></span>

### <span data-ttu-id="6617f-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6617f-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6617f-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6617f-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6617f-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617f-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6617f-120">Opis</span><span class="sxs-lookup"><span data-stu-id="6617f-120">DESCRIPTION</span></span>

<span data-ttu-id="6617f-121">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6617f-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="6617f-122">W domyślnym ustawieniu parametrów są używane wartości domyślne parametrów, o ile nie zostały one podane.</span><span class="sxs-lookup"><span data-stu-id="6617f-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="6617f-123">Aby uzyskać więcej informacji na temat wartości domyślnych, zobacz opisy poszczególnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="6617f-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="6617f-124">To polecenie cmdlet umożliwia przypisanie roli do podmiotu zabezpieczeń przy użyciu parametrów **rola** i **zakres** .</span><span class="sxs-lookup"><span data-stu-id="6617f-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="6617f-125">Jeśli oba zostaną pominięte, rola współautora zostanie przypisana do podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="6617f-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="6617f-126">Domyślne wartości parametrów **rola** i **zakres** są **współautorami** dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6617f-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="6617f-127">Polecenie cmdlet tworzy aplikację i ustawia jej właściwości, jeśli nie jest podany identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6617f-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="6617f-128">Aby zaktualizować parametry specyficzne dla aplikacji, użyj polecenia cmdlet [Update-AzADApplication](./update-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="6617f-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="6617f-129">Podczas tworzenia podmiotu usługi za pomocą polecenia **New-AzADServicePrincipal** dane wyjściowe będą zawierały poświadczenia, które należy chronić.</span><span class="sxs-lookup"><span data-stu-id="6617f-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="6617f-130">Upewnij się, że nie są uwzględniane te poświadczenia w kodzie, lub sprawdź poświadczenia w kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="6617f-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="6617f-131">Alternatywne rozwiązanie polega na użyciu [tożsamości zarządzanych](/azure/active-directory/managed-identities-azure-resources/overview) , aby uniknąć konieczności korzystania z poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="6617f-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="6617f-132">Domyślnie polecenie **New-AzADServicePrincipal** przypisuje rolę [współautora](/azure/role-based-access-control/built-in-roles#contributor) głównemu usługi w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6617f-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="6617f-133">Aby zmniejszyć ryzyko naruszenia zabezpieczeń usługi, należy przypisać bardziej określoną rolę i zawęzić jej zakres do zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6617f-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="6617f-134">Aby uzyskać więcej informacji [, zobacz instrukcje dodawania zadania roli](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="6617f-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="6617f-135">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6617f-135">EXAMPLES</span></span>

### <span data-ttu-id="6617f-136">Przykład 1: proste tworzenie podmiotu zabezpieczeń usługi reklamy</span><span class="sxs-lookup"><span data-stu-id="6617f-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="6617f-137">W poniższym przykładzie jest tworzony podmiot zabezpieczeń usługi AD, który używa wartości domyślnych dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="6617f-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="6617f-138">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="6617f-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="6617f-139">Ponieważ dla **roli** lub **zakresu** nie są podane żadne wartości, utworzonym podmiotowi zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6617f-139">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="6617f-140">Przykład 2: proste tworzenie podmiotów głównych usługi REKLAMowej z określoną rolą i zakresem domyślnym</span><span class="sxs-lookup"><span data-stu-id="6617f-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="6617f-141">W poniższym przykładzie następuje utworzenie podmiotu zabezpieczeń usługi AD przy użyciu wartości domyślnych dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="6617f-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="6617f-142">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="6617f-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="6617f-143">Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **czytelnika** dla bieżącej subskrypcji, ponieważ parametr **zakres** nie ma wartości.</span><span class="sxs-lookup"><span data-stu-id="6617f-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="6617f-144">Przykład 3: proste tworzenie głównych usług REKLAMowych z określonym zakresem i rolą domyślną</span><span class="sxs-lookup"><span data-stu-id="6617f-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="6617f-145">W poniższym przykładzie następuje utworzenie podmiotu zabezpieczeń usługi AD przy użyciu wartości domyślnych dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="6617f-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="6617f-146">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="6617f-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="6617f-147">Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **współautorów** dla podanego zakresu grupy zasobów, ponieważ nie jest podana wartość parametru **role** .</span><span class="sxs-lookup"><span data-stu-id="6617f-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="6617f-148">Przykład 4: proste tworzenie głównych usług REKLAMowych z określonym zakresem i rolą</span><span class="sxs-lookup"><span data-stu-id="6617f-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="6617f-149">W poniższym przykładzie następuje utworzenie podmiotu zabezpieczeń usługi AD przy użyciu wartości domyślnych dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="6617f-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="6617f-150">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="6617f-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="6617f-151">Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **czytelnika** dla podanego zakresu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6617f-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="6617f-152">Przykład 5: Tworzenie nowego podmiotu usługi reklamy przy użyciu identyfikatora aplikacji z przypisaniem roli</span><span class="sxs-lookup"><span data-stu-id="6617f-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="6617f-153">W poniższym przykładzie jest tworzony nowy podmiot zabezpieczeń usługi reklamy dla aplikacji z IDENTYFIKATORem aplikacji ' 00000000-0000-0000-0000-000000000000 '.</span><span class="sxs-lookup"><span data-stu-id="6617f-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="6617f-154">Ponieważ dla **roli** lub **zakresu** nie są podane żadne wartości, utworzonym podmiotowi zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6617f-154">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="6617f-155">Przykład 6: Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="6617f-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="6617f-156">Poniższy przykład pobiera aplikację z IDENTYFIKATORem obiektu 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' przy użyciu polecenia cmdlet [Get-AzADApplication](./get-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="6617f-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="6617f-157">Wyniki są potoku do `New-AzADServicePrincipal` polecenia cmdlet w celu utworzenia nowego podmiotu zabezpieczeń usługi AD dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6617f-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="6617f-158">Przykład 7: Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczenia DisplayName i hasła</span><span class="sxs-lookup"><span data-stu-id="6617f-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="6617f-159">W poniższym przykładzie jest tworzona nowa aplikacja z nazwą **ServicePrincipalName** i hasłem **StrongPassworld! 23**.</span><span class="sxs-lookup"><span data-stu-id="6617f-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="6617f-160">Tworzy on nazwę główną usługi na podstawie utworzonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6617f-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="6617f-161">Data rozpoczęcia i Data zakończenia zostaną dodane do poświadczenia hasła.</span><span class="sxs-lookup"><span data-stu-id="6617f-161">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="6617f-162">Przykład 8: Tworzenie nowego podmiotu usługi reklamy przy użyciu poświadczenia DisplayName i zwykłego klucza</span><span class="sxs-lookup"><span data-stu-id="6617f-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="6617f-163">W poniższym przykładzie jest tworzona nowa aplikacja z nazwą **ServicePrincipalName** i certyfikatem **$CERT**. Tworzy on nazwę główną usługi na podstawie utworzonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6617f-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="6617f-164">Data zakończenia zostanie dodana do poświadczenia klucza.</span><span class="sxs-lookup"><span data-stu-id="6617f-164">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="6617f-165">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6617f-165">PARAMETERS</span></span>

### <span data-ttu-id="6617f-166">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="6617f-166">-ApplicationId</span></span>

<span data-ttu-id="6617f-167">Unikatowy identyfikator aplikacji dla podmiotu zabezpieczeń usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="6617f-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="6617f-168">Po utworzeniu tej właściwości nie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="6617f-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="6617f-169">Jeśli nie określono identyfikatora aplikacji dla istniejącej aplikacji, zostanie utworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="6617f-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="6617f-170">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="6617f-170">-ApplicationObject</span></span>

<span data-ttu-id="6617f-171">Obiekt reprezentujący aplikację, dla której jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="6617f-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="6617f-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="6617f-172">-CertValue</span></span>

<span data-ttu-id="6617f-173">Wartość typu poświadczeń asymetrycznych.</span><span class="sxs-lookup"><span data-stu-id="6617f-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="6617f-174">Reprezentuje certyfikat kodowany algorytmem Base64.</span><span class="sxs-lookup"><span data-stu-id="6617f-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="6617f-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6617f-175">-DefaultProfile</span></span>

<span data-ttu-id="6617f-176">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6617f-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6617f-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6617f-177">-DisplayName</span></span>

<span data-ttu-id="6617f-178">Przyjazna nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="6617f-178">The friendly name of the service principal.</span></span> <span data-ttu-id="6617f-179">Jeśli nie podano nazwy wyświetlanej, ta wartość będzie domyślnie równa **platformie Azure-PowerShell-mm-dd-rrrr-hh-mm-SS** , gdzie sufiks jest momentem utworzenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6617f-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="6617f-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="6617f-180">-EndDate</span></span>

<span data-ttu-id="6617f-181">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="6617f-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="6617f-182">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="6617f-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="6617f-183">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="6617f-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="6617f-184">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="6617f-184">-KeyCredential</span></span>

<span data-ttu-id="6617f-185">Kolekcja kluczowych poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="6617f-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="6617f-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="6617f-186">-PasswordCredential</span></span>

<span data-ttu-id="6617f-187">Kolekcja poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="6617f-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="6617f-188">-Rola</span><span class="sxs-lookup"><span data-stu-id="6617f-188">-Role</span></span>

<span data-ttu-id="6617f-189">Rola podmiotu zabezpieczeń usługi w zakresie.</span><span class="sxs-lookup"><span data-stu-id="6617f-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="6617f-190">Jeśli nie podano żadnej wartości, rola jest domyślnie ustawiana przez **rolę** **współautora** .</span><span class="sxs-lookup"><span data-stu-id="6617f-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="6617f-191">-Zakres</span><span class="sxs-lookup"><span data-stu-id="6617f-191">-Scope</span></span>

<span data-ttu-id="6617f-192">Zakres, dla którego główna usługa ma uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="6617f-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="6617f-193">Jeśli nie podano żadnej wartości, to **zakresem** domyślnym jest bieżący abonament.</span><span class="sxs-lookup"><span data-stu-id="6617f-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="6617f-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="6617f-194">-SkipAssignment</span></span>

<span data-ttu-id="6617f-195">Jeśli jest ustawiona, Pomiń tworzenie domyślnego zadania roli dla podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="6617f-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="6617f-196">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="6617f-196">-StartDate</span></span>

<span data-ttu-id="6617f-197">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="6617f-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="6617f-198">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="6617f-198">The default start date value is today.</span></span> <span data-ttu-id="6617f-199">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="6617f-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="6617f-200">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6617f-200">-Confirm</span></span>

<span data-ttu-id="6617f-201">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6617f-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6617f-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6617f-202">-WhatIf</span></span>

<span data-ttu-id="6617f-203">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6617f-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6617f-204">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6617f-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6617f-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6617f-205">CommonParameters</span></span>
<span data-ttu-id="6617f-206">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6617f-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6617f-207">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="6617f-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="6617f-208">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6617f-208">INPUTS</span></span>

### <span data-ttu-id="6617f-209">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6617f-209">System.Guid</span></span>

### <span data-ttu-id="6617f-210">System. String</span><span class="sxs-lookup"><span data-stu-id="6617f-210">System.String</span></span>

### <span data-ttu-id="6617f-211">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6617f-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="6617f-212">Microsoft. Azure. Commands. pozycji. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="6617f-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="6617f-213">Microsoft. Azure. Commands. pozycji. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="6617f-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="6617f-214">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="6617f-214">System.DateTime</span></span>

## <span data-ttu-id="6617f-215">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6617f-215">OUTPUTS</span></span>

### <span data-ttu-id="6617f-216">Microsoft. Azure. Commands. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6617f-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="6617f-217">Microsoft. Azure. Commands. resources. models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="6617f-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="6617f-218">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6617f-218">NOTES</span></span>

<span data-ttu-id="6617f-219">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="6617f-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6617f-220">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6617f-220">RELATED LINKS</span></span>

[<span data-ttu-id="6617f-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6617f-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="6617f-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6617f-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="6617f-223">Nowe — AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6617f-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="6617f-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6617f-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="6617f-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6617f-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="6617f-226">Nowe — AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6617f-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="6617f-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6617f-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)