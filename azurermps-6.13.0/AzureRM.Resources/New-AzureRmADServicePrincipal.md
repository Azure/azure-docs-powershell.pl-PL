---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 50f4a277461e81e26d1e553ad24f817415d5b267
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716923"
---
# <span data-ttu-id="a30c2-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a30c2-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="a30c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a30c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a30c2-103">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a30c2-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a30c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a30c2-104">SYNTAX</span></span>

### <span data-ttu-id="a30c2-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a30c2-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a30c2-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a30c2-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a30c2-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a30c2-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a30c2-121">Opis</span><span class="sxs-lookup"><span data-stu-id="a30c2-121">DESCRIPTION</span></span>
<span data-ttu-id="a30c2-122">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a30c2-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="a30c2-123">W przypadku domyślnego zestawu parametrów są używane wartości domyślne parametrów, jeśli użytkownik nie udostępnił tego parametru.</span><span class="sxs-lookup"><span data-stu-id="a30c2-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="a30c2-124">Aby uzyskać więcej informacji na temat używanych wartości domyślnych, zapoznaj się z opisem podanych niżej parametrów.</span><span class="sxs-lookup"><span data-stu-id="a30c2-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="a30c2-125">To polecenie cmdlet umożliwia przypisywanie roli do podmiotu zabezpieczeń usługi z `Role` `Scope` parametrami i parametrami. Jeśli nie podano żadnego z tych parametrów, żadna rola nie zostanie przypisana do podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="a30c2-126">Domyślne wartości `Role` parametrów and są następujące `Scope` : "Współautor" oraz bieżący abonament ( _Uwaga_ : wartości domyślne są używane tylko wtedy, gdy użytkownik podaje wartość dla jednego z dwóch parametrów, ale nie z drugiej).</span><span class="sxs-lookup"><span data-stu-id="a30c2-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="a30c2-127">Polecenie cmdlet powoduje również niejawne utworzenie aplikacji i ustawienie jej właściwości (Jeśli identyfikator aplikacji nie jest dostarczany).</span><span class="sxs-lookup"><span data-stu-id="a30c2-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="a30c2-128">W celu zaktualizowania parametrów specyficznych dla aplikacji użyj polecenia cmdlet Set-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="a30c2-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="a30c2-129">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a30c2-129">EXAMPLES</span></span>

### <span data-ttu-id="a30c2-130">Przykład 1 — prosta operacja tworzenia podmiotu zabezpieczeń usługi REKLAMowej</span><span class="sxs-lookup"><span data-stu-id="a30c2-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="a30c2-131">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="a30c2-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="a30c2-132">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a30c2-133">Ponieważ nie zostały podane żadne wartości `Role` , ani też `Scope` utworzony podmiot zabezpieczeń usługi nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="a30c2-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="a30c2-134">Przykład 2 — proste tworzenie podmiotów głównych usługi REKLAMowej z określoną rolą i zakresem domyślnym</span><span class="sxs-lookup"><span data-stu-id="a30c2-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="a30c2-135">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="a30c2-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a30c2-136">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a30c2-137">Podmiot zabezpieczeń usługi został utworzony za pomocą uprawnień czytelnika w bieżącym abonamentzie (ponieważ nie podano wartości dla tego `Scope` parametru).</span><span class="sxs-lookup"><span data-stu-id="a30c2-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="a30c2-138">Przykład 3 — prosta główna usługa reklamy z określonym zakresem i rolą domyślną</span><span class="sxs-lookup"><span data-stu-id="a30c2-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="a30c2-139">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="a30c2-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a30c2-140">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a30c2-141">Podmiot zabezpieczeń usługi został utworzony za pomocą uprawnień "współautora" (ponieważ nie podano wartości `Role` parametru) w zakresie podanego zakresu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a30c2-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="a30c2-142">Przykład 4 — prosta główna usługa reklamy z określonym zakresem i rolą</span><span class="sxs-lookup"><span data-stu-id="a30c2-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="a30c2-143">Powyższe polecenie tworzy podmiot zabezpieczeń usługi AD, używając wartości domyślnych dla parametrów, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="a30c2-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a30c2-144">Ponieważ identyfikator aplikacji nie został podany, utworzono aplikację dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a30c2-145">Podmiot zabezpieczeń usługi został utworzony z uprawnieniami "czytelnik" w udostępnionym zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a30c2-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="a30c2-146">Przykład 5 — Utwórz nowy podmiot zabezpieczeń usługi reklamy przy użyciu identyfikatora aplikacji z przypisaniem roli</span><span class="sxs-lookup"><span data-stu-id="a30c2-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="a30c2-147">Tworzy nowy podmiot zabezpieczeń usługi reklamy dla aplikacji z identyfikatorem aplikacji "34a28ad2-DEC4-4a41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="a30c2-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="a30c2-148">Ponieważ nie zostały podane żadne wartości `Role` , ani też `Scope` utworzony podmiot zabezpieczeń usługi nie ma żadnych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="a30c2-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="a30c2-149">Przykład 6 — Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="a30c2-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="a30c2-150">Pobiera aplikację o identyfikatorze obiektu "3ede3c26-B443-4e0b-9efc-b05e68338dc3" i potokach, które są poleceniami cmdlet New-AzureRmADServicePrincipal, aby utworzyć nowy podmiot zabezpieczeń usługi AD dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a30c2-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="a30c2-151">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a30c2-151">PARAMETERS</span></span>

