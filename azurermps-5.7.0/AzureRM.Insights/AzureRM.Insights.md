---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522817"
---
# <span data-ttu-id="37edd-101">Moduł AzureRM. Insights</span><span class="sxs-lookup"><span data-stu-id="37edd-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="37edd-102">Opis</span><span class="sxs-lookup"><span data-stu-id="37edd-102">Description</span></span>
<span data-ttu-id="37edd-103">Ten temat zawiera tematy pomocy dotyczące apletów poleceń usługi Azure Insights.</span><span class="sxs-lookup"><span data-stu-id="37edd-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="37edd-104">AzureRM. Informacje o poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="37edd-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="37edd-105">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37edd-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="37edd-106">Umożliwia utworzenie ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="37edd-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="37edd-107">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="37edd-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="37edd-108">Dodanie lub zastąpienie reguły alertu dziennika.</span><span class="sxs-lookup"><span data-stu-id="37edd-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="37edd-109">Dodaj-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="37edd-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="37edd-110">Tworzy nowy profil dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="37edd-110">Creates a new activity log profile.</span></span> <span data-ttu-id="37edd-111">Ten profil służy do archiwizowania dziennika aktywności na koncie usługi Azure Storage lub przesyłania strumieniowego do centrum zdarzeń platformy Azure w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="37edd-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="37edd-112">**Konto magazynu** — obsługiwane jest tylko standardowe konto magazynu (konto magazynu Premium jest nieobsługiwane).</span><span class="sxs-lookup"><span data-stu-id="37edd-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="37edd-113">Być może jest to typ ARM lub klasyczny.</span><span class="sxs-lookup"><span data-stu-id="37edd-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="37edd-114">Jeśli jest on zarejestrowany na koncie magazynu, koszty przechowywania dziennika aktywności są rozliczane według zwykłych standardowych stawek za składowanie.</span><span class="sxs-lookup"><span data-stu-id="37edd-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="37edd-115">Tylko jeden profil dziennika dla jednej subskrypcji może zawierać tylko jedno konto magazynu na jedną subskrypcję, aby wyeksportować dziennik aktywności.</span><span class="sxs-lookup"><span data-stu-id="37edd-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="37edd-116">**Centrum zdarzeń** — tylko jeden profil dziennika dla jednej subskrypcji może mieć tylko jeden centrum zdarzeń na subskrypcję, aby wyeksportować dziennik aktywności.</span><span class="sxs-lookup"><span data-stu-id="37edd-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="37edd-117">Jeśli dziennik aktywności jest przesyłany strumieniowo do centrum zdarzeń, będą obowiązywać standardowe ceny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="37edd-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="37edd-118">Zdarzenia w dzienniku aktywności mogą dotyczyć regionu lub mogą być "globalnymi".</span><span class="sxs-lookup"><span data-stu-id="37edd-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="37edd-119">Globalnym względnie oznacza, że te zdarzenia są regionem agnostics i są niezależne od regionu, w rzeczywistości większość wydarzeń należy do tej kategorii.</span><span class="sxs-lookup"><span data-stu-id="37edd-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="37edd-120">Jeśli profil dziennika aktywności jest ustawiony na podstawie portalu, domyślnie dodawany jest komunikat "globalny" wraz z dowolnym innym regionem wybranym w interfejsie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="37edd-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="37edd-121">W przypadku korzystania z polecenia cmdlet lokalizacja "Global" musi być jawnie wymieniona poza dowolnym innym regionem.</span><span class="sxs-lookup"><span data-stu-id="37edd-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="37edd-122">**Uwaga** : w **przypadku niepowodzenia ustawienia "globalne" w lokalizacjach nie będzie można eksportować dziennika aktywności.**</span><span class="sxs-lookup"><span data-stu-id="37edd-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="37edd-123">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="37edd-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="37edd-124">Umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.</span><span class="sxs-lookup"><span data-stu-id="37edd-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="37edd-125">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="37edd-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="37edd-126">Umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.</span><span class="sxs-lookup"><span data-stu-id="37edd-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="37edd-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="37edd-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="37edd-128">Wyłącza alert dziennika aktywności i ustawia jego Tagi.</span><span class="sxs-lookup"><span data-stu-id="37edd-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="37edd-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="37edd-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="37edd-130">Włącza alert dziennika aktywności i ustawia jego Tagi.</span><span class="sxs-lookup"><span data-stu-id="37edd-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="37edd-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="37edd-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="37edd-132">Pobiera grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="37edd-132">Gets action group(s).</span></span>

