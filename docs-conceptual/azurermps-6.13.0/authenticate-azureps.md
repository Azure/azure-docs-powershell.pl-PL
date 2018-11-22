---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 6a42217c47c1e5101a708da87c15fc14004f2069
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259690"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="a7fd7-103">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a7fd7-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="a7fd7-104">Program Azure PowerShell obsługuje kilka metod uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="a7fd7-105">Najprostszym sposobem rozpoczęcia pracy jest interaktywne zalogowanie się w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="a7fd7-106">Logowanie interakcyjne</span><span class="sxs-lookup"><span data-stu-id="a7fd7-106">Sign in interactively</span></span>

<span data-ttu-id="a7fd7-107">Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="a7fd7-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="a7fd7-108">Po uruchomieniu to polecenie cmdlet spowoduje otworzenie okna dialogowego z monitem o podanie adresu e-mail i hasła skojarzonego z kontem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="a7fd7-109">To uwierzytelnienie obowiązuje dla bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7fd7-110">Począwszy od programu Azure PowerShell w wersji 6.3.0, poświadczenia są współużytkowane w ramach wielu sesji programu PowerShell, dopóki użytkownik jest zalogowany w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="a7fd7-111">Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a7fd7-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="a7fd7-112">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="a7fd7-112">Sign in with a service principal</span></span>

<span data-ttu-id="a7fd7-113">Jednostki usługi to nieinterakcyjne konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="a7fd7-114">Podobnie jak w przypadku innych kont użytkownika, ich uprawnieniami zarządza się za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="a7fd7-115">Udzielając jednostce usługi tylko potrzebnych uprawnień, możesz zapewnić bezpieczeństwo skryptom automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="a7fd7-116">Aby dowiedzieć się, jak utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a7fd7-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="a7fd7-117">Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="a7fd7-118">Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="a7fd7-119">Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="a7fd7-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="a7fd7-120">To polecenie cmdlet spowoduje wyświetlenie okna dialogowego umożliwiającego wprowadzenie identyfikatora i hasła użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="a7fd7-121">Logowanie się za pomocą tożsamości usługi zarządzanej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a7fd7-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="a7fd7-122">Zarządzane tożsamości dla zasobów platformy Azure to funkcja usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="a7fd7-123">Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="a7fd7-124">Tożsamości zarządzane są dostępne tylko w przypadku maszyn wirtualnych działających w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="a7fd7-125">Aby uzyskać więcej informacji na temat tożsamości zarządzanych dla zasobów platformy Azure, zobacz [Jak używać tożsamości zarządzanych dla zasobów platformy Azure na maszynie wirtualnej platformy Azure w celu uzyskania tokenu dostępu](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="a7fd7-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="a7fd7-126">Logowanie się jako dostawca rozwiązań w chmurze</span><span class="sxs-lookup"><span data-stu-id="a7fd7-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="a7fd7-127">Do zalogowania [dostawcy rozwiązań w chmurze](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) wymagane jest użycie parametru `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="a7fd7-128">Zazwyczaj ten parametr można podać jako identyfikator dzierżawy lub nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="a7fd7-129">Jednak w przypadku logowania dostawcy rozwiązań w chmurze trzeba podać **identyfikator dzierżawy**.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="a7fd7-130">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="a7fd7-130">Sign in to another Cloud</span></span>

<span data-ttu-id="a7fd7-131">Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="a7fd7-132">W przypadku kont w chmurze regionalnej określ środowisko po zalogowaniu się, używając argumentu `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="a7fd7-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="a7fd7-133">Na przykład jeśli Twoje konto znajduje się w chmurze w Chinach:</span><span class="sxs-lookup"><span data-stu-id="a7fd7-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="a7fd7-134">Następujące polecenie pozwala uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="a7fd7-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="a7fd7-135">Dowiedz się więcej o zarządzaniu dostępem opartym na rolach na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="a7fd7-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="a7fd7-136">Aby uzyskać więcej informacji o zarządzaniu uwierzytelnianiem i subskrypcjami platformy Azure, zobacz [Zarządzanie kontami, subskrypcjami i rolami administracyjnymi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="a7fd7-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="a7fd7-137">Polecenia cmdlet programu Azure PowerShell umożliwiające zarządzanie rolami:</span><span class="sxs-lookup"><span data-stu-id="a7fd7-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="a7fd7-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a7fd7-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="a7fd7-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a7fd7-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="a7fd7-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a7fd7-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="a7fd7-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a7fd7-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="a7fd7-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a7fd7-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="a7fd7-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a7fd7-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="a7fd7-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a7fd7-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
