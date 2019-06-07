---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498679"
---
## <a name="220---june-2019"></a><span data-ttu-id="94c01-101">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="94c01-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94c01-102">Az.Cdn</span></span>
* <span data-ttu-id="94c01-103">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="94c01-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-104">Az.Compute</span></span>
* <span data-ttu-id="94c01-105">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="94c01-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="94c01-106">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="94c01-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94c01-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94c01-107">Az.EventHub</span></span>
* <span data-ttu-id="94c01-108">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="94c01-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="94c01-109">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c01-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-110">Az.Network</span></span>
* <span data-ttu-id="94c01-111">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="94c01-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="94c01-112">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="94c01-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="94c01-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="94c01-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="94c01-114">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="94c01-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="94c01-116">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="94c01-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94c01-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94c01-117">Az.ServiceBus</span></span>
* <span data-ttu-id="94c01-118">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c01-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94c01-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94c01-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="94c01-120">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="94c01-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="94c01-121">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="94c01-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-122">Az.Sql</span></span>
* <span data-ttu-id="94c01-123">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="94c01-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="94c01-124">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="94c01-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="94c01-125">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="94c01-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="94c01-126">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="94c01-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-127">Az.Websites</span></span>
* <span data-ttu-id="94c01-128">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="94c01-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="94c01-129">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="94c01-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94c01-130">Az.ApiManagement</span></span>
* <span data-ttu-id="94c01-131">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="94c01-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="94c01-132">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="94c01-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="94c01-133">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="94c01-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="94c01-134">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="94c01-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="94c01-135">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="94c01-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="94c01-136">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="94c01-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="94c01-137">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="94c01-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="94c01-138">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="94c01-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="94c01-139">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94c01-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="94c01-140">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="94c01-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="94c01-141">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="94c01-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="94c01-142">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="94c01-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="94c01-143">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="94c01-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="94c01-144">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="94c01-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="94c01-145">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="94c01-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="94c01-146">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="94c01-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="94c01-147">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="94c01-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="94c01-148">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="94c01-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="94c01-149">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94c01-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="94c01-150">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="94c01-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="94c01-151">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="94c01-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="94c01-152">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="94c01-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="94c01-153">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="94c01-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="94c01-154">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94c01-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="94c01-155">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="94c01-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="94c01-156">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="94c01-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="94c01-157">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="94c01-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="94c01-158">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="94c01-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="94c01-159">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="94c01-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="94c01-160">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="94c01-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="94c01-161">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="94c01-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="94c01-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="94c01-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="94c01-163">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="94c01-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="94c01-164">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="94c01-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="94c01-165">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="94c01-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="94c01-166">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="94c01-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="94c01-167">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="94c01-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="94c01-168">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="94c01-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="94c01-169">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="94c01-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="94c01-170">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="94c01-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="94c01-171">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="94c01-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="94c01-172">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="94c01-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="94c01-173">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="94c01-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="94c01-174">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="94c01-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="94c01-175">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="94c01-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="94c01-176">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="94c01-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="94c01-177">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="94c01-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="94c01-178">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="94c01-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="94c01-179">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="94c01-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="94c01-180">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="94c01-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="94c01-181">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="94c01-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="94c01-182">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="94c01-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="94c01-183">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="94c01-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="94c01-184">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="94c01-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="94c01-185">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="94c01-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="94c01-186">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="94c01-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="94c01-187">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="94c01-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="94c01-188">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="94c01-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="94c01-189">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="94c01-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="94c01-190">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="94c01-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="94c01-191">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="94c01-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="94c01-192">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="94c01-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="94c01-193">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="94c01-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="94c01-194">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="94c01-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="94c01-195">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="94c01-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="94c01-196">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="94c01-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="94c01-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="94c01-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="94c01-198">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="94c01-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="94c01-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="94c01-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="94c01-200">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="94c01-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="94c01-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="94c01-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="94c01-202">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="94c01-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="94c01-203">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="94c01-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="94c01-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="94c01-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="94c01-205">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="94c01-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="94c01-206">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="94c01-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="94c01-207">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="94c01-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94c01-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-208">Az.Automation</span></span>
* <span data-ttu-id="94c01-209">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="94c01-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="94c01-210">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="94c01-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="94c01-211">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="94c01-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="94c01-212">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="94c01-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="94c01-213">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="94c01-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="94c01-214">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="94c01-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="94c01-215">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="94c01-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-216">Az.Compute</span></span>
* <span data-ttu-id="94c01-217">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="94c01-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="94c01-218">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="94c01-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94c01-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="94c01-220">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="94c01-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94c01-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94c01-221">Az.Monitor</span></span>
* <span data-ttu-id="94c01-222">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="94c01-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-223">Az.Network</span></span>
* <span data-ttu-id="94c01-224">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="94c01-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="94c01-225">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="94c01-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="94c01-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="94c01-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="94c01-227">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="94c01-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-228">Az.Resources</span></span>
* <span data-ttu-id="94c01-229">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="94c01-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-230">Az.Sql</span></span>
* <span data-ttu-id="94c01-231">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="94c01-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="94c01-232">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94c01-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-233">Az.Accounts</span></span>
* <span data-ttu-id="94c01-234">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="94c01-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="94c01-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94c01-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="94c01-236">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="94c01-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="94c01-237">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="94c01-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-238">Az.Compute</span></span>
* <span data-ttu-id="94c01-239">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="94c01-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="94c01-240">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="94c01-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="94c01-241">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="94c01-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="94c01-242">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="94c01-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="94c01-243">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="94c01-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="94c01-244">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="94c01-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="94c01-245">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="94c01-245">Breaking changes</span></span>
    - <span data-ttu-id="94c01-246">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="94c01-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="94c01-247">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="94c01-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="94c01-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="94c01-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="94c01-249">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="94c01-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="94c01-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="94c01-250">Az.Dns</span></span>
