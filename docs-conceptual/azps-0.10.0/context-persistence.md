---
title: Poświadczenia logowania i konteksty platformy Azure
description: Dowiedz się, jak używać ponownie poświadczeń platformy Azure i innych informacji w wielu sesjach programu PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: be9113ab1ad6a359832634ae2c21fd177b09318f
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410472"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="43815-103">Obiekty kontekstu środowiska Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="43815-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="43815-104">Środowisko Azure PowerShell używa _obiektów kontekstu środowiska Azure PowerShell_ (kontekstów platformy Azure) do przechowywania informacji o subskrypcji i uwierzytelnianiu.</span><span class="sxs-lookup"><span data-stu-id="43815-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="43815-105">Jeśli masz więcej niż jedną subskrypcję, konteksty platformy Azure umożliwiają wybranie subskrypcji, na której mają być uruchamiane polecenia cmdlet środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43815-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="43815-106">Konteksty platformy Azure są również używane do przechowywania informacji logowania w wielu sesjach programu PowerShell i uruchamiania zadań w tle.</span><span class="sxs-lookup"><span data-stu-id="43815-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="43815-107">W tym artykule opisano zarządzania kontekstami platformy Azure, a nie zarządzanie subskrypcjami ani kontami.</span><span class="sxs-lookup"><span data-stu-id="43815-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="43815-108">Jeśli chcesz zarządzać użytkownikami, subskrypcjami, dzierżawami lub innymi informacjami o koncie, zapoznaj się z dokumentacją usługi [Azure Active Directory](/azure/active-directory).</span><span class="sxs-lookup"><span data-stu-id="43815-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="43815-109">Aby dowiedzieć się więcej o używaniu kontekstów do uruchamiania zadań w tle lub równolegle, zobacz [Używanie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell](using-psjobs.md), gdy już zapoznasz się z kontekstami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43815-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="43815-110">Omówienie obiektów kontekstu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="43815-110">Overview of Azure context objects</span></span>

<span data-ttu-id="43815-111">Konteksty platformy Azure to obiekty programu PowerShell odzwierciedlające aktywną subskrypcję, w której są uruchamiane polecenia, oraz informacje uwierzytelniania wymagane do nawiązywania połączenia z chmurą platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43815-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="43815-112">Dzięki kontekstom platformy Azure środowisko Azure PowerShell nie musi ponownie uwierzytelniać Twojego konta za każdym razem, gdy przełączasz subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="43815-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="43815-113">Składniki kontekstu platformy Azure są następujące:</span><span class="sxs-lookup"><span data-stu-id="43815-113">An Azure context consists of:</span></span>

