---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786683"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="06a4c-103">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06a4c-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="06a4c-104">Program Azure PowerShell obsługuje kilka metod uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="06a4c-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="06a4c-105">Najprostszym sposobem rozpoczęcia pracy jest interaktywne zalogowanie się w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="06a4c-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="06a4c-106">Logowanie interakcyjne</span><span class="sxs-lookup"><span data-stu-id="06a4c-106">Sign in interactively</span></span>

<span data-ttu-id="06a4c-107">Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="06a4c-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="06a4c-108">Po uruchomieniu to polecenie cmdlet spowoduje wyświetlenie ciągu tokenu.</span><span class="sxs-lookup"><span data-stu-id="06a4c-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="06a4c-109">Aby się zalogować, skopiuj ten ciąg i wklej go w witrynie https://microsoft.com/devicelogin w przeglądarce.</span><span class="sxs-lookup"><span data-stu-id="06a4c-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="06a4c-110">Sesja programu PowerShell zostanie uwierzytelniona na potrzeby połączenia z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06a4c-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="06a4c-111">To uwierzytelnienie obowiązuje dla bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06a4c-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="06a4c-112">Poświadczenia są współdzielone w ramach wielu sesji programu PowerShell, dopóki użytkownik pozostanie zalogowany.</span><span class="sxs-lookup"><span data-stu-id="06a4c-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="06a4c-113">Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="06a4c-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="06a4c-114">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="06a4c-114">Sign in with a service principal</span></span>

<span data-ttu-id="06a4c-115">Jednostki usługi to nieinterakcyjne konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06a4c-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="06a4c-116">Podobnie jak w przypadku innych kont użytkownika, ich uprawnieniami zarządza się za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="06a4c-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="06a4c-117">Udzielając jednostce usługi tylko potrzebnych uprawnień, możesz zapewnić bezpieczeństwo skryptom automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="06a4c-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="06a4c-118">Aby dowiedzieć się, jak utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="06a4c-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="06a4c-119">Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="06a4c-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="06a4c-120">Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="06a4c-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="06a4c-121">Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="06a4c-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="06a4c-122">To polecenie cmdlet spowoduje wyświetlenie monitu o identyfikator użytkownika i hasło jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="06a4c-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="06a4c-123">Logowanie się za pomocą tożsamości usługi zarządzanej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="06a4c-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="06a4c-124">Zarządzane tożsamości dla zasobów platformy Azure to funkcja usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="06a4c-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="06a4c-125">Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="06a4c-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="06a4c-126">Tożsamości zarządzane są dostępne tylko w przypadku maszyn wirtualnych działających w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06a4c-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="06a4c-127">Aby uzyskać więcej informacji na temat tożsamości zarządzanych dla zasobów platformy Azure, zobacz [Jak używać tożsamości zarządzanych dla zasobów platformy Azure na maszynie wirtualnej platformy Azure w celu uzyskania tokenu dostępu](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="06a4c-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="06a4c-128">Logowanie się jako dostawca rozwiązań w chmurze</span><span class="sxs-lookup"><span data-stu-id="06a4c-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="06a4c-129">Do zalogowania [dostawcy rozwiązań w chmurze](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) wymagane jest użycie parametru `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="06a4c-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="06a4c-130">Zazwyczaj ten parametr można podać jako identyfikator dzierżawy lub nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="06a4c-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="06a4c-131">Jednak w przypadku logowania dostawcy rozwiązań w chmurze trzeba podać **identyfikator dzierżawy**.</span><span class="sxs-lookup"><span data-stu-id="06a4c-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="06a4c-132">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="06a4c-132">Sign in to another Cloud</span></span>

<span data-ttu-id="06a4c-133">Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych.</span><span class="sxs-lookup"><span data-stu-id="06a4c-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="06a4c-134">W przypadku kont w chmurze regionalnej określ środowisko po zalogowaniu się, używając argumentu `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="06a4c-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="06a4c-135">Na przykład jeśli Twoje konto znajduje się w chmurze w Chinach:</span><span class="sxs-lookup"><span data-stu-id="06a4c-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="06a4c-136">Następujące polecenie pozwala uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="06a4c-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="06a4c-137">Dowiedz się więcej o zarządzaniu dostępem opartym na rolach na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="06a4c-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="06a4c-138">Aby uzyskać więcej informacji o zarządzaniu uwierzytelnianiem i subskrypcjami platformy Azure, zobacz [Zarządzanie kontami, subskrypcjami i rolami administracyjnymi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="06a4c-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="06a4c-139">Polecenia cmdlet programu Azure PowerShell umożliwiające zarządzanie rolami:</span><span class="sxs-lookup"><span data-stu-id="06a4c-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="06a4c-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06a4c-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="06a4c-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06a4c-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="06a4c-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06a4c-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="06a4c-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06a4c-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="06a4c-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06a4c-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="06a4c-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06a4c-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="06a4c-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06a4c-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
