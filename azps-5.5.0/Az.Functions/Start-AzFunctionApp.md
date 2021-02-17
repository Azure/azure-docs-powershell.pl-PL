---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/start-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
ms.openlocfilehash: c5c5fd14f61be2526c62335b9f6ed33719846a12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188410"
---
# <span data-ttu-id="e1de5-101">Start-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e1de5-101">Start-AzFunctionApp</span></span>

## <span data-ttu-id="e1de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1de5-102">SYNOPSIS</span></span>
<span data-ttu-id="e1de5-103">Pozwala na rozpoczęcie pracy z aplikacją funkcyjną.</span><span class="sxs-lookup"><span data-stu-id="e1de5-103">Starts a function app.</span></span>

## <span data-ttu-id="e1de5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1de5-104">SYNTAX</span></span>

### <span data-ttu-id="e1de5-105">StartByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e1de5-105">StartByName (Default)</span></span>
```
Start-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1de5-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="e1de5-106">ByObjectInput</span></span>
```
Start-AzFunctionApp -InputObject <ISite> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e1de5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1de5-107">DESCRIPTION</span></span>
<span data-ttu-id="e1de5-108">Pozwala na rozpoczęcie pracy z aplikacją funkcyjną.</span><span class="sxs-lookup"><span data-stu-id="e1de5-108">Starts a function app.</span></span>

## <span data-ttu-id="e1de5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1de5-109">EXAMPLES</span></span>

### <span data-ttu-id="e1de5-110">Przykład 1. Uzyskiwanie aplikacji funkcji według nazwy i uruchamianie jej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-110">Example 1: Get a function app by name and start it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Start-AzFunctionApp
```

<span data-ttu-id="e1de5-111">To polecenie pobiera aplikację funkcji według nazwy i uruchamia ją.</span><span class="sxs-lookup"><span data-stu-id="e1de5-111">This command gets a function app by name and starts it.</span></span>

### <span data-ttu-id="e1de5-112">Przykład 2. Uruchamianie aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e1de5-112">Example 2: Start a function app by name.</span></span>
```powershell
PS C:\> Start-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="e1de5-113">To polecenie uruchamia aplikację funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e1de5-113">This command starts a function app by name.</span></span>

## <span data-ttu-id="e1de5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1de5-114">PARAMETERS</span></span>

### <span data-ttu-id="e1de5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1de5-115">-DefaultProfile</span></span>
<span data-ttu-id="e1de5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1de5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1de5-117">-InputObject</span></span>
<span data-ttu-id="e1de5-118">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e1de5-119">-Name</span></span>
<span data-ttu-id="e1de5-120">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-120">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1de5-121">-PassThru</span></span>
<span data-ttu-id="e1de5-122">Zwraca wartość true, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e1de5-122">Returns true when the command succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1de5-123">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1de5-124">-SubscriptionId</span></span>
<span data-ttu-id="e1de5-125">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1de5-125">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1de5-126">-Confirm</span></span>
<span data-ttu-id="e1de5-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1de5-128">-WhatIf</span></span>
<span data-ttu-id="e1de5-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1de5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1de5-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e1de5-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1de5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1de5-131">CommonParameters</span></span>
<span data-ttu-id="e1de5-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1de5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1de5-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1de5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1de5-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1de5-134">INPUTS</span></span>

### <span data-ttu-id="e1de5-135">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite</span><span class="sxs-lookup"><span data-stu-id="e1de5-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="e1de5-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1de5-136">OUTPUTS</span></span>

### <span data-ttu-id="e1de5-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1de5-137">System.Boolean</span></span>

## <span data-ttu-id="e1de5-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1de5-138">NOTES</span></span>

<span data-ttu-id="e1de5-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e1de5-139">ALIASES</span></span>