* <span data-ttu-id="94c01-251">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="94c01-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="94c01-252">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="94c01-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="94c01-253">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="94c01-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="94c01-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94c01-254">Az.FrontDoor</span></span>
* <span data-ttu-id="94c01-255">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94c01-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="94c01-256">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="94c01-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="94c01-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="94c01-257">Az.HDInsight</span></span>
* <span data-ttu-id="94c01-258">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="94c01-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="94c01-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="94c01-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="94c01-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="94c01-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="94c01-261">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="94c01-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="94c01-262">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="94c01-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="94c01-263">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="94c01-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="94c01-264">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="94c01-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94c01-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94c01-265">Az.Monitor</span></span>
* <span data-ttu-id="94c01-266">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="94c01-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="94c01-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="94c01-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="94c01-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="94c01-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="94c01-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="94c01-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="94c01-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="94c01-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="94c01-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="94c01-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="94c01-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="94c01-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="94c01-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94c01-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94c01-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94c01-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94c01-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94c01-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94c01-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94c01-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94c01-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94c01-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94c01-278">[Więcej](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="94c01-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="94c01-279">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="94c01-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-280">Az.Network</span></span>
* <span data-ttu-id="94c01-281">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="94c01-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="94c01-282">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="94c01-282">New cmdlets</span></span>
        - <span data-ttu-id="94c01-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94c01-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="94c01-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94c01-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="94c01-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94c01-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="94c01-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94c01-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="94c01-287">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="94c01-287">Updated cmdlets</span></span>
        - <span data-ttu-id="94c01-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="94c01-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="94c01-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="94c01-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="94c01-290">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="94c01-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="94c01-291">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="94c01-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="94c01-292">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="94c01-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="94c01-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="94c01-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="94c01-294">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="94c01-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="94c01-295">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="94c01-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="94c01-296">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="94c01-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="94c01-298">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="94c01-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="94c01-299">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="94c01-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="94c01-300">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="94c01-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="94c01-301">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="94c01-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="94c01-302">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="94c01-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="94c01-303">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="94c01-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="94c01-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="94c01-304">Az.Relay</span></span>