### [<span data-ttu-id="37edd-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="37edd-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="37edd-134">Pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="37edd-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="37edd-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="37edd-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="37edd-136">Pobiera historię alertów.</span><span class="sxs-lookup"><span data-stu-id="37edd-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="37edd-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="37edd-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="37edd-138">Pobiera reguły alertów.</span><span class="sxs-lookup"><span data-stu-id="37edd-138">Gets alert rules.</span></span>

### [<span data-ttu-id="37edd-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="37edd-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="37edd-140">Pobiera historię autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="37edd-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="37edd-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37edd-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="37edd-142">Pobiera ustawienia autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="37edd-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="37edd-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="37edd-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="37edd-144">Pobiera zarejestrowane kategorie i ziarno czasu.</span><span class="sxs-lookup"><span data-stu-id="37edd-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="37edd-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="37edd-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="37edd-146">Pobiera dziennik zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="37edd-146">Gets a log of events.</span></span>

### [<span data-ttu-id="37edd-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="37edd-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="37edd-148">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="37edd-148">Gets a log profile.</span></span>

### [<span data-ttu-id="37edd-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="37edd-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="37edd-150">Pobiera wartości metryki zasobu.</span><span class="sxs-lookup"><span data-stu-id="37edd-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="37edd-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="37edd-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="37edd-152">Pobiera definicje metryk.</span><span class="sxs-lookup"><span data-stu-id="37edd-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="37edd-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="37edd-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="37edd-154">Pobiera metryki użycia zasobu.</span><span class="sxs-lookup"><span data-stu-id="37edd-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="37edd-155">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="37edd-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="37edd-156">Tworzy obiekt odwołania do obiektu Actions w pamięci.</span><span class="sxs-lookup"><span data-stu-id="37edd-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="37edd-157">Nowe — AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="37edd-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="37edd-158">Tworzy nowy odbiorcę grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="37edd-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="37edd-159">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="37edd-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="37edd-160">Umożliwia utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="37edd-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="37edd-161">Nowe — AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="37edd-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="37edd-162">Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="37edd-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="37edd-163">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="37edd-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="37edd-164">Tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="37edd-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="37edd-165">Nowe — AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="37edd-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="37edd-166">Umożliwia utworzenie powiadomienia e-mail autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="37edd-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="37edd-167">Nowe — AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="37edd-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="37edd-168">Tworzy profil autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="37edd-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="37edd-169">Nowe — AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="37edd-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="37edd-170">Umożliwia utworzenie reguły skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="37edd-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="37edd-171">Nowe — AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="37edd-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="37edd-172">Umożliwia utworzenie elementu webhook autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="37edd-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="37edd-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="37edd-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="37edd-174">Usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="37edd-174">Removes an action group.</span></span>

### [<span data-ttu-id="37edd-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="37edd-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="37edd-176">Usuwa alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="37edd-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="37edd-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="37edd-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="37edd-178">Usuwa regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="37edd-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="37edd-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37edd-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="37edd-180">Usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="37edd-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="37edd-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="37edd-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="37edd-182">Usuwa profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="37edd-182">Removes a log profile.</span></span>

### [<span data-ttu-id="37edd-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="37edd-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="37edd-184">Umożliwia utworzenie nowej lub zaktualizowanie istniejącej grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="37edd-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="37edd-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="37edd-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="37edd-186">Tworzy nowy lub ustawia istniejący alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="37edd-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="37edd-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="37edd-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="37edd-188">Ustawia ustawienia dzienników i metryk dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="37edd-188">Sets the logs and metrics settings for the resource.</span></span>

