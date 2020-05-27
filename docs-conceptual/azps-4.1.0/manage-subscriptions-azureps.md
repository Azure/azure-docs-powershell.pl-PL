---
title: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell
description: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 2fbf4387bb6a3b70a95bf607e3a24d61539e5810
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/19/2020
ms.locfileid: "83630728"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="4a681-103">Korzystanie z wielu subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4a681-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="4a681-104">Większość użytkowników platformy Azure będzie mieć tylko jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="4a681-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="4a681-105">Jeśli jednak stanowisz składnik więcej niż jednej organizacji lub Twoja organizacja podzieliła dostęp do niektórych zasobów między grupy, możesz mieć wiele subskrypcji w obrębie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4a681-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="4a681-106">Interfejs wiersza polecenia obsługuje wybór subskrypcji zarówno globalnie, jak i za pomocą poleceń.</span><span class="sxs-lookup"><span data-stu-id="4a681-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="4a681-107">Aby uzyskać szczegółowe informacje o subskrypcjach, rozliczeniach i zarządzaniu kosztami, zobacz [dokumentację dotyczącą rozliczeń i zarządzania kosztami](/azure/billing/).</span><span class="sxs-lookup"><span data-stu-id="4a681-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="4a681-108">Dzierżawy, użytkownicy i subskrypcje</span><span class="sxs-lookup"><span data-stu-id="4a681-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="4a681-109">Rozpoznanie różnic między dzierżawami, użytkownikami i subskrypcjami w obrębie platformy Azure może być trudne.</span><span class="sxs-lookup"><span data-stu-id="4a681-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="4a681-110">_Dzierżawa_ to jednostka usługi Azure Active Directory, która obejmuje całą organizację.</span><span class="sxs-lookup"><span data-stu-id="4a681-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="4a681-111">Ta dzierżawa ma co najmniej jedną _subskrypcję_ i jednego _użytkownika_.</span><span class="sxs-lookup"><span data-stu-id="4a681-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="4a681-112">Użytkownik to osoba skojarzona z tylko jedną dzierżawą — organizacją, do której należy.</span><span class="sxs-lookup"><span data-stu-id="4a681-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="4a681-113">Użytkownicy to konta, które logują się do platformy Azure w celu tworzenia zasobów, korzystania z nich i zarządzania nimi.</span><span class="sxs-lookup"><span data-stu-id="4a681-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="4a681-114">Użytkownik może mieć dostęp do wielu _subskrypcji_, które są umowami z firmą Microsoft na korzystanie z usług w chmurze, w tym z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4a681-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="4a681-115">Każdy zasób jest skojarzony z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="4a681-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="4a681-116">Aby dowiedzieć się więcej na temat różnic między dzierżawami, użytkownikami i subskrypcjami, zobacz [Słownik terminologii dotyczący chmury Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="4a681-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="4a681-117">Aby dowiedzieć się, jak dodać nową subskrypcję do dzierżawy usługi Azure Active Directory, zobacz [Jak dodać subskrypcję platformy Azure do katalogu usługi Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="4a681-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="4a681-118">Aby dowiedzieć się, jak zalogować się do określonej dzierżawy, zobacz [Logowanie się za pomocą programu Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="4a681-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="4a681-119">Zmiana aktywnej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4a681-119">Change the active subscription</span></span>

<span data-ttu-id="4a681-120">W programie Azure PowerShell uzyskiwanie dostępu do zasobów subskrypcji wymaga zmiany subskrypcji skojarzonej z bieżącą sesją platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4a681-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="4a681-121">Odbywa się to poprzez zmodyfikowanie kontekstu aktywnej sesji, czyli informacji o tym, względem której dzierżawy, subskrypcji i użytkownika powinny być uruchamiane polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a681-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="4a681-122">Aby zmienić subskrypcje, należy najpierw pobrać obiekt kontekstu programu Azure PowerShell za pomocą polecenia [Get AzSubscription](/powershell/module/az.accounts/get-azsubscription), a następnie zmienić bieżący kontekst przy użyciu polecenia[Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="4a681-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="4a681-123">W kolejnym przykładzie pokazano, jak uzyskać subskrypcję w ramach bieżącej aktywnej dzierżawy i ustawić ją jako aktywną sesję:</span><span class="sxs-lookup"><span data-stu-id="4a681-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="4a681-124">Aby dowiedzieć się więcej na temat kontekstów programu Azure PowerShell, w tym jak je zapisać, a następnie szybko przełączać się między nimi na potrzeby pracy z wieloma subskrypcjami, zobacz [Persist credentials with Azure PowerShell contexts](context-persistence.md) (Utrwalanie poświadczeń za pomocą kontekstów programu Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="4a681-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>