* <span data-ttu-id="94c01-305">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="94c01-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94c01-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94c01-306">Az.ServiceBus</span></span>
* <span data-ttu-id="94c01-307">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="94c01-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94c01-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-308">Az.Storage</span></span>
* <span data-ttu-id="94c01-309">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="94c01-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="94c01-310">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="94c01-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="94c01-311">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="94c01-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="94c01-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="94c01-313">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="94c01-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="94c01-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="94c01-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="94c01-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-317">Az.Websites</span></span>
* <span data-ttu-id="94c01-318">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="94c01-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="94c01-319">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="94c01-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="94c01-320">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="94c01-321">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="94c01-321">Highlights since the last major release</span></span>
* <span data-ttu-id="94c01-322">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="94c01-322">General availability of `Az` module</span></span>
* <span data-ttu-id="94c01-323">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="94c01-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="94c01-324">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="94c01-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="94c01-325">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="94c01-326">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="94c01-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94c01-327">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="94c01-328">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="94c01-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94c01-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-329">Az.Accounts</span></span>
* <span data-ttu-id="94c01-330">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="94c01-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="94c01-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94c01-331">Az.Batch</span></span>
* <span data-ttu-id="94c01-332">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94c01-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94c01-333">Az.Cdn</span></span>
* <span data-ttu-id="94c01-334">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="94c01-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94c01-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="94c01-336">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-337">Az.Compute</span></span>
* <span data-ttu-id="94c01-338">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="94c01-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="94c01-339">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94c01-340">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="94c01-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94c01-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94c01-341">Az.DataFactory</span></span>
* <span data-ttu-id="94c01-342">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="94c01-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94c01-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="94c01-344">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="94c01-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="94c01-345">Az.EventGrid</span></span>
* <span data-ttu-id="94c01-346">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="94c01-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94c01-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94c01-347">Az.EventHub</span></span>
* <span data-ttu-id="94c01-348">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="94c01-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="94c01-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="94c01-349">Az.HDInsight</span></span>
* <span data-ttu-id="94c01-350">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94c01-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94c01-351">Az.IotHub</span></span>
* <span data-ttu-id="94c01-352">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94c01-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94c01-353">Az.KeyVault</span></span>
* <span data-ttu-id="94c01-354">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94c01-355">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="94c01-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="94c01-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="94c01-356">Az.MachineLearning</span></span>
* <span data-ttu-id="94c01-357">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="94c01-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="94c01-358">Az.Media</span></span>
* <span data-ttu-id="94c01-359">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94c01-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94c01-360">Az.Monitor</span></span>
  * <span data-ttu-id="94c01-361">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="94c01-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="94c01-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="94c01-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="94c01-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="94c01-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="94c01-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="94c01-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="94c01-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="94c01-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="94c01-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="94c01-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="94c01-367">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="94c01-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-368">Az.Network</span></span>
* <span data-ttu-id="94c01-369">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94c01-370">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="94c01-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="94c01-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="94c01-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="94c01-372">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94c01-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94c01-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="94c01-374">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="94c01-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="94c01-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="94c01-376">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="94c01-378">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94c01-379">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="94c01-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="94c01-380">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="94c01-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="94c01-381">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="94c01-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="94c01-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="94c01-382">Az.RedisCache</span></span>
* <span data-ttu-id="94c01-383">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-384">Az.Resources</span></span>
* <span data-ttu-id="94c01-385">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="94c01-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-386">Az.Sql</span></span>
* <span data-ttu-id="94c01-387">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="94c01-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="94c01-388">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94c01-389">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="94c01-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="94c01-390">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="94c01-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="94c01-391">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="94c01-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="94c01-392">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="94c01-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="94c01-393">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="94c01-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-394">Az.Websites</span></span>
* <span data-ttu-id="94c01-395">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="94c01-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="94c01-396">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="94c01-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94c01-397">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="94c01-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="94c01-398">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="94c01-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="94c01-399">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="94c01-400">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="94c01-400">Highlights since the last major release</span></span>
* <span data-ttu-id="94c01-401">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="94c01-401">General availability of `Az` module</span></span>
* <span data-ttu-id="94c01-402">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="94c01-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="94c01-403">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="94c01-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="94c01-404">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="94c01-405">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="94c01-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94c01-406">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="94c01-407">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="94c01-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94c01-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-408">Az.Accounts</span></span>
* <span data-ttu-id="94c01-409">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="94c01-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="94c01-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94c01-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="94c01-411">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="94c01-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="94c01-412">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="94c01-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94c01-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-413">Az.Automation</span></span>
* <span data-ttu-id="94c01-414">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="94c01-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="94c01-415">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="94c01-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="94c01-416">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-417">Az.Compute</span></span>
* <span data-ttu-id="94c01-418">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="94c01-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="94c01-419">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="94c01-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="94c01-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="94c01-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="94c01-421">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="94c01-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94c01-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94c01-422">Az.DataFactory</span></span>
* <span data-ttu-id="94c01-423">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="94c01-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="94c01-424">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="94c01-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-425">Az.Resources</span></span>
* <span data-ttu-id="94c01-426">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="94c01-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="94c01-427">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="94c01-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="94c01-428">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="94c01-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="94c01-429">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="94c01-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="94c01-430">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="94c01-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="94c01-431">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="94c01-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-432">Az.Sql</span></span>
* <span data-ttu-id="94c01-433">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="94c01-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94c01-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-434">Az.Storage</span></span>
* <span data-ttu-id="94c01-435">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="94c01-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="94c01-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="94c01-436">New-AzStorageContext</span></span>
* <span data-ttu-id="94c01-437">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="94c01-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="94c01-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="94c01-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="94c01-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="94c01-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="94c01-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94c01-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="94c01-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94c01-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="94c01-442">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="94c01-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="94c01-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94c01-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="94c01-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94c01-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="94c01-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94c01-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="94c01-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94c01-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="94c01-447">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="94c01-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="94c01-448">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="94c01-448">Highlights since the last major release</span></span>
* <span data-ttu-id="94c01-449">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="94c01-449">General availability of `Az` module</span></span>
* <span data-ttu-id="94c01-450">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="94c01-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="94c01-451">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="94c01-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="94c01-452">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="94c01-453">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="94c01-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94c01-454">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="94c01-455">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="94c01-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94c01-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-456">Az.Automation</span></span>
* <span data-ttu-id="94c01-457">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="94c01-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="94c01-458">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="94c01-458">Dynamic grouping</span></span>
    * <span data-ttu-id="94c01-459">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="94c01-459">Pre-Post script</span></span>
    * <span data-ttu-id="94c01-460">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="94c01-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-461">Az.Compute</span></span>
