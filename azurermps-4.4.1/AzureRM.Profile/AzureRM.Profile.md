---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: bc3ccc2c2b0574eee40357fb0079fe22124ea3e6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522833"
---
# <span data-ttu-id="33333-101">AzureRM. profile, moduł</span><span class="sxs-lookup"><span data-stu-id="33333-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="33333-102">Opis</span><span class="sxs-lookup"><span data-stu-id="33333-102">Description</span></span>
<span data-ttu-id="33333-103">Zarządza poświadczeniami i typową konfiguracją dla wszystkich modułów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="33333-104">AzureRM. profile poleceń</span><span class="sxs-lookup"><span data-stu-id="33333-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="33333-105">Dodaj-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="33333-105">Add-AzureRmAccount</span></span>](Add-AzureRmAccount.md)
<span data-ttu-id="33333-106">Dodaje uwierzytelnione konto, które będzie używane dla żądań polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-106">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="33333-107">Dodaj-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="33333-107">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="33333-108">Dodaje punkty końcowe i metadane wystąpienia Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-108">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="33333-109">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-109">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="33333-110">Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="33333-110">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="33333-111">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="33333-111">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="33333-112">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-112">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="33333-113">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33333-113">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="33333-114">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="33333-114">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="33333-115">Nie możesz zbierać danych, aby ulepszyć polecenia cmdlet usługi AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="33333-115">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="33333-116">Dane nie są zbierane, jeśli użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="33333-116">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="33333-117">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="33333-117">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="33333-118">Zezwalaj na zapisywanie i automatyczne ładowanie informacji o poświadczeniach platformy Azure, kontach i subskrypcjach podczas otwierania okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33333-118">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="33333-119">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="33333-119">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="33333-120">Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet usługi AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="33333-120">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="33333-121">Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="33333-121">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="33333-122">Nie są zbierane żadne dane, o ile użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="33333-122">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="33333-123">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-123">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="33333-124">Pobiera metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-124">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="33333-125">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="33333-125">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="33333-126">Wyświetlanie metadanych funkcji automatycznego zapisu kontekstowego, w tym whterh, że kontekst jest automatycznie zapisywany i gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.</span><span class="sxs-lookup"><span data-stu-id="33333-126">Display metadata about the context autosave feature, including whterh the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="33333-127">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="33333-127">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="33333-128">Uzyskiwanie punktów końcowych i metadanych dla wystąpienia usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-128">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="33333-129">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="33333-129">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="33333-130">Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="33333-130">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="33333-131">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="33333-131">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="33333-132">Pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="33333-132">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="33333-133">Import — AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-133">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="33333-134">Ładuje informacje o uwierzytelnianiu platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="33333-134">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="33333-135">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="33333-135">Remove-AzureRmAccount</span></span>](Remove-AzureRmAccount.md)
<span data-ttu-id="33333-136">Usuń wszystkie poświadczenia i konteksty skojarzone z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="33333-136">Remove all credentials and contexts associated with this account.</span></span>

### [<span data-ttu-id="33333-137">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-137">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="33333-138">Usuwanie kontekstu z zestawu dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="33333-138">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="33333-139">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="33333-139">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="33333-140">Umożliwia usunięcie punktów końcowych i metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-140">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="33333-141">Zmień nazwę — AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-141">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="33333-142">Zmienianie nazwy kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-142">Rename an Azure context.</span></span>  <span data-ttu-id="33333-143">Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.</span><span class="sxs-lookup"><span data-stu-id="33333-143">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="33333-144">Rozpoznaj — AzureRmError</span><span class="sxs-lookup"><span data-stu-id="33333-144">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="33333-145">Wyświetlanie szczegółowych informacji o błędach programu PowerShell z rozszerzonymi szczegółami dotyczącymi błędów programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33333-145">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="33333-146">Zapisz — AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-146">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="33333-147">Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33333-147">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="33333-148">Wybierz — AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-148">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="33333-149">Wybierz subskrypcję do lokalizacji docelowej (lub konta, dzierżawy) w poleceniach cmdlet środowiska Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="33333-149">Select a subscription to target (or account, tenant) in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="33333-150">Wysyłanie opinii</span><span class="sxs-lookup"><span data-stu-id="33333-150">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="33333-151">Wysyła opinię do zespołu programu Azure PowerShell za pomocą zestawu interakcyjnych wskazówek.</span><span class="sxs-lookup"><span data-stu-id="33333-151">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="33333-152">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33333-152">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="33333-153">Ustawia dzierżawę, abonament i środowisko dla poleceń cmdlet, które mają być używane w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="33333-153">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="33333-154">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="33333-154">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="33333-155">Ustawia właściwości dla środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-155">Sets properties for an Azure environment.</span></span>