* <span data-ttu-id="43815-114">_Konto_ użyte do zalogowania się do platformy Azure za pomocą polecenia [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="43815-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="43815-115">Konteksty platformy Azure traktują użytkowników, identyfikatory aplikacji i jednostki usług tak samo z perspektywy konta.</span><span class="sxs-lookup"><span data-stu-id="43815-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="43815-116">Aktywna _subskrypcja_ , umowa serwisowa z firmą Microsoft na tworzenie i uruchamianie zasobów platformy Azure, które są skojarzone z _dzierżawą_.</span><span class="sxs-lookup"><span data-stu-id="43815-116">The active _subscription_ , a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="43815-117">Dzierżawy są często określane jako _organizacje_ w dokumentacji lub podczas pracy z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="43815-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="43815-118">Odwołanie do _pamięci podręcznej tokenu_ , przechowywanego tokenu uwierzytelniania na potrzeby uzyskiwania dostępu do chmury platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43815-118">A reference to a _token cache_ , a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="43815-119">Miejsce, w którym ten token jest przechowywany, oraz czas jego trwania jest określany przez [ustawienia automatycznego zapisywania kontekstu](#save-azure-contexts-across-powershell-sessions).</span><span class="sxs-lookup"><span data-stu-id="43815-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="43815-120">Aby uzyskać więcej informacji o tych terminach, zobacz [Terminologia usługi Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="43815-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="43815-121">Tokeny uwierzytelniania używane przez konteksty platformy Azure są takie same jak inne przechowywane tokeny będące składnikami sesji trwałej.</span><span class="sxs-lookup"><span data-stu-id="43815-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span>

<span data-ttu-id="43815-122">Po zalogowaniu się przy użyciu polecenia `Connect-AzAccount` dla domyślnej subskrypcji zostanie utworzony co najmniej jeden kontekst platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43815-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="43815-123">Obiekt zwrócony przez polecenie `Connect-AzAccount` jest domyślnym kontekstem platformy Azure używanym przez pozostałą część sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43815-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="43815-124">Pobieranie kontekstów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="43815-124">Get Azure contexts</span></span>

<span data-ttu-id="43815-125">Dostępne konteksty platformy Azure są pobierane za pomocą polecenia cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext).</span><span class="sxs-lookup"><span data-stu-id="43815-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="43815-126">Wyświetl listę wszystkich dostępnych kontekstów, używając parametru `-ListAvailable`:</span><span class="sxs-lookup"><span data-stu-id="43815-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="43815-127">Lub pobierz kontekst według nazwy:</span><span class="sxs-lookup"><span data-stu-id="43815-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="43815-128">Nazwy kontekstów mogą być inne od nazwy skojarzonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="43815-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43815-129">Dostępne konteksty platformy Azure to __nie zawsze są__ Twoje dostępne subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="43815-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="43815-130">Konteksty platformy Azure odzwierciedlają tylko lokalnie przechowywane informacje.</span><span class="sxs-lookup"><span data-stu-id="43815-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="43815-131">Subskrypcje można pobrać przy użyciu polecenia cmdlet [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription).</span><span class="sxs-lookup"><span data-stu-id="43815-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="43815-132">Tworzenie nowego kontekstu platformy Azure na podstawie informacji o subskrypcji</span><span class="sxs-lookup"><span data-stu-id="43815-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="43815-133">Polecenie cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) służy zarówno do tworzenia nowych kontekstów platformy Azure, jak i ustawiania ich jako aktywnego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="43815-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="43815-134">Najprostszy sposób na utworzenie nowego kontekstu platformy Azure to użycie informacji o istniejącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="43815-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="43815-135">Polecenie cmdlet ma za zadanie pobranie obiektu wyjściowego z polecenia `Get-AzSubscription` jako wartości w postaci potoku i skonfigurowanie nowego kontekstu platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="43815-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="43815-136">Lub podania w razie potrzeby identyfikatora albo nazwy subskrypcji oraz identyfikatora dzierżawy:</span><span class="sxs-lookup"><span data-stu-id="43815-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="43815-137">Jeśli argument `-Name` zostanie pominięty, jako nazwa kontekstu będzie używany identyfikator i nazwa subskrypcji w formacie `Subscription Name (subscription-id)`.</span><span class="sxs-lookup"><span data-stu-id="43815-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="43815-138">Zmienianie aktywnego kontekstu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="43815-138">Change the active Azure context</span></span>

<span data-ttu-id="43815-139">Aby zmienić aktywny kontekst platformy Azure, można użyć zarówno polecenia `Set-AzContext`, jak i [Select-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="43815-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="43815-140">Tak jak opisano w sekcji [Tworzenie nowego kontekstu platformy Azure](#create-a-new-azure-context-from-subscription-information), polecenie `Set-AzContext` tworzy nowy kontekst platformy Azure dla subskrypcji, jeśli taki nie istnieje, a następnie przełącza się na używanie tego kontekstu jako aktywnego.</span><span class="sxs-lookup"><span data-stu-id="43815-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="43815-141">Polecenie `Select-AzContext` powinno być używane tylko z istniejącymi kontekstami platformy Azure i działa podobnie do stosowania polecenia `Set-AzContext -Context`, ale jest przeznaczone do używania z potokowaniem:</span><span class="sxs-lookup"><span data-stu-id="43815-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="43815-142">Podobnie jak wiele innych poleceń zarządzania kontem i kontekstem w środowisku Azure PowerShell, polecenia `Set-AzContext` i `Select-AzContext` obsługują argument `-Scope`, co pozwala kontrolować czas aktywności kontekstu.</span><span class="sxs-lookup"><span data-stu-id="43815-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="43815-143">Argument `-Scope` pozwala na zmianę aktywnego kontekstu pojedynczej sesji bez zmieniania domyślnego:</span><span class="sxs-lookup"><span data-stu-id="43815-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="43815-144">Aby uniknąć przełączania kontekstów dla całej sesji programu PowerShell, wszystkie polecenia środowiska Azure PowerShell można uruchamiać względem danego kontekstu z argumentem `-AzContext`:</span><span class="sxs-lookup"><span data-stu-id="43815-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="43815-145">Innym głównym zastosowaniem kontekstów z poleceniami cmdlet środowiska Azure PowerShell jest uruchamianie poleceń w tle.</span><span class="sxs-lookup"><span data-stu-id="43815-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="43815-146">Aby dowiedzieć się więcej o uruchamianiu zadań programu PowerShell przy użyciu środowiska Azure PowerShell, zobacz [Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="43815-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="43815-147">Zapisywanie kontekstów platformy Azure w różnych sesjach programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="43815-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="43815-148">Domyślnie konteksty platformy Azure są zapisywane w celu używania ich między sesjami programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43815-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="43815-149">To zachowanie można zmienić w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="43815-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="43815-150">Zaloguj się przy użyciu polecenia `-Scope Process` z parametrem `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="43815-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="43815-151">Kontekst platformy Azure zwrócony jako część tego logowania jest prawidłowy _tylko_ dla bieżącej sesji i nie zostanie automatycznie zapisany, niezależnie od ustawienia automatycznego zapisywania kontekstu środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43815-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="43815-152">Wyłącz automatyczne zapisywanie kontekstu środowiska Azure PowerShell przy użyciu polecenia cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="43815-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="43815-153">Wyłączenie automatycznego zapisywania kontekstu __nie__ powoduje wyczyszczenia żadnych przechowywanych tokenów.</span><span class="sxs-lookup"><span data-stu-id="43815-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="43815-154">Aby dowiedzieć się, jak wyczyścić przechowywane informacje o kontekście platformy Azure, zobacz [Usuwanie poświadczeń i kontekstów platformy Azure](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="43815-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="43815-155">Jawnie włącz automatyczne zapisywanie kontekstu platformy Azure przy użyciu polecenia cmdlet [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="43815-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="43815-156">Gdy automatyczne zapisywanie jest włączone, wszystkie konteksty użytkownika są przechowywane lokalnie na potrzeby przyszłych sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43815-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="43815-157">Za pomocą polecenia [Save-AzContext](/powershell/module/az.accounts/save-azcontext) ręcznie zapisz konteksty do używania w przyszłych sesjach programu PowerShell, w których mogą być one ładowane za pomocą polecenia [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span><span class="sxs-lookup"><span data-stu-id="43815-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="43815-158">Wyłączenie automatycznego zapisywania kontekstu __nie__ powoduje wyczyszczenia żadnych zapisanych informacji o kontekście.</span><span class="sxs-lookup"><span data-stu-id="43815-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="43815-159">Aby usunąć przechowywane informacje, użyj polecenia cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="43815-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="43815-160">Aby uzyskać więcej informacji na temat usuwania zapisanych kontekstów, zobacz sekcję [Usuwanie kontekstów i poświadczeń](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="43815-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="43815-161">Każde z tych poleceń obsługuje parametr `-Scope`, który może przyjmować wartość `Process` do stosowania tylko do obecnie uruchomionego procesu.</span><span class="sxs-lookup"><span data-stu-id="43815-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="43815-162">Aby na przykład zapewnić, że nowo utworzone konteksty nie są zapisywane po zakończeniu sesji programu PowerShell:</span><span class="sxs-lookup"><span data-stu-id="43815-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="43815-163">Informacje o kontekście i tokeny są przechowywane w katalogu `$env:USERPROFILE\.Azure` w systemie Windows oraz w katalogu `$HOME/.Azure` na innych platformach.</span><span class="sxs-lookup"><span data-stu-id="43815-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="43815-164">Informacje poufne, takie jak identyfikatory subskrypcji i identyfikatory dzierżawy, mogą być nadal ujawnione w przechowywanych informacjach za pośrednictwem dzienników lub zapisanych kontekstów.</span><span class="sxs-lookup"><span data-stu-id="43815-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="43815-165">Aby dowiedzieć się, jak wyczyścić przechowywane informacje, zobacz sekcję [Usuwanie kontekstów i poświadczeń](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="43815-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="43815-166">Usuwanie przechowywanych poświadczeń i kontekstów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="43815-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="43815-167">Aby wyczyścić poświadczenia i konteksty platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="43815-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="43815-168">Wyloguj się z konta przy użyciu polecenia [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="43815-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="43815-169">Możesz wylogować się z dowolnego konta według konta lub kontekstu:</span><span class="sxs-lookup"><span data-stu-id="43815-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="43815-170">Rozłączenie zawsze powoduje usunięcie przechowywanych tokenów uwierzytelniania i wyczyszczenie zapisanych kontekstów skojarzonych z odłączonym użytkownikiem lub kontekstem.</span><span class="sxs-lookup"><span data-stu-id="43815-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="43815-171">Użyj polecenia [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="43815-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="43815-172">To polecenie cmdlet zawsze gwarantuje usunięcie przechowywanych kontekstów i tokenów uwierzytelniania, a także wyloguje Cię.</span><span class="sxs-lookup"><span data-stu-id="43815-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="43815-173">Usuń kontekst za pomocą polecenia [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span><span class="sxs-lookup"><span data-stu-id="43815-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>

  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="43815-174">Jeśli usuniesz aktywny kontekst, nastąpi odłączenie od platformy Azure i będzie konieczne ponowne uwierzytelnienie przy użyciu polecenia `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="43815-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="43815-175">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="43815-175">See also</span></span>

* [<span data-ttu-id="43815-176">Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="43815-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="43815-177">Terminologia usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="43815-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="43815-178">Dokumentacja modułu Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="43815-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
