---
title: Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell
description: Dowiedz się, jak używać ponownie poświadczeń platformy Azure i innych informacji w wielu sesjach programu PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8702de48429482748939fb1a43ff911bed15f6c0
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475429"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="317b3-103">Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="317b3-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="317b3-104">Program Azure PowerShell oferuje funkcję **automatycznego zapisywania kontekstu platformy Azure**, która udostępnia następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="317b3-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="317b3-105">Przechowywanie informacji logowania do ponownego użycia w nowych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="317b3-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="317b3-106">Łatwiejsze korzystanie z zadań w tle w celu wykonywania długotrwałych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="317b3-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="317b3-107">Możliwość przełączania kont, subskrypcji i środowisk bez konieczności osobnego logowania się.</span><span class="sxs-lookup"><span data-stu-id="317b3-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="317b3-108">Możliwość wykonywania zadań z użyciem różnych poświadczeń i subskrypcji jednocześnie w tej samej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="317b3-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="317b3-109">Zdefiniowane konteksty platformy Azure</span><span class="sxs-lookup"><span data-stu-id="317b3-109">Azure contexts defined</span></span>

<span data-ttu-id="317b3-110">*Kontekst platformy Azure* to zestaw informacji, który definiuje cel poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="317b3-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="317b3-111">Kontekst składa się z pięciu części:</span><span class="sxs-lookup"><span data-stu-id="317b3-111">The context consists of five parts:</span></span>

