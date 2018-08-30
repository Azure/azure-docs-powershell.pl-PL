---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości usługi zarządzanej.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018846"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="25523-103">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="25523-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="25523-104">Program Azure PowerShell obsługuje wiele metod uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="25523-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="25523-105">Najprostszym sposobem rozpoczęcia pracy jest interaktywne zalogowanie się w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="25523-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="25523-106">Logowanie interakcyjne</span><span class="sxs-lookup"><span data-stu-id="25523-106">Sign in interactively</span></span>

<span data-ttu-id="25523-107">Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="25523-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="25523-108">Po uruchomieniu to polecenie cmdlet spowoduje otworzenie okna dialogowego z monitem o podanie adresu e-mail i hasła skojarzonego z kontem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="25523-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="25523-109">Po uwierzytelnieniu te informacje są zapisywane dla bieżącej sesji programu PowerShell, okno dialogowe jest zamykane i zapewniany jest dostęp do wszystkich poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25523-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25523-110">Począwszy od programu Azure PowerShell w wersji 6.3.0, poświadczenia są współużytkowane w ramach wielu sesji programu PowerShell, dopóki użytkownik jest zalogowany w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="25523-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="25523-111">Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="25523-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="25523-112">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="25523-112">Sign in with a service principal</span></span>

<span data-ttu-id="25523-113">Jednostki usługi zapewniają możliwość tworzenia nieinteraktywnych kont, których możesz używać do manipulowania zasobami.</span><span class="sxs-lookup"><span data-stu-id="25523-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="25523-114">Jednostki usługi są podobne do kont użytkowników, do których można zastosować reguły za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25523-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="25523-115">Udzielając minimalnych uprawnień niezbędnych dla jednostki usługi, możesz zapewnić, że skrypty automatyzacji będą jeszcze bezpieczniejsze.</span><span class="sxs-lookup"><span data-stu-id="25523-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="25523-116">Jeśli chcesz utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="25523-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="25523-117">Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="25523-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="25523-118">Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="25523-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="25523-119">Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="25523-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="25523-120">To polecenie cmdlet spowoduje wyświetlenie okna dialogowego umożliwiającego wprowadzenie identyfikatora i hasła użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25523-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="25523-121">Logowanie się za pomocą tożsamości usługi zarządzanej maszyny wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="25523-121">Sign in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="25523-122">Tożsamość usługi zarządzanej (MSI) jest dostępna w wersji zapoznawczej usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25523-122">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="25523-123">Jednostki usługi tożsamości usługi zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="25523-123">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="25523-124">Tożsamość MSI jest dostępna tylko w przypadku maszyn wirtualnych działających w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="25523-124">MSI is only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="25523-125">Aby uzyskać więcej informacji na temat tożsamości usługi zarządzanej, zobacz [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition (Sposób użycia tożsamości usługi zarządzanej maszyny wirtualnej platformy Azure do logowania się i uzyskania tokenu)](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="25523-125">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="25523-126">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="25523-126">Sign in to another Cloud</span></span>

<span data-ttu-id="25523-127">Usługi w chmurze platformy Azure udostępniają różne środowiska zgodne z przepisami dotyczącymi obsługi danych obowiązującymi w różnych regionach.</span><span class="sxs-lookup"><span data-stu-id="25523-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="25523-128">Jeśli konto platformy Azure znajduje się w chmurze skojarzonej z jednym z tych regionów, podczas logowania należy określić środowisko.</span><span class="sxs-lookup"><span data-stu-id="25523-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="25523-129">Jeśli na przykład konto należy do chmury chińskiej, rejestracja odbywa się za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="25523-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="25523-130">Użyj następującego polecenia, aby uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="25523-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="25523-131">Dowiedz się więcej o zarządzaniu dostępem opartym na rolach na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="25523-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="25523-132">Aby uzyskać więcej informacji o zarządzaniu uwierzytelnianiem i subskrypcjami platformy Azure, zobacz [Zarządzanie kontami, subskrypcjami i rolami administracyjnymi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="25523-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="25523-133">Polecenia cmdlet programu Azure PowerShell umożliwiające zarządzanie rolami:</span><span class="sxs-lookup"><span data-stu-id="25523-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="25523-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="25523-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="25523-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="25523-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="25523-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="25523-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="25523-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="25523-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="25523-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="25523-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="25523-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="25523-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="25523-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="25523-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
