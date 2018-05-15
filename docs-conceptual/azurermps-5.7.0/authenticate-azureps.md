---
title: Logowanie za pomocą programu Azure PowerShell
description: Logowanie za pomocą programu Azure PowerShell
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f07dee0eed106e39879d58ae06ff08b787faa531
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="129a7-103">Logowanie za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="129a7-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="129a7-104">Program Azure PowerShell obsługuje wiele metod logowania.</span><span class="sxs-lookup"><span data-stu-id="129a7-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="129a7-105">Najprostszym sposobem rozpoczęcia pracy jest interaktywne zalogowanie się w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="129a7-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="129a7-106">Logowanie interaktywne</span><span class="sxs-lookup"><span data-stu-id="129a7-106">Interactive log in</span></span>

1. <span data-ttu-id="129a7-107">Wpisz polecenie `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="129a7-107">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="129a7-108">Zostanie wyświetlone okno dialogowe z monitem o podanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="129a7-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="129a7-109">Wpisz adres e-mail i hasło skojarzone z kontem.</span><span class="sxs-lookup"><span data-stu-id="129a7-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="129a7-110">Nastąpi uwierzytelnienie i zapisanie informacji o poświadczeniach na platformie Azure, a następnie zamknięcie okna.</span><span class="sxs-lookup"><span data-stu-id="129a7-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="129a7-111">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="129a7-111">Log in with a service principal</span></span>

<span data-ttu-id="129a7-112">Jednostki usługi zapewniają możliwość tworzenia nieinteraktywnych kont, których możesz używać do manipulowania zasobami.</span><span class="sxs-lookup"><span data-stu-id="129a7-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="129a7-113">Jednostki usługi są podobne do kont użytkowników, do których można zastosować reguły za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="129a7-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="129a7-114">Udzielając minimalnych uprawnień niezbędnych dla jednostki usługi, możesz zapewnić, że skrypty automatyzacji będą jeszcze bezpieczniejsze.</span><span class="sxs-lookup"><span data-stu-id="129a7-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="129a7-115">Jeśli nie masz jeszcze jednostki usługi, [utwórz ją](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="129a7-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="129a7-116">Zaloguj się za pomocą jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="129a7-116">Log in with the service principal.</span></span>

    ```powershell
    Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="129a7-117">Aby uzyskać identyfikator TenantId, zaloguj się interaktywnie i uzyskaj identyfikator dzierżawy ze swojej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="129a7-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="129a7-118">Logowanie się za pomocą tożsamości zarządzanej usługi maszyny wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="129a7-118">Log in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="129a7-119">Tożsamość usługi zarządzanej (MSI) jest dostępna w wersji zapoznawczej usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="129a7-119">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="129a7-120">Jednostki usługi tożsamości usługi zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="129a7-120">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="129a7-121">Aby uzyskać więcej informacji na temat tożsamości usługi zarządzanej, zobacz [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition (Sposób użycia tożsamości usługi zarządzanej maszyny wirtualnej platformy Azure do logowania się i uzyskania tokenu)](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="129a7-121">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="129a7-122">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="129a7-122">Log in to another Cloud</span></span>

<span data-ttu-id="129a7-123">Usługi w chmurze platformy Azure udostępniają różne środowiska zgodne z przepisami dotyczącymi obsługi danych określonymi przez administrację rządową poszczególnych krajów.</span><span class="sxs-lookup"><span data-stu-id="129a7-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="129a7-124">Jeśli dane konto Azure znajduje się w chmurze administracji rządowej, podczas logowania należy określić środowisko.</span><span class="sxs-lookup"><span data-stu-id="129a7-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="129a7-125">Jeśli na przykład konto należy do chmury chińskiej, rejestracja odbywa się za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="129a7-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="129a7-126">Użyj następującego polecenia, aby uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="129a7-126">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="129a7-127">Dowiedz się więcej o zarządzaniu dostępem opartym na rolach na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="129a7-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="129a7-128">Aby uzyskać więcej informacji o zarządzaniu uwierzytelnianiem i subskrypcjami platformy Azure, zobacz [Zarządzanie kontami, subskrypcjami i rolami administracyjnymi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="129a7-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="129a7-129">Polecenia cmdlet programu Azure PowerShell umożliwiające zarządzanie rolami</span><span class="sxs-lookup"><span data-stu-id="129a7-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="129a7-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="129a7-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="129a7-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="129a7-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="129a7-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="129a7-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="129a7-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="129a7-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="129a7-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="129a7-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="129a7-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="129a7-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="129a7-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="129a7-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