* <span data-ttu-id="94c01-462">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="94c01-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="94c01-463">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="94c01-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94c01-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94c01-464">Az.KeyVault</span></span>
* <span data-ttu-id="94c01-465">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="94c01-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-466">Az.Network</span></span>
* <span data-ttu-id="94c01-467">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="94c01-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="94c01-468">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="94c01-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="94c01-470">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="94c01-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="94c01-471">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="94c01-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-472">Az.Resources</span></span>
* <span data-ttu-id="94c01-473">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94c01-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="94c01-474">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="94c01-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-475">Az.Sql</span></span>
* <span data-ttu-id="94c01-476">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="94c01-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94c01-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-477">Az.Storage</span></span>
* <span data-ttu-id="94c01-478">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="94c01-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="94c01-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="94c01-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="94c01-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="94c01-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="94c01-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="94c01-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="94c01-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="94c01-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="94c01-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="94c01-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="94c01-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="94c01-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-485">Az.Websites</span></span>
* <span data-ttu-id="94c01-486">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="94c01-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="94c01-487">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="94c01-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94c01-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-488">Az.Accounts</span></span>
* <span data-ttu-id="94c01-489">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="94c01-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="94c01-490">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94c01-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-491">Az.Automation</span></span>
* <span data-ttu-id="94c01-492">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="94c01-493">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="94c01-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="94c01-494">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="94c01-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94c01-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94c01-495">Az.Cdn</span></span>
* <span data-ttu-id="94c01-496">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="94c01-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-497">Az.Compute</span></span>
* <span data-ttu-id="94c01-498">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="94c01-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94c01-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94c01-499">Az.DataFactory</span></span>
* <span data-ttu-id="94c01-500">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="94c01-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="94c01-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="94c01-501">Az.LogicApp</span></span>
* <span data-ttu-id="94c01-502">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="94c01-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-503">Az.Network</span></span>
* <span data-ttu-id="94c01-504">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="94c01-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="94c01-506">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="94c01-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="94c01-507">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="94c01-507">SDK Update</span></span>
* <span data-ttu-id="94c01-508">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="94c01-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="94c01-509">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="94c01-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-510">Az.Resources</span></span>
* <span data-ttu-id="94c01-511">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="94c01-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="94c01-512">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="94c01-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="94c01-513">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="94c01-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="94c01-514">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="94c01-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="94c01-515">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="94c01-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="94c01-516">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="94c01-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-517">Az.Sql</span></span>
* <span data-ttu-id="94c01-518">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="94c01-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="94c01-519">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="94c01-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94c01-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-520">Az.Storage</span></span>
* <span data-ttu-id="94c01-521">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="94c01-522">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="94c01-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94c01-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="94c01-524">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94c01-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-525">Az.Automation</span></span>
* <span data-ttu-id="94c01-526">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="94c01-527">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="94c01-528">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="94c01-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94c01-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="94c01-530">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="94c01-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-531">Az.Compute</span></span>
* <span data-ttu-id="94c01-532">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="94c01-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="94c01-533">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="94c01-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="94c01-534">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="94c01-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="94c01-535">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="94c01-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94c01-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="94c01-537">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="94c01-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94c01-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94c01-538">Az.EventHub</span></span>
* <span data-ttu-id="94c01-539">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="94c01-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="94c01-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94c01-540">Az.KeyVault</span></span>
* <span data-ttu-id="94c01-541">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94c01-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="94c01-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="94c01-542">Az.LogicApp</span></span>
* <span data-ttu-id="94c01-543">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="94c01-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="94c01-544">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="94c01-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="94c01-545">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="94c01-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="94c01-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94c01-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="94c01-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94c01-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="94c01-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94c01-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="94c01-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94c01-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="94c01-550">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="94c01-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="94c01-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="94c01-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="94c01-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="94c01-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="94c01-555">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="94c01-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94c01-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94c01-556">Az.Monitor</span></span>
* <span data-ttu-id="94c01-557">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="94c01-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-558">Az.Network</span></span>
* <span data-ttu-id="94c01-559">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="94c01-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94c01-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94c01-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="94c01-561">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="94c01-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="94c01-562">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="94c01-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="94c01-563">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="94c01-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="94c01-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-564">Az.Resources</span></span>
* <span data-ttu-id="94c01-565">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="94c01-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="94c01-566">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="94c01-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="94c01-567">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="94c01-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="94c01-568">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="94c01-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-569">Az.Sql</span></span>
* <span data-ttu-id="94c01-570">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="94c01-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="94c01-571">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="94c01-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-572">Az.Websites</span></span>
* <span data-ttu-id="94c01-573">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="94c01-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="94c01-574">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94c01-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-575">Az.Accounts</span></span>
* <span data-ttu-id="94c01-576">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="94c01-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="94c01-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94c01-577">Az.AnalysisServices</span></span>
<span data-ttu-id="94c01-578">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="94c01-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-579">Az.Compute</span></span>
* <span data-ttu-id="94c01-580">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="94c01-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="94c01-581">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="94c01-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="94c01-582">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="94c01-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-583">Az.RecoveryServices</span></span>
<span data-ttu-id="94c01-584">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="94c01-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-585">Az.Resources</span></span>
* <span data-ttu-id="94c01-586">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="94c01-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="94c01-587">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="94c01-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="94c01-588">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="94c01-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="94c01-589">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="94c01-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-590">Az.Sql</span></span>
* <span data-ttu-id="94c01-591">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94c01-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="94c01-592">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="94c01-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="94c01-593">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="94c01-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="94c01-594">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94c01-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-595">Az.Accounts</span></span>
* <span data-ttu-id="94c01-596">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="94c01-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="94c01-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94c01-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="94c01-598">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="94c01-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="94c01-600">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="94c01-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="94c01-601">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94c01-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-602">Az.Accounts</span></span>
* <span data-ttu-id="94c01-603">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="94c01-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94c01-604">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94c01-605">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="94c01-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="94c01-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="94c01-606">Az.Aks</span></span>
* <span data-ttu-id="94c01-607">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94c01-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-608">Az.Automation</span></span>
* <span data-ttu-id="94c01-609">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="94c01-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="94c01-610">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94c01-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94c01-611">Az.Cdn</span></span>
* <span data-ttu-id="94c01-612">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-613">Az.Compute</span></span>
* <span data-ttu-id="94c01-614">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="94c01-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="94c01-615">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="94c01-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="94c01-616">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="94c01-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="94c01-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="94c01-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="94c01-618">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94c01-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94c01-619">Az.DataFactory</span></span>
* <span data-ttu-id="94c01-620">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="94c01-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94c01-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="94c01-622">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="94c01-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="94c01-623">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="94c01-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="94c01-624">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94c01-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94c01-625">Az.IotHub</span></span>
* <span data-ttu-id="94c01-626">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="94c01-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94c01-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94c01-627">Az.KeyVault</span></span>
* <span data-ttu-id="94c01-628">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-629">Az.Network</span></span>
* <span data-ttu-id="94c01-630">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-631">Az.Resources</span></span>
* <span data-ttu-id="94c01-632">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="94c01-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="94c01-633">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="94c01-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="94c01-634">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="94c01-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="94c01-635">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="94c01-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="94c01-636">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="94c01-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="94c01-637">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94c01-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="94c01-638">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="94c01-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94c01-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94c01-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="94c01-640">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="94c01-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="94c01-641">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="94c01-641">Fix some error messages.</span></span>
* <span data-ttu-id="94c01-642">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94c01-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="94c01-643">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="94c01-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="94c01-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="94c01-644">Az.SignalR</span></span>
* <span data-ttu-id="94c01-645">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-646">Az.Sql</span></span>
* <span data-ttu-id="94c01-647">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94c01-648">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="94c01-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="94c01-649">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="94c01-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="94c01-650">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="94c01-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94c01-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-651">Az.Storage</span></span>
* <span data-ttu-id="94c01-652">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94c01-653">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="94c01-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="94c01-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="94c01-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="94c01-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="94c01-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="94c01-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="94c01-656">Az.TrafficManager</span></span>
* <span data-ttu-id="94c01-657">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-658">Az.Websites</span></span>
* <span data-ttu-id="94c01-659">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="94c01-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94c01-660">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="94c01-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="94c01-661">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="94c01-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="94c01-662">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94c01-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-663">Az.Accounts</span></span>
* <span data-ttu-id="94c01-664">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="94c01-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-665">Az.Compute</span></span>
* <span data-ttu-id="94c01-666">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="94c01-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="94c01-667">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="94c01-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="94c01-668">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94c01-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="94c01-670">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="94c01-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="94c01-671">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="94c01-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="94c01-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="94c01-672">Az.EventGrid</span></span>
* <span data-ttu-id="94c01-673">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="94c01-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="94c01-674">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="94c01-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="94c01-675">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="94c01-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="94c01-676">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="94c01-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="94c01-677">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="94c01-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="94c01-678">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="94c01-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="94c01-679">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="94c01-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="94c01-680">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="94c01-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="94c01-681">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="94c01-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="94c01-682">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="94c01-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="94c01-683">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="94c01-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="94c01-684">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94c01-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94c01-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94c01-685">Az.IotHub</span></span>
* <span data-ttu-id="94c01-686">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="94c01-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="94c01-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="94c01-687">Az.LogicApp</span></span>
* <span data-ttu-id="94c01-688">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="94c01-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-689">Az.Resources</span></span>
* <span data-ttu-id="94c01-690">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="94c01-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="94c01-691">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="94c01-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="94c01-692">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="94c01-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="94c01-693">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="94c01-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="94c01-694">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="94c01-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="94c01-695">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="94c01-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="94c01-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="94c01-696">Az.SignalR</span></span>
* <span data-ttu-id="94c01-697">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-698">Az.Sql</span></span>
* <span data-ttu-id="94c01-699">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="94c01-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94c01-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-700">Az.Storage</span></span>
* <span data-ttu-id="94c01-701">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="94c01-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="94c01-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="94c01-702">New-AzStorageContext</span></span>
* <span data-ttu-id="94c01-703">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="94c01-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="94c01-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="94c01-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-705">Az.Websites</span></span>
* <span data-ttu-id="94c01-706">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="94c01-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="94c01-707">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="94c01-708">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="94c01-709">Ogólne</span><span class="sxs-lookup"><span data-stu-id="94c01-709">General</span></span>

