---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 530eafcd0d14dbfd790a22d80c5922f304f4e0b2
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737564"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="c2d1f-103">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2d1f-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="c2d1f-104">Program Azure PowerShell obsługuje wiele metod uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="c2d1f-105">Najprostszym sposobem rozpoczęcia pracy jest interaktywne zalogowanie się w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="c2d1f-106">Logowanie interakcyjne</span><span class="sxs-lookup"><span data-stu-id="c2d1f-106">Sign in interactively</span></span>

<span data-ttu-id="c2d1f-107">Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="c2d1f-108">Po uruchomieniu to polecenie cmdlet spowoduje otworzenie okna dialogowego z monitem o podanie adresu e-mail i hasła skojarzonego z kontem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="c2d1f-109">Po uwierzytelnieniu te informacje są zapisywane dla bieżącej sesji programu PowerShell, okno dialogowe jest zamykane i zapewniany jest dostęp do wszystkich poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2d1f-110">Logowanie obowiązuje _tylko_ w ramach bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-110">This sign in is for the current PowerShell session _only_.</span></span> <span data-ttu-id="c2d1f-111">Aby utrwalić uwierzytelnianie na wiele sesji, zapoznaj się z artykułem dotyczącym [poświadczeń trwałych](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-111">To persist authentication across multiple sessions, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="c2d1f-112">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="c2d1f-112">Sign in with a service principal</span></span>

<span data-ttu-id="c2d1f-113">Jednostki usługi zapewniają możliwość tworzenia nieinteraktywnych kont, których możesz używać do manipulowania zasobami.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="c2d1f-114">Jednostki usługi są podobne do kont użytkowników, do których można zastosować reguły za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="c2d1f-115">Udzielając minimalnych uprawnień niezbędnych dla jednostki usługi, możesz zapewnić, że skrypty automatyzacji będą jeszcze bezpieczniejsze.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="c2d1f-116">Jeśli chcesz utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="c2d1f-117">Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="c2d1f-118">Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="c2d1f-119">Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="c2d1f-120">To polecenie cmdlet spowoduje wyświetlenie okna dialogowego umożliwiającego wprowadzenie identyfikatora i hasła użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="c2d1f-121">Logowanie się przy użyciu tożsamości zarządzanych dla zasobów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c2d1f-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="c2d1f-122">Zarządzane tożsamości dla zasobów platformy Azure to funkcja usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="c2d1f-123">Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="c2d1f-124">Tożsamości zarządzane są dostępne tylko w przypadku maszyn wirtualnych działających w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="c2d1f-125">Aby uzyskać więcej informacji na temat tożsamości zarządzanych dla zasobów platformy Azure, zobacz [Jak używać tożsamości zarządzanych dla zasobów platformy Azure na maszynie wirtualnej platformy Azure w celu uzyskania tokenu dostępu](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="c2d1f-126">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="c2d1f-126">Sign in to another Cloud</span></span>

<span data-ttu-id="c2d1f-127">Usługi w chmurze platformy Azure udostępniają różne środowiska zgodne z przepisami dotyczącymi obsługi danych obowiązującymi w różnych regionach.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="c2d1f-128">Jeśli konto platformy Azure znajduje się w chmurze skojarzonej z jednym z tych regionów, podczas logowania należy określić środowisko.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="c2d1f-129">Jeśli na przykład konto należy do chmury chińskiej, rejestracja odbywa się za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="c2d1f-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="c2d1f-130">Użyj następującego polecenia, aby uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="c2d1f-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="c2d1f-131">Dowiedz się więcej o zarządzaniu dostępem opartym na rolach na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="c2d1f-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="c2d1f-132">Aby uzyskać więcej informacji o zarządzaniu uwierzytelnianiem i subskrypcjami platformy Azure, zobacz [Zarządzanie kontami, subskrypcjami i rolami administracyjnymi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="c2d1f-133">Polecenia cmdlet programu Azure PowerShell umożliwiające zarządzanie rolami:</span><span class="sxs-lookup"><span data-stu-id="c2d1f-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="c2d1f-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2d1f-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="c2d1f-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2d1f-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="c2d1f-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2d1f-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="c2d1f-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2d1f-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="c2d1f-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2d1f-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="c2d1f-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2d1f-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="c2d1f-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2d1f-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
