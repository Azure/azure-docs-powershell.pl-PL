---
title: Zachowywanie danych logowania użytkownika między sesjami programu PowerShell
description: W niniejszym artykule wyjaśniono nowe funkcje programu Azure PowerShell, które umożliwiają ponowne korzystanie z poświadczeń i innych danych użytkownika między wieloma sesjami programu PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 678d08c24cf254cd904850071872eea18c6bf6cf
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821602"
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="8e4d5-103">Zachowywanie danych logowania użytkownika między sesjami programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="8e4d5-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="8e4d5-104">W wersji z września 2017 r. programu Azure PowerShell polecenia cmdlet usługi Azure Resource Manager wprowadzają nową funkcję — **automatyczny zapis kontekstu platformy Azure**.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="8e4d5-105">Ta funkcja umożliwia korzystanie z kilku nowych scenariuszy dotyczących użytkowników:</span><span class="sxs-lookup"><span data-stu-id="8e4d5-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="8e4d5-106">Przechowywanie danych logowania do ponownego wykorzystania w nowych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="8e4d5-107">Łatwiejsze korzystanie z zadań w tle w celu wykonywania długotrwałych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="8e4d5-108">Możliwość przełączania kont, subskrypcji i środowisk bez konieczności osobnego logowania się.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="8e4d5-109">Możliwość wykonywania zadań z użyciem różnych poświadczeń i subskrypcji jednocześnie w tej samej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="8e4d5-110">Zdefiniowane konteksty platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8e4d5-110">Azure contexts defined</span></span>

<span data-ttu-id="8e4d5-111">*Kontekst platformy Azure* to zestaw informacji, który definiuje cel poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="8e4d5-112">Kontekst składa się z pięciu części:</span><span class="sxs-lookup"><span data-stu-id="8e4d5-112">The context consists of five parts:</span></span>