- <span data-ttu-id="94c01-710">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="94c01-710">General Availability of Az Module</span></span>
- <span data-ttu-id="94c01-711">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="94c01-711">Online help for each module</span></span>
- <span data-ttu-id="94c01-712">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="94c01-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="94c01-713">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="94c01-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="94c01-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-714">Az.Accounts</span></span>
- <span data-ttu-id="94c01-715">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94c01-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="94c01-716">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="94c01-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="94c01-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94c01-717">Az.ApiManagement</span></span>
- <span data-ttu-id="94c01-718">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="94c01-718">Fixes for #7002</span></span>
- <span data-ttu-id="94c01-719">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="94c01-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94c01-720">Az.Batch</span></span>
- <span data-ttu-id="94c01-721">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="94c01-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="94c01-722">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="94c01-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="94c01-723">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="94c01-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="94c01-724">Az.Billing</span></span>
- <span data-ttu-id="94c01-725">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="94c01-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="94c01-726">Az.CognitivServices</span></span>
- <span data-ttu-id="94c01-727">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="94c01-728">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="94c01-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="94c01-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="94c01-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="94c01-730">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="94c01-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="94c01-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="94c01-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="94c01-732">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="94c01-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="94c01-734">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="94c01-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94c01-735">Az.Monitor</span></span>
- <span data-ttu-id="94c01-736">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="94c01-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94c01-737">Az.KeyVault</span></span>
- <span data-ttu-id="94c01-738">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="94c01-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="94c01-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="94c01-739">Az.MachineLearning</span></span>
- <span data-ttu-id="94c01-740">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="94c01-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="94c01-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="94c01-741">Az.Media</span></span>
- <span data-ttu-id="94c01-742">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="94c01-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="94c01-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-743">Az.Network</span></span>
<span data-ttu-id="94c01-744">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="94c01-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="94c01-745">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="94c01-745">New cmdlets added:</span></span>
        - <span data-ttu-id="94c01-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94c01-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94c01-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94c01-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94c01-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94c01-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94c01-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94c01-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94c01-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94c01-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94c01-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="94c01-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="94c01-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="94c01-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="94c01-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="94c01-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="94c01-754">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94c01-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="94c01-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94c01-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="94c01-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="94c01-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="94c01-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="94c01-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="94c01-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94c01-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="94c01-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="94c01-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="94c01-760">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="94c01-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="94c01-761">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94c01-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="94c01-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94c01-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="94c01-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94c01-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="94c01-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94c01-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="94c01-765">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="94c01-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="94c01-766">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="94c01-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94c01-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="94c01-768">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="94c01-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94c01-769">Az.Profile</span></span>