- <span data-ttu-id="317b3-112">*Konto* — nazwa użytkownika lub jednostka usługi używana do uwierzytelniania komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="317b3-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="317b3-113">*Subskrypcja* — subskrypcja platformy Azure zawierająca zasoby, których dotyczą wykonywane operacje.</span><span class="sxs-lookup"><span data-stu-id="317b3-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="317b3-114">*Dzierżawa* — dzierżawa usługi Azure Active Directory, która zawiera Twoją subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="317b3-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="317b3-115">Dzierżawy są ważniejsze w przypadku uwierzytelniania za pomocą jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="317b3-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="317b3-116">*Środowisko* — konkretna chmura platformy Azure będąca chmurą docelową. Zwykle jest to chmura globalna platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="317b3-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="317b3-117">Jednak ustawienia środowiska pozwalają również wybierać jako obiekty docelowe chmury krajowe, rządowe oraz lokalne (usługa Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="317b3-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="317b3-118">*Poświadczenia* — informacje używane przez platformę Azure do zweryfikowania Twojej tożsamości i potwierdzenia, że masz autoryzację do uzyskania dostępu do zasobów na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="317b3-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="317b3-119">Od najnowszej wersji programu Azure PowerShell konteksty platformy Azure mogą być automatycznie zapisywane przy każdym otwarciu nowej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="317b3-119">With the latest version of Azure PowerShell, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="317b3-120">Automatyczne zapisywanie kontekstu na potrzeby następnego logowania</span><span class="sxs-lookup"><span data-stu-id="317b3-120">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="317b3-121">Program Azure PowerShell automatycznie zachowuje informacje o kontekście między sesjami.</span><span class="sxs-lookup"><span data-stu-id="317b3-121">Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="317b3-122">Aby skonfigurować w programie PowerShell zapominanie kontekstu i poświadczeń, użyj polecenia `Disable-AzContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="317b3-122">To set PowerShell to forget your context and credentials, use `Disable-AzContextAutoSave`.</span></span> <span data-ttu-id="317b3-123">Po wyłączeniu zapisywania kontekstu konieczne będzie logowanie się do platformy Azure każdorazowo po otwarciu nowej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="317b3-123">With context saving disabled, you'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="317b3-124">Aby umożliwić programowi Azure PowerShell zapamiętywanie kontekstu po zamknięciu sesji programu PowerShell, użyj polecenia `Enable-AzContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="317b3-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzContextAutosave`.</span></span> <span data-ttu-id="317b3-125">Informacje o kontekście i poświadczenia będą automatycznie zapisywane w specjalnym ukrytym folderze w katalogu użytkownika (`$env:USERPROFILE\.Azure` w systemie Windows oraz `$HOME/.Azure` na innych platformach).</span><span class="sxs-lookup"><span data-stu-id="317b3-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="317b3-126">Każda nowa sesja programu PowerShell wybiera kontekst użyty w ostatniej sesji jako docelowy.</span><span class="sxs-lookup"><span data-stu-id="317b3-126">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="317b3-127">Polecenia cmdlet, które umożliwiają zarządzanie kontekstami platformy Azure, umożliwiają także szczegółowe kontrolowanie.</span><span class="sxs-lookup"><span data-stu-id="317b3-127">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="317b3-128">Dzięki nim można określić, czy zmiany mają obowiązywać tylko w bieżącej sesji programu PowerShell (zakres `Process`), czy każdej sesji programu PowerShell (zakres `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="317b3-128">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="317b3-129">Te opcje są szczegółowo omówione w temacie [Korzystanie z zakresów kontekstu](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="317b3-129">These options are discussed in more detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="317b3-130">Uruchamianie poleceń cmdlet programu PowerShell platformy Azure jako zadań w tle</span><span class="sxs-lookup"><span data-stu-id="317b3-130">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="317b3-131">Funkcja **automatycznego zapisywania kontekstu platformy Azure** umożliwia udostępnianie kontekstu użytkownika zadaniom programu PowerShell wykonywanym w tle.</span><span class="sxs-lookup"><span data-stu-id="317b3-131">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="317b3-132">Program PowerShell umożliwia uruchamianie i monitorowanie długo wykonywanych zadań jako zadań w tle bez konieczności oczekiwania na zakończenie tych zadań.</span><span class="sxs-lookup"><span data-stu-id="317b3-132">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="317b3-133">Użytkownik może udostępniać poświadczenia zadaniom w tle na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="317b3-133">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="317b3-134">Przekazując kontekst jako argument</span><span class="sxs-lookup"><span data-stu-id="317b3-134">Passing the context as an argument</span></span>

  <span data-ttu-id="317b3-135">Większość poleceń cmdlet usługi AzureRM umożliwia przekazanie kontekstu w postaci parametru do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="317b3-135">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="317b3-136">Kontekst można przekazać do zadania w tle w sposób przedstawiony w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="317b3-136">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- <span data-ttu-id="317b3-137">Używając domyślnego kontekstu z włączoną funkcją automatycznego zapisywania</span><span class="sxs-lookup"><span data-stu-id="317b3-137">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="317b3-138">Jeśli włączono funkcję **automatycznego zapisywania kontekstu**, wówczas zadania w tle automatycznie używają domyślnego zapisanego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="317b3-138">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

<span data-ttu-id="317b3-139">Jeśli chcesz poznać wynik zadania w tle, użyj polecenia `Get-Job`, aby sprawdzić stan zadania, oraz polecenia `Wait-Job`, aby poczekać na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="317b3-139">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="317b3-140">Aby przechwycić lub wyświetlić wynik zadania w tle, użyj polecenia `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="317b3-140">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="317b3-141">Aby uzyskać więcej informacji, zobacz opis polecenia [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="317b3-141">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="317b3-142">Tworzenie, wybieranie i usuwanie kontekstów oraz zmiana ich nazw</span><span class="sxs-lookup"><span data-stu-id="317b3-142">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="317b3-143">Aby utworzyć kontekst, musisz zalogować się do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="317b3-143">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="317b3-144">Polecenie cmdlet `Connect-AzAccount` (lub jego alias — `Login-AzAccount`) ustawia domyślny kontekst używany przez polecenia cmdlet programu Azure PowerShell i pozwala użytkownikowi na dostęp do dowolnych dzierżaw lub subskrypcji, na które pozwalają poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="317b3-144">The `Connect-AzAccount` cmdlet (or its alias, `Login-AzAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="317b3-145">Aby dodać nowy kontekst po zalogowaniu, użyj polecenia `Set-AzContext` (lub jego aliasu — `Select-AzSubscription`).</span><span class="sxs-lookup"><span data-stu-id="317b3-145">To add a new context after sign-in, use `Set-AzContext` (or its alias, `Select-AzSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="317b3-146">Poprzedni przykład dodaje nowy kontekst, którego obiektem docelowym jest „Contoso Subscription 1”, z użyciem bieżących poświadczeń użytkownika.</span><span class="sxs-lookup"><span data-stu-id="317b3-146">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="317b3-147">Nowy kontekst ma nazwę „Contoso1”.</span><span class="sxs-lookup"><span data-stu-id="317b3-147">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="317b3-148">Jeśli nie podasz nazwy dla tego kontekstu, będzie używana nazwa domyślna zawierająca identyfikator konta i identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="317b3-148">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="317b3-149">Aby zmienić nazwę istniejącego kontekstu, użyj polecenia cmdlet `Rename-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="317b3-149">To rename an existing context, use the `Rename-AzContext` cmdlet.</span></span> <span data-ttu-id="317b3-150">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="317b3-150">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="317b3-151">Ten przykład zmienia nazwę kontekstu o nazwie automatycznej `[user1@contoso.org; 123456-7890-1234-564321]` na prostą nazwę „Contoso2”.</span><span class="sxs-lookup"><span data-stu-id="317b3-151">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="317b3-152">Polecenia cmdlet, które zarządzają kontekstami, używają również wypełniania po naciśnięciu klawisza TAB, dzięki czemu możliwe jest szybkie wybieranie kontekstu.</span><span class="sxs-lookup"><span data-stu-id="317b3-152">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="317b3-153">Aby na koniec usunąć kontekst, użyj polecenia cmdlet `Remove-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="317b3-153">Finally, to remove a context, use the `Remove-AzContext` cmdlet.</span></span>  <span data-ttu-id="317b3-154">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="317b3-154">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

<span data-ttu-id="317b3-155">Powoduje zapomnienie kontekstu o nazwie „Contoso2”.</span><span class="sxs-lookup"><span data-stu-id="317b3-155">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="317b3-156">Możesz utworzyć ten kontekst ponownie, używając polecenia `Set-AzContext`</span><span class="sxs-lookup"><span data-stu-id="317b3-156">You can recreate this context using `Set-AzContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="317b3-157">Usuwanie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="317b3-157">Removing credentials</span></span>

<span data-ttu-id="317b3-158">Można usunąć wszystkie poświadczenia i skojarzone konteksty dla użytkownika lub jednostki usługi przy użyciu polecenia `Disconnect-AzAccount` (znanego również jako `Logout-AzAccount`).</span><span class="sxs-lookup"><span data-stu-id="317b3-158">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzAccount` (also known as `Logout-AzAccount`).</span></span> <span data-ttu-id="317b3-159">Polecenie cmdlet `Disconnect-AzAccount` wykonywane bez parametrów usuwa wszystkie poświadczenia i konteksty skojarzone z użytkownikiem lub jednostką usługi w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="317b3-159">When executed without parameters, the `Disconnect-AzAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="317b3-160">Możesz przekazać nazwę użytkownika, jednostkę usługi lub kontekst do konkretnego docelowego podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="317b3-160">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="317b3-161">Korzystanie z zakresów kontekstu</span><span class="sxs-lookup"><span data-stu-id="317b3-161">Using context scopes</span></span>

<span data-ttu-id="317b3-162">W niektórych okolicznościach kontekst można wybrać, zmienić lub usunąć w sesji programu PowerShell bez wpływu na pozostałe sesje.</span><span class="sxs-lookup"><span data-stu-id="317b3-162">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="317b3-163">Aby zmienić domyślne zachowanie poleceń cmdlet kontekstu, użyj parametru `Scope`.</span><span class="sxs-lookup"><span data-stu-id="317b3-163">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="317b3-164">Zakres `Process` zastępuje domyślne działanie tego parametru, sprawiając, że dotyczy tylko bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="317b3-164">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="317b3-165">Z drugiej strony zakres `CurrentUser` zmienia kontekst we wszystkich sesjach, a nie tylko w bieżącej.</span><span class="sxs-lookup"><span data-stu-id="317b3-165">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="317b3-166">Aby na przykład zmienić kontekst domyślny w bieżącej sesji programu PowerShell bez wpływu na inne okna albo na kontekst używany przy następnym otwarciu sesji, użyj następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="317b3-166">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="317b3-167">Jak zapamiętywane jest ustawienie automatycznego zapisywania kontekstu</span><span class="sxs-lookup"><span data-stu-id="317b3-167">How the context autosave setting is remembered</span></span>

<span data-ttu-id="317b3-168">Ustawienie automatycznego zapisywania kontekstu jest zapisywane w katalogu użytkownika programu Azure PowerShell (`$env:USERPROFILE\.Azure` w systemie Windows i `$HOME/.Azure` na innych platformach).</span><span class="sxs-lookup"><span data-stu-id="317b3-168">The context AutoSave setting is saved to the user Azure PowerShell directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="317b3-169">Niektóre rodzaje kont komputerów mogą nie mieć dostępu do tego katalogu.</span><span class="sxs-lookup"><span data-stu-id="317b3-169">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="317b3-170">W przypadku takich scenariuszy można użyć zmiennej środowiskowej</span><span class="sxs-lookup"><span data-stu-id="317b3-170">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="317b3-171">Gdy zostanie ustawiona na wartość „true”, kontekst będzie zapisywany automatycznie.</span><span class="sxs-lookup"><span data-stu-id="317b3-171">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="317b3-172">Jeśli zostanie ustawiona na wartość „false”, kontekst nie będzie zapisywany.</span><span class="sxs-lookup"><span data-stu-id="317b3-172">If set to 'false', the context isn't saved.</span></span>

## <a name="context-management-cmdlets"></a><span data-ttu-id="317b3-173">Polecenia cmdlet do zarządzania kontekstem</span><span class="sxs-lookup"><span data-stu-id="317b3-173">Context management cmdlets</span></span>

- <span data-ttu-id="317b3-174">[Enable-AzContextAutosave][enable] — umożliwia zapisywanie kontekstu między sesjami programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="317b3-174">[Enable-AzContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="317b3-175">Wszelkie zmiany powodują zmianę kontekstu globalnego.</span><span class="sxs-lookup"><span data-stu-id="317b3-175">Any changes alter the global context.</span></span>
- <span data-ttu-id="317b3-176">[Disable-AzContextAutosave][disable] — wyłącza automatyczne zapisywanie kontekstu.</span><span class="sxs-lookup"><span data-stu-id="317b3-176">[Disable-AzContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="317b3-177">W każdej nowej sesji programu PowerShell konieczne będzie ponowne logowanie się.</span><span class="sxs-lookup"><span data-stu-id="317b3-177">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="317b3-178">[Select-AzContext][select] — umożliwia wybór kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="317b3-178">[Select-AzContext][select] - Select a context as the default.</span></span> <span data-ttu-id="317b3-179">Wszystkie polecenia cmdlet będą używać poświadczeń z tego kontekstu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="317b3-179">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="317b3-180">[Disconnect-AzAccount][remove-cred] — usuwa wszystkie poświadczenia i konteksty skojarzone z danym kontem.</span><span class="sxs-lookup"><span data-stu-id="317b3-180">[Disconnect-AzAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="317b3-181">[Remove-AzContext][remove-context] — usuwa nazwany kontekst.</span><span class="sxs-lookup"><span data-stu-id="317b3-181">[Remove-AzContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="317b3-182">[Rename-AzContext][rename] — zmienia nazwę istniejącego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="317b3-182">[Rename-AzContext][rename] - Rename an existing context.</span></span>
- <span data-ttu-id="317b3-183">[Add-AzAccount][login] — umożliwia określenie zakresu logowania do procesu lub bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="317b3-183">[Add-AzAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="317b3-184">Pozwala na nazwanie domyślnego kontekstu po uwierzytelnieniu się.</span><span class="sxs-lookup"><span data-stu-id="317b3-184">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="317b3-185">[Import-AzContext][import] — umożliwia określenie zakresu logowania do procesu lub bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="317b3-185">[Import-AzContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="317b3-186">[Set-AzContext][set-context] — umożliwia wybór istniejących nazwanych kontekstów oraz określenie zakresu zmian do procesu lub bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="317b3-186">[Set-AzContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