- <span data-ttu-id="8e4d5-113">*Konto* — nazwa użytkownika lub jednostka usługi używana do uwierzytelniania komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8e4d5-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="8e4d5-114">*Subskrypcja* — subskrypcja platformy Azure zawierająca zasoby, których dotyczą wykonywane operacje.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="8e4d5-115">*Dzierżawa* — dzierżawa usługi Azure Active Directory, która zawiera Twoją subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="8e4d5-116">Dzierżawy są ważniejsze w przypadku uwierzytelniania za pomocą jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="8e4d5-117">*Środowisko* — konkretna chmura platformy Azure będąca chmurą docelową. Zwykle jest to chmura globalna platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="8e4d5-118">Jednak ustawienia środowiska pozwalają również wybierać jako obiekty docelowe chmury krajowe, rządowe oraz lokalne (usługa Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="8e4d5-119">*Poświadczenia* — informacje używane przez platformę Azure do zweryfikowania Twojej tożsamości i sprawdzenia, czy masz autoryzację do uzyskania dostępu do zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="8e4d5-120">W poprzednich wersjach kontekst platformy Azure musiał być tworzony każdorazowo po otwarciu nowej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="8e4d5-121">Począwszy od wersji 4.4.0 programu Azure PowerShell można włączyć automatyczne zapisywanie i ponowne użycie kontekstów platformy Azure przy każdym otwarciu nowej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="8e4d5-122">Automatyczne zapisywanie kontekstu na potrzeby następnego logowania</span><span class="sxs-lookup"><span data-stu-id="8e4d5-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="8e4d5-123">Domyślnie program Azure PowerShell odrzuca informacje o kontekście przy każdym zamknięciu sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="8e4d5-124">Aby umożliwić programowi Azure PowerShell zapamiętywanie kontekstu po zamknięciu sesji programu PowerShell, użyj polecenia `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="8e4d5-125">Informacje o kontekście i poświadczenia będą automatycznie zapisywane w specjalnym ukrytym folderze w katalogu użytkownika (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="8e4d5-126">Następnie każda nowa sesja programu PowerShell wybiera kontekst użyty w ostatniej sesji jako docelowy.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="8e4d5-127">Aby skonfigurować w programie PowerShell zapominanie kontekstu i poświadczeń, użyj polecenia `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="8e4d5-128">W takim przypadku konieczne będzie logowanie się do platformy Azure każdorazowo po otwarciu nowej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="8e4d5-129">Polecenia cmdlet, które umożliwiają zarządzanie kontekstami platformy Azure, umożliwiają także szczegółowe kontrolowanie.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="8e4d5-130">Dzięki nim można określić, czy zmiany mają obowiązywać tylko w bieżącej sesji programu PowerShell (zakres `Process`), czy każdej sesji programu PowerShell (zakres `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="8e4d5-131">Te opcje są szczegółowo omówione w temacie [Korzystanie z zakresów kontekstu](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="8e4d5-132">Uruchamianie poleceń cmdlet programu PowerShell platformy Azure jako zadań w tle</span><span class="sxs-lookup"><span data-stu-id="8e4d5-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="8e4d5-133">Funkcja **automatycznego zapisywania kontekstu platformy Azure** umożliwia udostępnianie kontekstu użytkownika zadaniom programu PowerShell wykonywanym w tle.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="8e4d5-134">Program PowerShell umożliwia uruchamianie i monitorowanie długo wykonywanych zadań jako zadań w tle bez konieczności oczekiwania na zakończenie tych zadań.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="8e4d5-135">Użytkownik może udostępniać poświadczenia zadaniom w tle na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="8e4d5-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="8e4d5-136">Przekazując kontekst jako argument</span><span class="sxs-lookup"><span data-stu-id="8e4d5-136">Passing the context as an argument</span></span>

  <span data-ttu-id="8e4d5-137">Większość poleceń cmdlet usługi AzureRM umożliwia przekazanie kontekstu w postaci parametru do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="8e4d5-138">Kontekst można przekazać do zadania w tle w sposób przedstawiony w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="8e4d5-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="8e4d5-139">Używając domyślnego kontekstu z włączoną funkcją automatycznego zapisywania</span><span class="sxs-lookup"><span data-stu-id="8e4d5-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="8e4d5-140">Jeśli włączono funkcję **automatycznego zapisywania kontekstu**, wówczas zadania w tle automatycznie używają domyślnego zapisanego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="8e4d5-141">Jeśli chcesz poznać wynik zadania w tle, użyj polecenia `Get-Job`, aby sprawdzić stan zadania, oraz polecenia `Wait-Job`, aby poczekać na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="8e4d5-142">Aby przechwycić lub wyświetlić wynik zadania w tle, użyj polecenia `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="8e4d5-143">Aby uzyskać więcej informacji, zobacz opis polecenia [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="8e4d5-144">Tworzenie, wybieranie i usuwanie kontekstów oraz zmiana ich nazw</span><span class="sxs-lookup"><span data-stu-id="8e4d5-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="8e4d5-145">Aby utworzyć kontekst, musisz zalogować się do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="8e4d5-146">Polecenie cmdlet `Connect-AzureRmAccount` (lub jego alias — `Login-AzureRmAccount`) ustawia domyślny kontekst używany przez następujące po nim polecenia cmdlet programu Azure PowerShell i pozwala użytkownikowi na dostęp do dowolnych dzierżaw lub subskrypcji, na które pozwalają poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-146">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="8e4d5-147">Aby dodać nowy kontekst po zalogowaniu, użyj polecenia `Set-AzureRmContext` (lub jego aliasu — `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="8e4d5-148">Poprzedni przykład dodaje nowy kontekst, którego obiektem docelowym jest „Contoso Subscription 1”, z użyciem bieżących poświadczeń użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="8e4d5-149">Nowy kontekst ma nazwę „Contoso1”.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="8e4d5-150">Jeśli nie podasz nazwy dla tego kontekstu, będzie używana nazwa domyślna zawierająca identyfikator konta i identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="8e4d5-151">Aby zmienić nazwę istniejącego kontekstu, użyj polecenia cmdlet `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="8e4d5-152">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="8e4d5-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="8e4d5-153">Ten przykład zmienia nazwę kontekstu o nazwie automatycznej `[user1@contoso.org; 123456-7890-1234-564321]` na prostą nazwę „Contoso2”.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="8e4d5-154">Polecenia cmdlet, które zarządzają kontekstami, używają również wypełniania po naciśnięciu klawisza TAB, dzięki czemu możliwe jest szybkie wybieranie kontekstu.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="8e4d5-155">Aby na koniec usunąć kontekst, użyj polecenia cmdlet `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="8e4d5-156">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="8e4d5-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="8e4d5-157">Powoduje zapomnienie kontekstu o nazwie „Contoso2”.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="8e4d5-158">Ten sam kontekst można odtworzyć za pomocą polecenia `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="8e4d5-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="8e4d5-159">Usuwanie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="8e4d5-159">Removing credentials</span></span>

<span data-ttu-id="8e4d5-160">Można usunąć wszystkie poświadczenia i skojarzone konteksty dla użytkownika lub jednostki usługi przy użyciu polecenia `Disconnect-AzureRmAccount` (znanego również jako `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-160">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="8e4d5-161">Polecenie cmdlet `Disconnect-AzureRmAccount` wykonywane bez parametrów usuwa wszystkie poświadczenia i konteksty skojarzone z użytkownikiem lub jednostką usługi w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-161">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="8e4d5-162">Możesz przekazać nazwę użytkownika, jednostkę usługi lub kontekst do konkretnego docelowego podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="8e4d5-163">Korzystanie z zakresów kontekstu</span><span class="sxs-lookup"><span data-stu-id="8e4d5-163">Using context scopes</span></span>

<span data-ttu-id="8e4d5-164">W niektórych okolicznościach kontekst można wybrać, zmienić lub usunąć w sesji programu PowerShell bez wpływu na pozostałe sesje.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="8e4d5-165">Aby zmienić domyślne zachowanie poleceń cmdlet kontekstu, użyj parametru `Scope`.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="8e4d5-166">Zakres `Process` zastępuje domyślne działanie tego parametru, sprawiając, że dotyczy tylko bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="8e4d5-167">Z drugiej strony zakres `CurrentUser` zmienia kontekst we wszystkich sesjach, a nie tylko w bieżącej.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="8e4d5-168">Aby na przykład zmienić kontekst domyślny w bieżącej sesji programu PowerShell bez wpływu na inne okna albo na kontekst używany przy następnym otwarciu sesji, użyj następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="8e4d5-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="8e4d5-169">Jak zapamiętywane jest ustawienie automatycznego zapisywania kontekstu</span><span class="sxs-lookup"><span data-stu-id="8e4d5-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="8e4d5-170">Ustawienie automatycznego zapisywania kontekstu jest zapisywane q katalogu użytkownika programu Azure PowerShell (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="8e4d5-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="8e4d5-171">Niektóre rodzaje kont komputerów mogą nie mieć dostępu do tego katalogu.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="8e4d5-172">W przypadku takich scenariuszy można użyć zmiennej środowiskowej</span><span class="sxs-lookup"><span data-stu-id="8e4d5-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="8e4d5-173">Jeśli zostanie ustawiona na wartość „true”, kontekst będzie zapisywany automatycznie.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="8e4d5-174">Jeśli zostanie ustawiona na wartość „false”, kontekst nie będzie zapisywany.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="8e4d5-175">Zmiany w module AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e4d5-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="8e4d5-176">Nowe polecenia cmdlet do zarządzania kontekstem</span><span class="sxs-lookup"><span data-stu-id="8e4d5-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="8e4d5-177">[Enable-AzureRmContextAutosave][enable] — umożliwia zapisywanie kontekstu między sesjami programu Powershell.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="8e4d5-178">Wszelkie zmiany powodują zmianę kontekstu globalnego.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="8e4d5-179">[Disable-AzureRmContextAutosave][disable] — wyłącza automatyczne zapisywanie kontekstu.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="8e4d5-180">W każdej nowej sesji programu PowerShell konieczne będzie ponowne logowanie się.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="8e4d5-181">[Select-AzureRmContext][select] — umożliwia wybór kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="8e4d5-182">Wszystkie kolejne polecenia cmdlet będą używać poświadczeń z tego kontekstu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="8e4d5-183">[Disconnect-AzureRmAccount][remove-cred] — usuwa wszystkie poświadczenia i konteksty skojarzone z danym kontem.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-183">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="8e4d5-184">[Remove-AzureRmContext][remove-context] — usuwa nazwany kontekst.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="8e4d5-185">[Rename-AzureRmContext][rename] — zmienia nazwę istniejącego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="8e4d5-186">Zmiany istniejących poleceń cmdlet dotyczących profilu</span><span class="sxs-lookup"><span data-stu-id="8e4d5-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="8e4d5-187">[Add-AzureRmAccount][login] — umożliwia określenie zakresu logowania do procesu lub bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="8e4d5-188">Pozwala na nazwanie domyślnego kontekstu po zalogowaniu się.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="8e4d5-189">[Import-AzureRmContext][import] — umożliwia określenie zakresu logowania do procesu lub bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="8e4d5-190">[Set-AzureRmContext][set-context] — umożliwia wybór istniejących nazwanych kontekstów oraz określenie zakresu zmian kontekstu do procesu lub bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e4d5-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
