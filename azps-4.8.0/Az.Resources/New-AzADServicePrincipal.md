---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9fc7b3de271188c2f8ebd0be3293892a6fae56e3
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251781"
---
# <span data-ttu-id="be833-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be833-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="be833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be833-102">SYNOPSIS</span></span>
<span data-ttu-id="be833-103">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be833-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="be833-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be833-104">SYNTAX</span></span>

### <span data-ttu-id="be833-105">SimpleParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="be833-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be833-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be833-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be833-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be833-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be833-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="be833-120">DESCRIPTION</span></span>

<span data-ttu-id="be833-121">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be833-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="be833-122">Domyślny zestaw parametrów używa wartości domyślnych dla parametrów, jeśli nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="be833-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="be833-123">Aby uzyskać więcej informacji na temat wartości domyślnych, zobacz opis każdego parametru.</span><span class="sxs-lookup"><span data-stu-id="be833-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="be833-124">To polecenie cmdlet umożliwia przypisanie roli do podmiotu zabezpieczeń usługi za pomocą **parametrów Rola** **i** Zakres.</span><span class="sxs-lookup"><span data-stu-id="be833-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="be833-125">Jeśli oba te czynniki zostaną pominięte, rola współautora zostanie przypisana do podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be833-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="be833-126">Wartości domyślne parametrów **Rola** i **Zakres** są **wartościami współautorów** dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="be833-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="be833-127">Polecenie cmdlet tworzy aplikację i ustawia jej właściwości, jeśli nie podano właściwości ApplicationId.</span><span class="sxs-lookup"><span data-stu-id="be833-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="be833-128">Aby zaktualizować parametry specyficzne dla aplikacji, użyj polecenia cmdlet [Update-AzADApplication.](./update-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="be833-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="be833-129">Po utworzeniu podmiotu zabezpieczeń usługi za pomocą **polecenia New-AzADServicePrincipal** dane wyjściowe zawierają poświadczenia, które należy chronić.</span><span class="sxs-lookup"><span data-stu-id="be833-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="be833-130">Rozważ użycie tożsamości [zarządzanych,](/azure/active-directory/managed-identities-azure-resources/overview) aby uniknąć konieczności używania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="be833-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="be833-131">Domyślnie **new-AzADServicePrincipal** przypisuje rolę [](/azure/role-based-access-control/built-in-roles#contributor) współautora podmiotowi usługi w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="be833-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="be833-132">Aby zmniejszyć ryzyko wystąpienia naruszonego podmiotu zabezpieczeń usługi, przypisz bardziej konkretną rolę i zawęzij zakres do grupy zasobów lub zasobu.</span><span class="sxs-lookup"><span data-stu-id="be833-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="be833-133">Zobacz [Kroki, aby dodać przypisanie roli,](/azure/role-based-access-control/role-assignments-steps) aby uzyskać więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="be833-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="be833-134">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be833-134">EXAMPLES</span></span>

### <span data-ttu-id="be833-135">Przykład 1. Tworzenie podmiotu zabezpieczeń prostej usługi AD</span><span class="sxs-lookup"><span data-stu-id="be833-135">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="be833-136">W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="be833-136">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="be833-137">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="be833-137">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="be833-138">Ponieważ nie podano żadnych wartości dla **roli** lub **zakresu,** do utworzonego podmiotu zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="be833-138">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="be833-139">Przykład 2. Proste utworzenie podmiotu zabezpieczeń usługi AD z określoną rolą i zakresem domyślnym</span><span class="sxs-lookup"><span data-stu-id="be833-139">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="be833-140">W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="be833-140">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="be833-141">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="be833-141">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="be833-142">Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **czytnika** dla bieżącej subskrypcji, ponieważ dla parametru Zakres nie jest podano **żadnej** wartości.</span><span class="sxs-lookup"><span data-stu-id="be833-142">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="be833-143">Przykład 3. Proste tworzenie podmiotu zabezpieczeń usługi AD z określonym zakresem i rolą domyślną</span><span class="sxs-lookup"><span data-stu-id="be833-143">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="be833-144">W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="be833-144">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="be833-145">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="be833-145">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="be833-146">Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **współautora** dla podanego zakresu grupy zasobów, ponieważ dla parametru Rola nie jest podano **żadnej** wartości.</span><span class="sxs-lookup"><span data-stu-id="be833-146">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="be833-147">Przykład 4. Proste tworzenie podmiotu zabezpieczeń usługi AD z określonym zakresem i rolą</span><span class="sxs-lookup"><span data-stu-id="be833-147">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="be833-148">W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone.</span><span class="sxs-lookup"><span data-stu-id="be833-148">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="be833-149">Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="be833-149">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="be833-150">Podmiot zabezpieczeń usługi jest tworzony przy użyciu uprawnień **czytnika** dla zakresu dostępnej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be833-150">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="be833-151">Przykład 5. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu identyfikatora aplikacji z przypisaniem roli</span><span class="sxs-lookup"><span data-stu-id="be833-151">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="be833-152">Poniższy przykład tworzy nowy podmiot zabezpieczeń usługi AD dla aplikacji o identyfikatorze aplikacji "000000000-0000-0000-0000-0000000000000".</span><span class="sxs-lookup"><span data-stu-id="be833-152">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="be833-153">Ponieważ nie podano żadnych wartości dla **roli** lub **zakresu,** do utworzonego podmiotu zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="be833-153">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="be833-154">Przykład 6. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="be833-154">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="be833-155">Poniższy przykład pobiera aplikację z identyfikatorem obiektu "3ede3c26-b443-4e0b-9efc-b05e68338dc3" za pomocą polecenia cmdlet [Get-AzADApplication.](./get-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="be833-155">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="be833-156">Wyniki są potokowe do polecenia cmdlet w celu utworzenia nowego podmiotu zabezpieczeń usługi `New-AzADServicePrincipal` AD dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="be833-156">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="be833-157">Przykład 7. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczeń displayname i hasła</span><span class="sxs-lookup"><span data-stu-id="be833-157">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="be833-158">Poniższy przykład tworzy nową aplikację o nazwie **ServicePrincipalName** i hasłem **strongPassworld!23.**</span><span class="sxs-lookup"><span data-stu-id="be833-158">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="be833-159">Na podstawie utworzonej aplikacji jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be833-159">It creates the service principal based on the created application.</span></span> <span data-ttu-id="be833-160">Data rozpoczęcia i data zakończenia zostaną dodane do poświadczeń hasła.</span><span class="sxs-lookup"><span data-stu-id="be833-160">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="be833-161">Przykład 8. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczeń DisplayName i zwykłego klucza</span><span class="sxs-lookup"><span data-stu-id="be833-161">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="be833-162">W poniższym przykładzie jest podmiot tworzący nową aplikację o nazwie **ServicePrincipalName** i **$cert.** Na podstawie utworzonej aplikacji jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be833-162">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="be833-163">Data zakończenia zostanie dodana do poświadczeń klucza.</span><span class="sxs-lookup"><span data-stu-id="be833-163">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="be833-164">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be833-164">PARAMETERS</span></span>

### <span data-ttu-id="be833-165">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="be833-165">-ApplicationId</span></span>

<span data-ttu-id="be833-166">Unikatowy identyfikator aplikacji dla podmiotu zabezpieczeń usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="be833-166">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="be833-167">Po utworzeniu tej właściwości nie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="be833-167">Once created this property cannot be changed.</span></span> <span data-ttu-id="be833-168">Jeśli nie określono identyfikatora aplikacji dla istniejącej aplikacji, zostanie utworzona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="be833-168">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="be833-169">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="be833-169">-ApplicationObject</span></span>

<span data-ttu-id="be833-170">Obiekt reprezentujący aplikację, dla której jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be833-170">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="be833-171">-CertValue</span><span class="sxs-lookup"><span data-stu-id="be833-171">-CertValue</span></span>

<span data-ttu-id="be833-172">Wartość asymetrycznego typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="be833-172">The value of the asymmetric credential type.</span></span> <span data-ttu-id="be833-173">Reprezentuje certyfikat zakodowany w bazie danych Base64.</span><span class="sxs-lookup"><span data-stu-id="be833-173">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="be833-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be833-174">-DefaultProfile</span></span>

<span data-ttu-id="be833-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be833-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be833-176">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="be833-176">-DisplayName</span></span>

<span data-ttu-id="be833-177">Przyjazna nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be833-177">The friendly name of the service principal.</span></span> <span data-ttu-id="be833-178">Jeśli nazwa wyświetlana nie zostanie podany, ta wartość będzie domyślnie wyświetlana w programie **azure-powershell-MM-dd-yyyy-HH-mm-ss,** gdzie sufiks jest czasem tworzenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="be833-178">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="be833-179">-EndDate</span><span class="sxs-lookup"><span data-stu-id="be833-179">-EndDate</span></span>

<span data-ttu-id="be833-180">Data zakończenia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="be833-180">The effective end date of the credential usage.</span></span> <span data-ttu-id="be833-181">Domyślna wartość daty końcowej wynosi jeden rok od dnia dzisiejszego.</span><span class="sxs-lookup"><span data-stu-id="be833-181">The default end date value is one year from today.</span></span>
<span data-ttu-id="be833-182">W przypadku poświadczeń typu asymetrycznego musi to być ustawione na datę ważności certyfikatu X509 lub wcześniejszą.</span><span class="sxs-lookup"><span data-stu-id="be833-182">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="be833-183">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="be833-183">-KeyCredential</span></span>

<span data-ttu-id="be833-184">Zbiór poświadczeń klucza skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="be833-184">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="be833-185">- PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="be833-185">-PasswordCredential</span></span>

<span data-ttu-id="be833-186">Zbiór poświadczeń hasła skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="be833-186">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="be833-187">— Rola</span><span class="sxs-lookup"><span data-stu-id="be833-187">-Role</span></span>

<span data-ttu-id="be833-188">Rola podmiotu zabezpieczeń usługi w zakresie.</span><span class="sxs-lookup"><span data-stu-id="be833-188">The role that the service principal has over the scope.</span></span> <span data-ttu-id="be833-189">Jeśli nie podano żadnej wartości, **rola będzie** domyślnie pełnić rolę **współautora.**</span><span class="sxs-lookup"><span data-stu-id="be833-189">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="be833-190">— Zakres</span><span class="sxs-lookup"><span data-stu-id="be833-190">-Scope</span></span>

<span data-ttu-id="be833-191">Zakres uprawnień podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be833-191">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="be833-192">Jeśli nie podano żadnej wartości, **zakres jest** domyślnie domyślny dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="be833-192">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="be833-193">- SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="be833-193">-SkipAssignment</span></span>

<span data-ttu-id="be833-194">W przypadku ustawienia pomiń tworzenie domyślnego przydziału ról dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be833-194">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="be833-195">- StartDate</span><span class="sxs-lookup"><span data-stu-id="be833-195">-StartDate</span></span>

<span data-ttu-id="be833-196">Data rozpoczęcia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="be833-196">The effective start date of the credential usage.</span></span> <span data-ttu-id="be833-197">Domyślna wartość daty rozpoczęcia to dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="be833-197">The default start date value is today.</span></span> <span data-ttu-id="be833-198">W przypadku poświadczeń typu asymetrycznego musi on być ustawiony na datę ważności certyfikatu X509 lub późniejszą.</span><span class="sxs-lookup"><span data-stu-id="be833-198">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="be833-199">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be833-199">-Confirm</span></span>

<span data-ttu-id="be833-200">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be833-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be833-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be833-201">-WhatIf</span></span>

<span data-ttu-id="be833-202">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be833-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be833-203">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be833-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be833-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be833-204">CommonParameters</span></span>
<span data-ttu-id="be833-205">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be833-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be833-206">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="be833-206">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="be833-207">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be833-207">INPUTS</span></span>

### <span data-ttu-id="be833-208">System.Guid</span><span class="sxs-lookup"><span data-stu-id="be833-208">System.Guid</span></span>

### <span data-ttu-id="be833-209">System.String</span><span class="sxs-lookup"><span data-stu-id="be833-209">System.String</span></span>

### <span data-ttu-id="be833-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="be833-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="be833-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="be833-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="be833-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="be833-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="be833-213">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="be833-213">System.DateTime</span></span>

## <span data-ttu-id="be833-214">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be833-214">OUTPUTS</span></span>

### <span data-ttu-id="be833-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be833-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="be833-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="be833-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="be833-217">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be833-217">NOTES</span></span>

<span data-ttu-id="be833-218">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="be833-218">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="be833-219">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be833-219">RELATED LINKS</span></span>

[<span data-ttu-id="be833-220">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be833-220">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="be833-221">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be833-221">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="be833-222">New-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="be833-222">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="be833-223">Remove-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="be833-223">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="be833-224">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="be833-224">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="be833-225">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="be833-225">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="be833-226">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="be833-226">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)