<span data-ttu-id="e1de5-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1de5-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1de5-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e1de5-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1de5-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1de5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1de5-143">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="e1de5-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="e1de5-144">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="e1de5-145">`CloningInfoSourceWebAppId <String>`: ARM identyfikator zasobu aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="e1de5-146">Identyfikator zasobu aplikacji to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span><span class="sxs-lookup"><span data-stu-id="e1de5-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="e1de5-147">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="e1de5-148">`[Tag <IResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1de5-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e1de5-149">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="e1de5-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e1de5-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> aby włączyć ffinity klienta; aby zatrzymać wysyłanie plików cookie chętnych do sesji, które wysyłają żądania klienta w tej samej sesji <code>false</code> do tego samego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="e1de5-151">Wartość domyślna <code>true</code> to.</span><span class="sxs-lookup"><span data-stu-id="e1de5-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="e1de5-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> aby włączyć uwierzytelnianie klienta (TLS mutual authentication), w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e1de5-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="e1de5-153">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="e1de5-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="e1de5-154">`[ClientCertExclusionPath <String>]`: ścieżki wykluczeń oddzielone przecinkami uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="e1de5-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="e1de5-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: ustawienie aplikacji zastępuje sklonowane aplikacje.</span><span class="sxs-lookup"><span data-stu-id="e1de5-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="e1de5-156">Jeśli jest to określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="e1de5-157">W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej zostaną zachowane.</span><span class="sxs-lookup"><span data-stu-id="e1de5-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="e1de5-158">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="e1de5-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e1de5-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> aby sklonować niestandardowe nazwy hostów z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e1de5-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> aby sklonować kontrolkę źródłową z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e1de5-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> w celu skonfigurowania równoważenia obciążenia dla aplikacji źródłowej i docelowej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="e1de5-162">`[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania.</span><span class="sxs-lookup"><span data-stu-id="e1de5-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="e1de5-163">Ten identyfikator łączy wiele operacji klonowania w celu użycia tej samej migawki.</span><span class="sxs-lookup"><span data-stu-id="e1de5-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="e1de5-164">`[CloningInfoHostingEnvironment <String>]`: Środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="e1de5-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> aby zastąpić aplikację docelową; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e1de5-166">`[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej, np.: Stany Zjednoczone Zachód lub Europa Północna</span><span class="sxs-lookup"><span data-stu-id="e1de5-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="e1de5-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM identyfikator zasobu profilu Menedżera ruchu, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="e1de5-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="e1de5-168">Identyfikator zasobu Menedżera ruchu to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="e1de5-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="e1de5-169">`[CloningInfoTrafficManagerProfileName <String>]`: nazwa profilu Menedżera ruchu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="e1de5-170">Jest to potrzebne tylko wtedy, gdy nie istnieje jeszcze profil menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="e1de5-171">`[Config <ISiteConfig>]`: konfiguracja aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="e1de5-172">`IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy jest włączony punkt końcowy push.</span><span class="sxs-lookup"><span data-stu-id="e1de5-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="e1de5-173">`[ActionMinProcessExecutionTime <String>]`: minimalny czas wykonywania procesu przed podjęciem działania</span><span class="sxs-lookup"><span data-stu-id="e1de5-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="e1de5-174">`[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonanej czynności.</span><span class="sxs-lookup"><span data-stu-id="e1de5-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="e1de5-175">`[AlwaysOn <Boolean?>]`: <code>true</code> jeśli opcja Zawsze jest włączona, a w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e1de5-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-176">`[ApiDefinitionUrl <String>]`: adres URL definicji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e1de5-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="e1de5-177">`[ApiManagementConfigId <String>]`: APIM-Api identyfikator.</span><span class="sxs-lookup"><span data-stu-id="e1de5-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="e1de5-178">`[AppCommandLine <String>]`: wiersz polecenia aplikacji do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="e1de5-179">`[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="e1de5-180">`[Name <String>]`: nazwa parowania.</span><span class="sxs-lookup"><span data-stu-id="e1de5-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="e1de5-181">`[Value <String>]`: Paruj wartość.</span><span class="sxs-lookup"><span data-stu-id="e1de5-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="e1de5-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> jeśli jest włączona funkcja Autosytowania, a w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e1de5-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-183">`[AutoSwapSlotName <String>]`: nazwa gniazda automatycznego zamiany.</span><span class="sxs-lookup"><span data-stu-id="e1de5-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="e1de5-184">`[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="e1de5-185">`[ConnectionString <String>]`: wartość parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="e1de5-186">`[Name <String>]`: nazwa parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="e1de5-187">`[Type <ConnectionStringType?>]`: typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e1de5-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="e1de5-188">`[CorAllowedOrigin <String[]>]`: pobiera lub ustawia listę pochodzenia, z których powinno być dozwolone dzwonienie między pochodzeniem (na http://example.com:12345) przykład:</span><span class="sxs-lookup"><span data-stu-id="e1de5-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="e1de5-189">Aby zezwolić wszystkim, użyj "\*".</span><span class="sxs-lookup"><span data-stu-id="e1de5-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="e1de5-190">`[CorSupportCredentials <Boolean?>]`: Pobiera lub określa, czy żądania CORS z poświadczeniami są dozwolone.</span><span class="sxs-lookup"><span data-stu-id="e1de5-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="e1de5-191">Aby         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="e1de5-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="e1de5-192">`[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="e1de5-193">`[CustomActionParameter <String>]`: parametry pliku wykonywalnego.</span><span class="sxs-lookup"><span data-stu-id="e1de5-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="e1de5-194">`[DefaultDocument <String[]>]`: dokumenty domyślne.</span><span class="sxs-lookup"><span data-stu-id="e1de5-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="e1de5-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> jeśli funkcja szczegółowego rejestrowania błędów jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-196">`[DocumentRoot <String>]`: katalog główny dokumentu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="e1de5-197">`[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą obliczane na stronie claims użytkowników w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="e1de5-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: lista reguł dotyczących rampy.</span><span class="sxs-lookup"><span data-stu-id="e1de5-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="e1de5-199">`[ActionHostName <String>]`: nazwa hosta miejsca, do którego ruch zostanie przekierowany w razie decyzji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="e1de5-200">Np.</span><span class="sxs-lookup"><span data-stu-id="e1de5-200">E.g.</span></span> <span data-ttu-id="e1de5-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="e1de5-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="e1de5-202">`[ChangeDecisionCallbackUrl <String>]`: Niestandardowy algorytm decyzyjny może być podany w rozszerzeniu witryny TiPCallback, którego adres URL można określić.</span><span class="sxs-lookup"><span data-stu-id="e1de5-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="e1de5-203">Zobacz rozszerzenie witryny TiPCallback dla szkieletów i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="e1de5-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="e1de5-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="e1de5-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="e1de5-205">`[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach, aby ponownie określić wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="e1de5-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="e1de5-206">`[ChangeStep <Double?>]`: W scenariuszu automatycznego rozsuwu jest to krok, z którym należy dodać/usunąć, aż osiągnie <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="e1de5-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="e1de5-207">Metryki witryny są sprawdzane co N minut określonych w pliku .\nCustom decision algorithm can be provided in TiPCallback site extension (Rozszerzenie witryny TiPCallback), w którym można określić <code>ChangeIntervalInMinutes</code> adres <code>ChangeDecisionCallbackUrl</code> URL.</span><span class="sxs-lookup"><span data-stu-id="e1de5-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="e1de5-208">`[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="e1de5-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="e1de5-209">`[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="e1de5-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="e1de5-210">`[Name <String>]`: nazwa reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="e1de5-211">Zalecaną nazwą będzie wskaż miejsce, w którym zostanie wyświetlony ruch w eksperymencie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="e1de5-212">`[ReroutePercentage <Double?>]`: procent ruchu, do którego zostanie przekierowany <code>ActionHostName</code> ruch.</span><span class="sxs-lookup"><span data-stu-id="e1de5-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="e1de5-213">`[FtpsState <FtpsState?>]`: stan usługi FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="e1de5-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="e1de5-214">`[HandlerMapping <IHandlerMapping[]>]`: mapowania programów obsługi.</span><span class="sxs-lookup"><span data-stu-id="e1de5-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="e1de5-215">`[Argument <String>]`: argumenty wiersza polecenia przekazywane do edytora skryptów.</span><span class="sxs-lookup"><span data-stu-id="e1de5-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="e1de5-216">`[Extension <String>]`: Żądania z tym rozszerzeniem będą obsługiwane przy użyciu określonej aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="e1de5-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="e1de5-217">`[ScriptProcessor <String>]`: ścieżka bezwzględna do aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="e1de5-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="e1de5-218">`[HealthCheckPath <String>]`: ścieżka kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="e1de5-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="e1de5-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web w celu zezwalania klientom na łączenie się przez http2.0</span><span class="sxs-lookup"><span data-stu-id="e1de5-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="e1de5-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> jeśli rejestrowanie HTTP jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla głównych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="e1de5-222">`[Action <String>]`: Zezwalaj lub odmów dostępu dla tego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="e1de5-223">`[Description <String>]`: opis reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="e1de5-224">`[IPAddress <String>]`: adres IP, dla których obowiązuje ograniczenie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="e1de5-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="e1de5-225">Może mieć postać wyłącznie adresu ipv4 (wymagana właściwość SubnetMask) lub notacji CIDR, takiej jak ipv4/mask (wiodące dopasowanie bitów).</span><span class="sxs-lookup"><span data-stu-id="e1de5-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="e1de5-226">W przypadku cidru CIDR nie można określić właściwości SubnetMask.</span><span class="sxs-lookup"><span data-stu-id="e1de5-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="e1de5-227">`[Name <String>]`: nazwa reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="e1de5-228">`[Priority <Int32?>]`: Priorytet reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="e1de5-229">`[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których jest obowiązujące ograniczenie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="e1de5-230">`[SubnetTrafficTag <Int32?>]`: (wewnętrzny) Tag ruchu podsieci</span><span class="sxs-lookup"><span data-stu-id="e1de5-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="e1de5-231">`[Tag <IPFilterTag?>]`: określa, do czego będzie używany ten filtr IP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="e1de5-232">Ma to na celu obsługę filtrowania adresów IP w serwerach proxy.</span><span class="sxs-lookup"><span data-stu-id="e1de5-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="e1de5-233">`[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e1de5-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="e1de5-234">`[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci Vnet</span><span class="sxs-lookup"><span data-stu-id="e1de5-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="e1de5-235">`[JavaContainer <String>]`: kontener języka Java.</span><span class="sxs-lookup"><span data-stu-id="e1de5-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="e1de5-236">`[JavaContainerVersion <String>]`: wersja kontenera języka Java.</span><span class="sxs-lookup"><span data-stu-id="e1de5-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="e1de5-237">`[JavaVersion <String>]`: wersja Java.</span><span class="sxs-lookup"><span data-stu-id="e1de5-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="e1de5-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalny dozwolony rozmiar dysku w MB.</span><span class="sxs-lookup"><span data-stu-id="e1de5-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="e1de5-239">`[LimitMaxMemoryInMb <Int64?>]`: Maksymalna dozwolona ilość pamięci w MB.</span><span class="sxs-lookup"><span data-stu-id="e1de5-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="e1de5-240">`[LimitMaxPercentageCpu <Double?>]`: Maksymalna dozwolona wartość procentowa użycia procesora.</span><span class="sxs-lookup"><span data-stu-id="e1de5-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="e1de5-241">`[LinuxFxVersion <String>]`: Linux App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="e1de5-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="e1de5-242">`[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.</span><span class="sxs-lookup"><span data-stu-id="e1de5-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="e1de5-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> aby włączyć lokalną funkcję MySQL; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-244">`[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogu dzienników HTTP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="e1de5-245">`[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="e1de5-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="e1de5-246">`[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="e1de5-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="e1de5-247">`[MachineKeyValidation <String>]`: Sprawdzanie poprawności klucza maszynowego.</span><span class="sxs-lookup"><span data-stu-id="e1de5-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="e1de5-248">`[MachineKeyValidationKey <String>]`: klucz sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="e1de5-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="e1de5-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: tryb zarządzanych potoków.</span><span class="sxs-lookup"><span data-stu-id="e1de5-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="e1de5-250">`[ManagedServiceIdentityId <Int32?>]`: Identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="e1de5-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="e1de5-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję protokołu TLS wymaganą dla żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="e1de5-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="e1de5-252">`[NetFrameworkVersion <String>]`: wersja programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e1de5-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="e1de5-253">`[NodeVersion <String>]`: wersja Node.js.</span><span class="sxs-lookup"><span data-stu-id="e1de5-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="e1de5-254">`[NumberOfWorker <Int32?>]`: Liczba pracowników.</span><span class="sxs-lookup"><span data-stu-id="e1de5-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="e1de5-255">`[PhpVersion <String>]`: Wersja PHP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="e1de5-256">`[PowerShellVersion <String>]`: wersja programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e1de5-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="e1de5-257">`[PreWarmedInstanceCount <Int32?>]`: liczba prewarmed instances.</span><span class="sxs-lookup"><span data-stu-id="e1de5-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="e1de5-258">To ustawienie dotyczy tylko planów zużycia i elastyczności</span><span class="sxs-lookup"><span data-stu-id="e1de5-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="e1de5-259">`[PublishingUsername <String>]`: nazwa użytkownika publikowania.</span><span class="sxs-lookup"><span data-stu-id="e1de5-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="e1de5-260">`[PushKind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="e1de5-261">`[PythonVersion <String>]`: Wersja języka Python.</span><span class="sxs-lookup"><span data-stu-id="e1de5-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="e1de5-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> jeśli debugowanie zdalne jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-263">`[RemoteDebuggingVersion <String>]`: Wersja debugowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="e1de5-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="e1de5-264">`[RequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="e1de5-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="e1de5-265">`[RequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="e1de5-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> jeśli śledzenie żądania jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-267">`[RequestTracingExpirationTime <DateTime?>]`: Zażądaj czasu wygaśnięcia śledzenia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="e1de5-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm.</span><span class="sxs-lookup"><span data-stu-id="e1de5-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="e1de5-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm do używania głównych.</span><span class="sxs-lookup"><span data-stu-id="e1de5-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="e1de5-270">`[ScmType <ScmType?>]`: typ SCM.</span><span class="sxs-lookup"><span data-stu-id="e1de5-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="e1de5-271">`[SlowRequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="e1de5-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="e1de5-272">`[SlowRequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="e1de5-273">`[SlowRequestTimeTaken <String>]`: Czas trwania.</span><span class="sxs-lookup"><span data-stu-id="e1de5-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="e1de5-274">`[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są na liście na białej liście do użycia w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="e1de5-275">`[TagsRequiringAuth <String>]`: pobiera lub ustawia ciąg JSON zawierający listę tagów wymagających uwierzytelniania użytkownika w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="e1de5-276">Tagi mogą składać się ze znaków alfanumerycznych i następujących znaków: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="e1de5-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="e1de5-277">Sprawdzanie poprawności należy przeprowadzić na stronie PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="e1de5-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="e1de5-278">`[TracingOption <String>]`: Opcje śledzenia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="e1de5-279">`[TriggerPrivateBytesInKb <Int32?>]`: reguła oparta na bajtach prywatnych.</span><span class="sxs-lookup"><span data-stu-id="e1de5-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="e1de5-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: reguła oparta na kodach stanów.</span><span class="sxs-lookup"><span data-stu-id="e1de5-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="e1de5-281">`[Count <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="e1de5-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="e1de5-282">`[Status <Int32?>]`: kod stanu HTTP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="e1de5-283">`[SubStatus <Int32?>]`: Zażądaj stanu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="e1de5-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="e1de5-284">`[TimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="e1de5-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="e1de5-285">`[Win32Status <Int32?>]`: Kod błędu win32.</span><span class="sxs-lookup"><span data-stu-id="e1de5-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="e1de5-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> aby użyć procesu 32-bitowego pracownika; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-287">`[VirtualApplication <IVirtualApplication[]>]`: aplikacje wirtualne.</span><span class="sxs-lookup"><span data-stu-id="e1de5-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="e1de5-288">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="e1de5-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="e1de5-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> jeśli wstępne ładowanie jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="e1de5-290">`[VirtualDirectory <IVirtualDirectory[]>]`: katalogi wirtualne dla aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="e1de5-291">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="e1de5-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="e1de5-292">`[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="e1de5-293">`[VirtualPath <String>]`: Ścieżka wirtualna.</span><span class="sxs-lookup"><span data-stu-id="e1de5-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="e1de5-294">`[VnetName <String>]`: nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="e1de5-295">`[WebSocketsEnabled <Boolean?>]`: jeśli jest włączona funkcja <code>true</code> WebSocket; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e1de5-296">`[WindowsFxVersion <String>]`: Xenon App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="e1de5-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="e1de5-297">`[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="e1de5-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="e1de5-298">`[ContainerSize <Int32?>]`: rozmiar kontenera funkcji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="e1de5-299">`[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony dzienny przydział czasu pamięci (obowiązuje tylko w przypadku aplikacji dynamicznych).</span><span class="sxs-lookup"><span data-stu-id="e1de5-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="e1de5-300">`[Enabled <Boolean?>]`: <code>true</code> jeśli aplikacja jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="e1de5-301">Ustawienie wartości fałsz powoduje wyłączenie aplikacji (przenosi ją do trybu offline).</span><span class="sxs-lookup"><span data-stu-id="e1de5-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="e1de5-302">`[HostNameSslState <IHostNameSslState[]>]`: Stany SSL o nazwie hosta służą do zarządzania powiązaniami SSL dla nazw hostów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="e1de5-303">`[HostType <HostType?>]`: wskazuje, czy nazwa hosta jest standardową, czy nazwą hosta repozytorium.</span><span class="sxs-lookup"><span data-stu-id="e1de5-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="e1de5-304">`[Name <String>]`: Nazwa hosta.</span><span class="sxs-lookup"><span data-stu-id="e1de5-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="e1de5-305">`[SslState <SslState?>]`: typ SSL.</span><span class="sxs-lookup"><span data-stu-id="e1de5-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="e1de5-306">`[Thumbprint <String>]`: Thumbprint certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="e1de5-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="e1de5-307">`[ToUpdate <Boolean?>]`: ustaw, <code>true</code> aby zaktualizować istniejącą nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="e1de5-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="e1de5-308">`[VirtualIP <String>]`: wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na adresie IP.</span><span class="sxs-lookup"><span data-stu-id="e1de5-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="e1de5-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="e1de5-310">Jeśli, <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e1de5-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="e1de5-311">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1de5-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="e1de5-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web tak, aby akceptowała tylko żądania https.</span><span class="sxs-lookup"><span data-stu-id="e1de5-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="e1de5-313">Przekierowywanie problemów dla żądań http</span><span class="sxs-lookup"><span data-stu-id="e1de5-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="e1de5-314">`[HyperV <Boolean?>]`: Piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e1de5-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="e1de5-315">`[IdentityType <ManagedServiceIdentityType?>]`: typ tożsamości usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e1de5-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="e1de5-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: lista tożsamości przypisanych do użytkownika skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="e1de5-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="e1de5-317">Odwołania do kluczy słownika tożsamości użytkownika będą ARM identyfikatorami zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="e1de5-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="e1de5-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="e1de5-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e1de5-319">`[IsXenon <Boolean?>]`: Przestarzałe: piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e1de5-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="e1de5-320">`[RedundancyMode <RedundancyMode?>]`: tryb nadmiarowości witryn</span><span class="sxs-lookup"><span data-stu-id="e1de5-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="e1de5-321">`[Reserved <Boolean?>]`: <code>true</code> jeśli jest zarezerwowana; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e1de5-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="e1de5-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="e1de5-323">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="e1de5-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="e1de5-324">`[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi aplikacji w formacie: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="e1de5-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="e1de5-325">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1de5-325">RELATED LINKS</span></span>