- <span data-ttu-id="94c01-770">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94c01-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="94c01-772">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="94c01-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-773">Az.Resources</span></span>
- <span data-ttu-id="94c01-774">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="94c01-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94c01-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="94c01-776">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="94c01-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="94c01-777">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="94c01-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="94c01-778">Az.SIgnalR</span></span>
- <span data-ttu-id="94c01-779">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="94c01-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="94c01-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-780">Az.Sql</span></span>
- <span data-ttu-id="94c01-781">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="94c01-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="94c01-782">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="94c01-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="94c01-783">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="94c01-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-784">Az.Storage</span></span>
- <span data-ttu-id="94c01-785">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="94c01-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-786">Az.Websites</span></span>
- <span data-ttu-id="94c01-787">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="94c01-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="94c01-788">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="94c01-789">Ogólne</span><span class="sxs-lookup"><span data-stu-id="94c01-789">General</span></span>

* <span data-ttu-id="94c01-790">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="94c01-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="94c01-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-791">Az.Compute</span></span>

* <span data-ttu-id="94c01-792">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="94c01-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="94c01-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="94c01-794">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="94c01-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="94c01-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94c01-795">Az.FrontDoor</span></span>

* <span data-ttu-id="94c01-796">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="94c01-796">Fixed some broken links</span></span>
    - <span data-ttu-id="94c01-797">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="94c01-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="94c01-798">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="94c01-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="94c01-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94c01-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="94c01-800">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94c01-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="94c01-801">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94c01-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="94c01-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-802">Az.Resources</span></span>