### <span data-ttu-id="a30c2-152">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="a30c2-152">-ApplicationId</span></span>
<span data-ttu-id="a30c2-153">Unikatowy identyfikator aplikacji dla podmiotu zabezpieczeń usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="a30c2-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="a30c2-154">Po utworzeniu tej właściwości nie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="a30c2-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="a30c2-155">Jeśli nie podano identyfikatora aplikacji, zostanie on wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="a30c2-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="a30c2-156">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="a30c2-156">-ApplicationObject</span></span>
<span data-ttu-id="a30c2-157">Obiekt reprezentujący aplikację, dla której jest tworzony podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-157">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="a30c2-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a30c2-158">-CertValue</span></span>
<span data-ttu-id="a30c2-159">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a30c2-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a30c2-160">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="a30c2-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="a30c2-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30c2-161">-DefaultProfile</span></span>
<span data-ttu-id="a30c2-162">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a30c2-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a30c2-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a30c2-163">-DisplayName</span></span>
<span data-ttu-id="a30c2-164">Przyjazna nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-164">The friendly name of the service principal.</span></span> <span data-ttu-id="a30c2-165">Jeśli nie podano nazwy wyświetlanej, ta wartość będzie domyślnie równa "Azure-PowerShell-MM-DD-RRRR-HH-mm-SS", gdzie sufiks jest momentem utworzenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a30c2-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="a30c2-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a30c2-166">-EndDate</span></span>
<span data-ttu-id="a30c2-167">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a30c2-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a30c2-168">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="a30c2-168">The default end date value is one year from today.</span></span> <span data-ttu-id="a30c2-169">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="a30c2-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a30c2-170">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="a30c2-170">-KeyCredential</span></span>
<span data-ttu-id="a30c2-171">Kolekcja kluczowych poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="a30c2-171">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="a30c2-172">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="a30c2-172">-Password</span></span>
<span data-ttu-id="a30c2-173">Hasło, które ma zostać skojarzone z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="a30c2-174">Jeśli hasło nie zostanie podane, jako hasło zostanie wygenerowana Losowa identyfikator GUID.</span><span class="sxs-lookup"><span data-stu-id="a30c2-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

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

### <span data-ttu-id="a30c2-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="a30c2-175">-PasswordCredential</span></span>
<span data-ttu-id="a30c2-176">Kolekcja poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="a30c2-176">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="a30c2-177">-Rola</span><span class="sxs-lookup"><span data-stu-id="a30c2-177">-Role</span></span>
<span data-ttu-id="a30c2-178">Rola podmiotu zabezpieczeń usługi w zakresie.</span><span class="sxs-lookup"><span data-stu-id="a30c2-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="a30c2-179">Jeśli wartość `Scope` jest podana, ale nie jest podana wartość `Role` , domyślnie zostanie wykorzystana `Role` rola współautora.</span><span class="sxs-lookup"><span data-stu-id="a30c2-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="a30c2-180">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a30c2-180">-Scope</span></span>
<span data-ttu-id="a30c2-181">Zakres, dla którego główna usługa ma uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="a30c2-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="a30c2-182">Jeśli wartość `Role` jest podana, ale nie jest podana wartość `Scope` , domyślnie zostanie wykorzystana `Scope` bieżąca subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="a30c2-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="a30c2-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="a30c2-183">-SkipAssignment</span></span>
<span data-ttu-id="a30c2-184">Jeśli zostanie ustawiona, spowoduje to Pominięcie tworzenia domyślnego zadania roli dla podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="a30c2-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="a30c2-185">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="a30c2-185">-StartDate</span></span>
<span data-ttu-id="a30c2-186">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a30c2-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a30c2-187">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="a30c2-187">The default start date value is today.</span></span> <span data-ttu-id="a30c2-188">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="a30c2-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a30c2-189">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a30c2-189">-Confirm</span></span>
<span data-ttu-id="a30c2-190">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a30c2-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a30c2-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a30c2-191">-WhatIf</span></span>
<span data-ttu-id="a30c2-192">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a30c2-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a30c2-193">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a30c2-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a30c2-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30c2-194">CommonParameters</span></span>
<span data-ttu-id="a30c2-195">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a30c2-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30c2-196">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a30c2-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30c2-197">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a30c2-197">INPUTS</span></span>

### <span data-ttu-id="a30c2-198">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a30c2-198">System.Guid</span></span>

### <span data-ttu-id="a30c2-199">System. String</span><span class="sxs-lookup"><span data-stu-id="a30c2-199">System.String</span></span>

### <span data-ttu-id="a30c2-200">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a30c2-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="a30c2-201">Parametry: Applicationobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a30c2-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="a30c2-202">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="a30c2-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="a30c2-203">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="a30c2-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="a30c2-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a30c2-204">System.Security.SecureString</span></span>

### <span data-ttu-id="a30c2-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="a30c2-205">System.DateTime</span></span>

## <span data-ttu-id="a30c2-206">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a30c2-206">OUTPUTS</span></span>

### <span data-ttu-id="a30c2-207">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a30c2-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="a30c2-208">Microsoft. Azure. Commands. resources. models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="a30c2-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="a30c2-209">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a30c2-209">NOTES</span></span>
<span data-ttu-id="a30c2-210">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="a30c2-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a30c2-211">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a30c2-211">RELATED LINKS</span></span>

[<span data-ttu-id="a30c2-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a30c2-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a30c2-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a30c2-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a30c2-214">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a30c2-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="a30c2-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a30c2-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="a30c2-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a30c2-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="a30c2-217">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a30c2-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="a30c2-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a30c2-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