* <span data-ttu-id="94c01-803">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="94c01-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="94c01-804">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="94c01-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="94c01-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-805">Az.Sql</span></span>

* <span data-ttu-id="94c01-806">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="94c01-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="94c01-807">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="94c01-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="94c01-808">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="94c01-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="94c01-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-809">Az.Storage</span></span>

* <span data-ttu-id="94c01-810">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="94c01-811">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="94c01-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="94c01-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="94c01-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="94c01-813">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="94c01-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="94c01-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="94c01-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="94c01-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="94c01-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="94c01-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-816">Az.Websites</span></span>

* <span data-ttu-id="94c01-817">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94c01-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="94c01-818">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="94c01-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="94c01-819">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="94c01-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="94c01-820">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="94c01-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94c01-821">Az.ApiManagement</span></span>
* <span data-ttu-id="94c01-822">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="94c01-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="94c01-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94c01-823">Az.Automation</span></span>
* <span data-ttu-id="94c01-824">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="94c01-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="94c01-825">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="94c01-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="94c01-826">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="94c01-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="94c01-827">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="94c01-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="94c01-828">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="94c01-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="94c01-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-829">Az.Compute</span></span>
* <span data-ttu-id="94c01-830">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="94c01-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="94c01-831">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="94c01-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="94c01-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="94c01-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="94c01-833">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="94c01-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="94c01-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="94c01-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="94c01-835">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="94c01-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="94c01-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-836">Az.Network</span></span>
* <span data-ttu-id="94c01-837">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="94c01-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="94c01-838">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="94c01-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="94c01-839">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="94c01-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="94c01-840">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94c01-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="94c01-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="94c01-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="94c01-842">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="94c01-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="94c01-843">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="94c01-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="94c01-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="94c01-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="94c01-845">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="94c01-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="94c01-846">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="94c01-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="94c01-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="94c01-847">Az.Relay</span></span>
* <span data-ttu-id="94c01-848">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="94c01-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="94c01-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-849">Az.Resources</span></span>
* <span data-ttu-id="94c01-850">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="94c01-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="94c01-851">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="94c01-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="94c01-852">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="94c01-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="94c01-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94c01-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="94c01-854">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="94c01-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="94c01-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-855">Az.Sql</span></span>
* <span data-ttu-id="94c01-856">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="94c01-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="94c01-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94c01-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94c01-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94c01-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94c01-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94c01-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94c01-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94c01-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94c01-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94c01-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="94c01-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94c01-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="94c01-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94c01-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="94c01-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94c01-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="94c01-865">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="94c01-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="94c01-866">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="94c01-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="94c01-867">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="94c01-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="94c01-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="94c01-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="94c01-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="94c01-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="94c01-870">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="94c01-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="94c01-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="94c01-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="94c01-872">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="94c01-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="94c01-873">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="94c01-874">Ogólne</span><span class="sxs-lookup"><span data-stu-id="94c01-874">General</span></span>
* <span data-ttu-id="94c01-875">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="94c01-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="94c01-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94c01-876">Az.Profile</span></span>
* <span data-ttu-id="94c01-877">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="94c01-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="94c01-878">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="94c01-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="94c01-879">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="94c01-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="94c01-880">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="94c01-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="94c01-881">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="94c01-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="94c01-882">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="94c01-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="94c01-883">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="94c01-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="94c01-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94c01-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="94c01-885">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="94c01-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-886">Az.Compute</span></span>
* <span data-ttu-id="94c01-887">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="94c01-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="94c01-888">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="94c01-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="94c01-889">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="94c01-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94c01-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="94c01-891">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="94c01-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="94c01-892">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="94c01-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="94c01-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="94c01-893">Az.Insights</span></span>
* <span data-ttu-id="94c01-894">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="94c01-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="94c01-895">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="94c01-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="94c01-896">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="94c01-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="94c01-897">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="94c01-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-898">Az.Network</span></span>
* <span data-ttu-id="94c01-899">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="94c01-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="94c01-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="94c01-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="94c01-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="94c01-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="94c01-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="94c01-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="94c01-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="94c01-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="94c01-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="94c01-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="94c01-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="94c01-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="94c01-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="94c01-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="94c01-907">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="94c01-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-908">Az.Resources</span></span>
* <span data-ttu-id="94c01-909">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="94c01-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="94c01-910">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="94c01-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94c01-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94c01-911">Az.ServiceBus</span></span>
* <span data-ttu-id="94c01-912">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="94c01-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94c01-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94c01-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="94c01-914">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="94c01-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="94c01-915">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="94c01-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="94c01-916">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="94c01-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="94c01-917">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="94c01-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="94c01-918">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="94c01-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="94c01-919">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="94c01-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94c01-920">Az.Profile</span></span>
* <span data-ttu-id="94c01-921">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="94c01-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="94c01-922">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="94c01-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-923">Az.Compute</span></span>
* <span data-ttu-id="94c01-924">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="94c01-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="94c01-925">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c01-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94c01-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94c01-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="94c01-927">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="94c01-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="94c01-928">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="94c01-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="94c01-929">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="94c01-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="94c01-930">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="94c01-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="94c01-931">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="94c01-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-932">Az.Network</span></span>
* <span data-ttu-id="94c01-933">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="94c01-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="94c01-934">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c01-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-935">Az.Resources</span></span>
* <span data-ttu-id="94c01-936">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="94c01-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="94c01-937">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="94c01-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="94c01-938">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="94c01-939">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="94c01-939">Azure.Storage</span></span>
* <span data-ttu-id="94c01-940">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="94c01-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="94c01-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="94c01-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="94c01-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="94c01-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="94c01-943">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="94c01-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="94c01-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="94c01-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="94c01-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94c01-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="94c01-946">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="94c01-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94c01-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94c01-947">Az.Compute</span></span>
* <span data-ttu-id="94c01-948">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="94c01-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="94c01-949">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="94c01-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="94c01-950">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="94c01-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="94c01-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="94c01-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="94c01-952">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="94c01-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94c01-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94c01-953">Az.Network</span></span>
* <span data-ttu-id="94c01-954">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="94c01-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="94c01-955">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="94c01-955">new cmdlets added</span></span>
    - <span data-ttu-id="94c01-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94c01-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="94c01-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94c01-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="94c01-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94c01-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="94c01-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94c01-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="94c01-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="94c01-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="94c01-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="94c01-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="94c01-962">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="94c01-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="94c01-963">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="94c01-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="94c01-964">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="94c01-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="94c01-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="94c01-965">Az.RedisCache</span></span>
* <span data-ttu-id="94c01-966">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="94c01-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="94c01-967">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="94c01-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="94c01-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94c01-968">Az.Resources</span></span>
* <span data-ttu-id="94c01-969">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="94c01-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="94c01-970">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="94c01-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="94c01-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94c01-971">Az.Sql</span></span>
* <span data-ttu-id="94c01-972">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="94c01-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94c01-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94c01-973">Az.Websites</span></span>
* <span data-ttu-id="94c01-974">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="94c01-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="94c01-975">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="94c01-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="94c01-976">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="94c01-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="94c01-977">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="94c01-977">Initial Release</span></span>