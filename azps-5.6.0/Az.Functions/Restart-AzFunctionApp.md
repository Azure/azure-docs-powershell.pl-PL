---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: ea5504decd1ac86cda7cf4e0c63744a8d71ce838
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998320"
---
# <span data-ttu-id="ca88d-101">Restart-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="ca88d-101">Restart-AzFunctionApp</span></span>

## <span data-ttu-id="ca88d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca88d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca88d-103">Powoduje ponowne uruchomienie aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-103">Restarts a function app.</span></span>

## <span data-ttu-id="ca88d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca88d-104">SYNTAX</span></span>

### <span data-ttu-id="ca88d-105">RestartByName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ca88d-105">RestartByName (Default)</span></span>
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca88d-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="ca88d-106">ByObjectInput</span></span>
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca88d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca88d-107">DESCRIPTION</span></span>
<span data-ttu-id="ca88d-108">Powoduje ponowne uruchomienie aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-108">Restarts a function app.</span></span>

## <span data-ttu-id="ca88d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca88d-109">EXAMPLES</span></span>

### <span data-ttu-id="ca88d-110">Przykład 1. Uzyskiwanie aplikacji funkcji według nazwy i ponowne uruchamianie jej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-110">Example 1: Get a function app by name and restart it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

<span data-ttu-id="ca88d-111">To polecenie pobiera aplikację funkcji według nazwy i uruchamia ją ponownie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-111">This command gets a function app by name and restarts it.</span></span>

### <span data-ttu-id="ca88d-112">Przykład 2. Ponowne uruchamianie aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ca88d-112">Example 2: Restart a function app by name.</span></span>
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="ca88d-113">To polecenie powoduje ponowne uruchomienie aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ca88d-113">This command restarts a function app by name.</span></span>

## <span data-ttu-id="ca88d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca88d-114">PARAMETERS</span></span>

### <span data-ttu-id="ca88d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca88d-115">-DefaultProfile</span></span>
<span data-ttu-id="ca88d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca88d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca88d-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ca88d-117">-Force</span></span>
<span data-ttu-id="ca88d-118">Wymusza ponowne uruchomienie aplikacji funkcji przez polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-118">Forces the cmdlet to restart the function app without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ca88d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca88d-119">-InputObject</span></span>
<span data-ttu-id="ca88d-120">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca88d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ca88d-121">-Name</span></span>
<span data-ttu-id="ca88d-122">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-122">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca88d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca88d-123">-PassThru</span></span>
<span data-ttu-id="ca88d-124">Zwraca wartość true, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ca88d-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="ca88d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca88d-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca88d-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca88d-126">-SubscriptionId</span></span>
<span data-ttu-id="ca88d-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca88d-127">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca88d-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca88d-128">-Confirm</span></span>
<span data-ttu-id="ca88d-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca88d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca88d-130">-WhatIf</span></span>
<span data-ttu-id="ca88d-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca88d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca88d-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ca88d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca88d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca88d-133">CommonParameters</span></span>
<span data-ttu-id="ca88d-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca88d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca88d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca88d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca88d-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca88d-136">INPUTS</span></span>

### <span data-ttu-id="ca88d-137">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite</span><span class="sxs-lookup"><span data-stu-id="ca88d-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="ca88d-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca88d-138">OUTPUTS</span></span>

### <span data-ttu-id="ca88d-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca88d-139">System.Boolean</span></span>

## <span data-ttu-id="ca88d-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca88d-140">NOTES</span></span>

<span data-ttu-id="ca88d-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ca88d-141">ALIASES</span></span>

<span data-ttu-id="ca88d-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca88d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca88d-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ca88d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca88d-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca88d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca88d-145">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="ca88d-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="ca88d-146">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="ca88d-147">`CloningInfoSourceWebAppId <String>`: ARM identyfikator zasobu aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="ca88d-148">Identyfikator zasobu aplikacji to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span><span class="sxs-lookup"><span data-stu-id="ca88d-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="ca88d-149">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="ca88d-150">`[Tag <IResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca88d-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ca88d-151">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ca88d-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ca88d-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> aby włączyć ffinity klienta; aby zatrzymać wysyłanie plików cookie chętnych do sesji, które wysyłają żądania klienta w tej samej sesji <code>false</code> do tego samego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="ca88d-153">Wartość domyślna <code>true</code> to.</span><span class="sxs-lookup"><span data-stu-id="ca88d-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="ca88d-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> aby włączyć uwierzytelnianie klienta (TLS, mutual authentication), w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="ca88d-155">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="ca88d-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="ca88d-156">`[ClientCertExclusionPath <String>]`: ścieżki wykluczeń oddzielone przecinkami uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="ca88d-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="ca88d-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: ustawienie aplikacji zastępuje sklonowane aplikacje.</span><span class="sxs-lookup"><span data-stu-id="ca88d-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="ca88d-158">Jeśli jest to określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="ca88d-159">W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej zostaną zachowane.</span><span class="sxs-lookup"><span data-stu-id="ca88d-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="ca88d-160">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ca88d-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ca88d-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> aby sklonować niestandardowe nazwy hosta z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ca88d-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> aby sklonować kontrolkę źródłową z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ca88d-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> aby skonfigurować równoważenie obciążenia dla aplikacji źródłowej i docelowej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="ca88d-164">`[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania.</span><span class="sxs-lookup"><span data-stu-id="ca88d-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="ca88d-165">Ten identyfikator łączy wiele operacji klonowania w celu użycia tej samej migawki.</span><span class="sxs-lookup"><span data-stu-id="ca88d-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="ca88d-166">`[CloningInfoHostingEnvironment <String>]`: Środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="ca88d-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> aby zastąpić aplikację docelową; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ca88d-168">`[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej, np.: Stany Zjednoczone Zachód lub Europa Północna</span><span class="sxs-lookup"><span data-stu-id="ca88d-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="ca88d-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM identyfikator zasobu profilu Menedżera ruchu, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="ca88d-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="ca88d-170">Identyfikator zasobu Menedżera ruchu to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="ca88d-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="ca88d-171">`[CloningInfoTrafficManagerProfileName <String>]`: nazwa profilu Menedżera ruchu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="ca88d-172">Jest to potrzebne tylko wtedy, gdy nie istnieje jeszcze profil menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="ca88d-173">`[Config <ISiteConfig>]`: konfiguracja aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="ca88d-174">`IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy punkt końcowy push jest włączony.</span><span class="sxs-lookup"><span data-stu-id="ca88d-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="ca88d-175">`[ActionMinProcessExecutionTime <String>]`: minimalny czas wykonywania procesu przed podjęciem działania</span><span class="sxs-lookup"><span data-stu-id="ca88d-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="ca88d-176">`[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonanego działania.</span><span class="sxs-lookup"><span data-stu-id="ca88d-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="ca88d-177">`[AlwaysOn <Boolean?>]`: <code>true</code> jeśli opcja Zawsze jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-178">`[ApiDefinitionUrl <String>]`: adres URL definicji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ca88d-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="ca88d-179">`[ApiManagementConfigId <String>]`: APIM-Api identyfikator.</span><span class="sxs-lookup"><span data-stu-id="ca88d-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="ca88d-180">`[AppCommandLine <String>]`: wiersz polecenia aplikacji do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="ca88d-181">`[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="ca88d-182">`[Name <String>]`: nazwa parowania.</span><span class="sxs-lookup"><span data-stu-id="ca88d-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="ca88d-183">`[Value <String>]`: Paruj wartość.</span><span class="sxs-lookup"><span data-stu-id="ca88d-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="ca88d-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> jeśli jest włączona funkcja Autosytowania, a w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="ca88d-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-185">`[AutoSwapSlotName <String>]`: nazwa gniazda automatycznego zamiany.</span><span class="sxs-lookup"><span data-stu-id="ca88d-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="ca88d-186">`[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="ca88d-187">`[ConnectionString <String>]`: wartość parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="ca88d-188">`[Name <String>]`: nazwa parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="ca88d-189">`[Type <ConnectionStringType?>]`: typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ca88d-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="ca88d-190">`[CorAllowedOrigin <String[]>]`: pobiera lub ustawia listę pochodzenia, z których powinno być dozwolone dzwonienie między pochodzeniem (na http://example.com:12345) przykład:</span><span class="sxs-lookup"><span data-stu-id="ca88d-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="ca88d-191">Aby zezwolić wszystkim, użyj "\*".</span><span class="sxs-lookup"><span data-stu-id="ca88d-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="ca88d-192">`[CorSupportCredentials <Boolean?>]`: Pobiera lub określa, czy żądania CORS z poświadczeniami są dozwolone.</span><span class="sxs-lookup"><span data-stu-id="ca88d-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="ca88d-193">Aby         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="ca88d-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="ca88d-194">`[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="ca88d-195">`[CustomActionParameter <String>]`: parametry pliku wykonywalnego.</span><span class="sxs-lookup"><span data-stu-id="ca88d-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="ca88d-196">`[DefaultDocument <String[]>]`: dokumenty domyślne.</span><span class="sxs-lookup"><span data-stu-id="ca88d-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="ca88d-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> jeśli funkcja szczegółowego rejestrowania błędów jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-198">`[DocumentRoot <String>]`: katalog główny dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="ca88d-199">`[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą obliczane na stronie claims użytkowników w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="ca88d-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: lista reguł dotyczących rampy.</span><span class="sxs-lookup"><span data-stu-id="ca88d-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="ca88d-201">`[ActionHostName <String>]`: nazwa hosta miejsca, do którego ruch zostanie przekierowany w razie decyzji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="ca88d-202">Np.</span><span class="sxs-lookup"><span data-stu-id="ca88d-202">E.g.</span></span> <span data-ttu-id="ca88d-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ca88d-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="ca88d-204">`[ChangeDecisionCallbackUrl <String>]`: Niestandardowy algorytm decyzyjny może być podany w rozszerzeniu witryny TiPCallback, którego adres URL można określić.</span><span class="sxs-lookup"><span data-stu-id="ca88d-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="ca88d-205">Zobacz rozszerzenie witryny TiPCallback dla szkieletów i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="ca88d-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="ca88d-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="ca88d-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="ca88d-207">`[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach, aby ponownie określić wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="ca88d-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="ca88d-208">`[ChangeStep <Double?>]`: W scenariuszu automatycznego rozsuwu jest to krok, z którym należy dodać/usunąć, aż osiągnie <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="ca88d-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="ca88d-209">Metryki witryny są sprawdzane co N minut określonych w pliku .\nCustom decision algorithm can be provided in TiPCallback site extension (Rozszerzenie <code>ChangeIntervalInMinutes</code> witryny TiPCallback), którego adres URL można określić <code>ChangeDecisionCallbackUrl</code> w .</span><span class="sxs-lookup"><span data-stu-id="ca88d-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="ca88d-210">`[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="ca88d-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="ca88d-211">`[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="ca88d-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="ca88d-212">`[Name <String>]`: nazwa reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="ca88d-213">Zalecaną nazwą będzie wskaż miejsce, w którym zostanie wyświetlony ruch w eksperymencie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="ca88d-214">`[ReroutePercentage <Double?>]`: procent ruchu, do którego zostanie przekierowany <code>ActionHostName</code> ruch.</span><span class="sxs-lookup"><span data-stu-id="ca88d-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="ca88d-215">`[FtpsState <FtpsState?>]`: stan usługi FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="ca88d-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="ca88d-216">`[HandlerMapping <IHandlerMapping[]>]`: mapowania programów obsługi.</span><span class="sxs-lookup"><span data-stu-id="ca88d-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="ca88d-217">`[Argument <String>]`: argumenty wiersza polecenia przekazywane do edytora skryptów.</span><span class="sxs-lookup"><span data-stu-id="ca88d-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="ca88d-218">`[Extension <String>]`: Żądania z tym rozszerzeniem będą obsługiwane przy użyciu określonej aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="ca88d-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="ca88d-219">`[ScriptProcessor <String>]`: ścieżka bezwzględna do aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="ca88d-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="ca88d-220">`[HealthCheckPath <String>]`: ścieżka kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="ca88d-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="ca88d-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web w celu zezwalania klientom na łączenie się przez http2.0</span><span class="sxs-lookup"><span data-stu-id="ca88d-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="ca88d-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> jeśli rejestrowanie HTTP jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla głównych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="ca88d-224">`[Action <String>]`: Zezwalaj lub odmów dostępu dla tego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="ca88d-225">`[Description <String>]`: opis reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="ca88d-226">`[IPAddress <String>]`: adres IP, dla których obowiązuje ograniczenie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ca88d-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="ca88d-227">Może mieć postać wyłącznie adresu ipv4 (wymagana właściwość SubnetMask) lub notacji CIDR, takiej jak ipv4/mask (wiodące dopasowanie bitów).</span><span class="sxs-lookup"><span data-stu-id="ca88d-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="ca88d-228">W przypadku cidru CIDR nie można określić właściwości SubnetMask.</span><span class="sxs-lookup"><span data-stu-id="ca88d-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="ca88d-229">`[Name <String>]`: nazwa reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="ca88d-230">`[Priority <Int32?>]`: Priorytet reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="ca88d-231">`[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których jest obowiązujące ograniczenie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="ca88d-232">`[SubnetTrafficTag <Int32?>]`: (wewnętrzny) Tag ruchu podsieci</span><span class="sxs-lookup"><span data-stu-id="ca88d-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="ca88d-233">`[Tag <IPFilterTag?>]`: określa, do czego będzie używany ten filtr IP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="ca88d-234">Ma to na celu obsługę filtrowania adresów IP w serwerach proxy.</span><span class="sxs-lookup"><span data-stu-id="ca88d-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="ca88d-235">`[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ca88d-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="ca88d-236">`[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci Vnet</span><span class="sxs-lookup"><span data-stu-id="ca88d-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="ca88d-237">`[JavaContainer <String>]`: kontener języka Java.</span><span class="sxs-lookup"><span data-stu-id="ca88d-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="ca88d-238">`[JavaContainerVersion <String>]`: wersja kontenera języka Java.</span><span class="sxs-lookup"><span data-stu-id="ca88d-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="ca88d-239">`[JavaVersion <String>]`: wersja Java.</span><span class="sxs-lookup"><span data-stu-id="ca88d-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="ca88d-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalny dozwolony rozmiar dysku w MB.</span><span class="sxs-lookup"><span data-stu-id="ca88d-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="ca88d-241">`[LimitMaxMemoryInMb <Int64?>]`: Maksymalna dozwolona ilość pamięci w MB.</span><span class="sxs-lookup"><span data-stu-id="ca88d-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="ca88d-242">`[LimitMaxPercentageCpu <Double?>]`: Maksymalna dozwolona wartość procentowa użycia procesora.</span><span class="sxs-lookup"><span data-stu-id="ca88d-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="ca88d-243">`[LinuxFxVersion <String>]`: Linux App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="ca88d-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="ca88d-244">`[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.</span><span class="sxs-lookup"><span data-stu-id="ca88d-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="ca88d-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> w celu włączenia lokalnego mysql; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-246">`[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogów dzienników HTTP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="ca88d-247">`[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="ca88d-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="ca88d-248">`[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="ca88d-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="ca88d-249">`[MachineKeyValidation <String>]`: Sprawdzanie poprawności klucza maszynowego.</span><span class="sxs-lookup"><span data-stu-id="ca88d-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="ca88d-250">`[MachineKeyValidationKey <String>]`: klucz sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="ca88d-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="ca88d-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: tryb zarządzanych potoków.</span><span class="sxs-lookup"><span data-stu-id="ca88d-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="ca88d-252">`[ManagedServiceIdentityId <Int32?>]`: Identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="ca88d-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="ca88d-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję protokołu TLS wymaganą dla żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="ca88d-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="ca88d-254">`[NetFrameworkVersion <String>]`: .NET Framework wersji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="ca88d-255">`[NodeVersion <String>]`: wersja Node.js.</span><span class="sxs-lookup"><span data-stu-id="ca88d-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="ca88d-256">`[NumberOfWorker <Int32?>]`: Liczba pracowników.</span><span class="sxs-lookup"><span data-stu-id="ca88d-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="ca88d-257">`[PhpVersion <String>]`: Wersja PHP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="ca88d-258">`[PowerShellVersion <String>]`: wersja programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca88d-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="ca88d-259">`[PreWarmedInstanceCount <Int32?>]`: liczba prewarmed instances.</span><span class="sxs-lookup"><span data-stu-id="ca88d-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="ca88d-260">To ustawienie dotyczy tylko planów zużycia i elastyczności</span><span class="sxs-lookup"><span data-stu-id="ca88d-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="ca88d-261">`[PublishingUsername <String>]`: nazwa użytkownika publikowania.</span><span class="sxs-lookup"><span data-stu-id="ca88d-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="ca88d-262">`[PushKind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="ca88d-263">`[PythonVersion <String>]`: Wersja języka Python.</span><span class="sxs-lookup"><span data-stu-id="ca88d-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="ca88d-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> jeśli debugowanie zdalne jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-265">`[RemoteDebuggingVersion <String>]`: Wersja debugowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="ca88d-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="ca88d-266">`[RequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="ca88d-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="ca88d-267">`[RequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="ca88d-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> jeśli śledzenie żądania jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-269">`[RequestTracingExpirationTime <DateTime?>]`: Zażądaj czasu wygaśnięcia śledzenia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="ca88d-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm.</span><span class="sxs-lookup"><span data-stu-id="ca88d-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="ca88d-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm do używania głównych.</span><span class="sxs-lookup"><span data-stu-id="ca88d-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="ca88d-272">`[ScmType <ScmType?>]`: typ SCM.</span><span class="sxs-lookup"><span data-stu-id="ca88d-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="ca88d-273">`[SlowRequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="ca88d-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="ca88d-274">`[SlowRequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="ca88d-275">`[SlowRequestTimeTaken <String>]`: Czas trwania.</span><span class="sxs-lookup"><span data-stu-id="ca88d-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="ca88d-276">`[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są na liście na białej liście do użycia w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="ca88d-277">`[TagsRequiringAuth <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które wymagają uwierzytelniania użytkownika w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="ca88d-278">Tagi mogą składać się ze znaków alfanumerycznych i następujących znaków: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="ca88d-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="ca88d-279">Sprawdzanie poprawności należy przeprowadzić na stronie PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="ca88d-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="ca88d-280">`[TracingOption <String>]`: Opcje śledzenia.</span><span class="sxs-lookup"><span data-stu-id="ca88d-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="ca88d-281">`[TriggerPrivateBytesInKb <Int32?>]`: reguła oparta na bajtach prywatnych.</span><span class="sxs-lookup"><span data-stu-id="ca88d-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="ca88d-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: reguła oparta na kodach stanów.</span><span class="sxs-lookup"><span data-stu-id="ca88d-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="ca88d-283">`[Count <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="ca88d-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="ca88d-284">`[Status <Int32?>]`: kod stanu HTTP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="ca88d-285">`[SubStatus <Int32?>]`: Zażądaj stanu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="ca88d-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="ca88d-286">`[TimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="ca88d-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="ca88d-287">`[Win32Status <Int32?>]`: Kod błędu win32.</span><span class="sxs-lookup"><span data-stu-id="ca88d-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="ca88d-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> aby użyć 32-bitowego procesu pracownika; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-289">`[VirtualApplication <IVirtualApplication[]>]`: aplikacje wirtualne.</span><span class="sxs-lookup"><span data-stu-id="ca88d-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="ca88d-290">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="ca88d-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="ca88d-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> jeśli wstępne ładowanie jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="ca88d-292">`[VirtualDirectory <IVirtualDirectory[]>]`: katalogi wirtualne dla aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="ca88d-293">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="ca88d-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="ca88d-294">`[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="ca88d-295">`[VirtualPath <String>]`: Ścieżka wirtualna.</span><span class="sxs-lookup"><span data-stu-id="ca88d-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="ca88d-296">`[VnetName <String>]`: nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="ca88d-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> jeśli funkcja WebSocket jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ca88d-298">`[WindowsFxVersion <String>]`: Xenon App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="ca88d-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="ca88d-299">`[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="ca88d-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="ca88d-300">`[ContainerSize <Int32?>]`: rozmiar kontenera funkcji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="ca88d-301">`[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony dzienny przydział czasu pamięci (obowiązuje tylko w przypadku aplikacji dynamicznych).</span><span class="sxs-lookup"><span data-stu-id="ca88d-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="ca88d-302">`[Enabled <Boolean?>]`: <code>true</code> jeśli aplikacja jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="ca88d-303">Ustawienie wartości fałsz powoduje wyłączenie aplikacji (przenosi ją do trybu offline).</span><span class="sxs-lookup"><span data-stu-id="ca88d-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="ca88d-304">`[HostNameSslState <IHostNameSslState[]>]`: Stany SSL o nazwie hosta służą do zarządzania powiązaniami SSL dla nazw hostów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="ca88d-305">`[HostType <HostType?>]`: wskazuje, czy nazwa hosta jest standardową, czy nazwą hosta repozytorium.</span><span class="sxs-lookup"><span data-stu-id="ca88d-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="ca88d-306">`[Name <String>]`: Nazwa hosta.</span><span class="sxs-lookup"><span data-stu-id="ca88d-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="ca88d-307">`[SslState <SslState?>]`: typ SSL.</span><span class="sxs-lookup"><span data-stu-id="ca88d-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="ca88d-308">`[Thumbprint <String>]`: Thumbprint certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="ca88d-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="ca88d-309">`[ToUpdate <Boolean?>]`: ustaw, <code>true</code> aby zaktualizować istniejącą nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="ca88d-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="ca88d-310">`[VirtualIP <String>]`: wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na adresie IP.</span><span class="sxs-lookup"><span data-stu-id="ca88d-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="ca88d-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="ca88d-312">Jeśli, <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ca88d-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="ca88d-313">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ca88d-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="ca88d-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web tak, aby akceptowała tylko żądania https.</span><span class="sxs-lookup"><span data-stu-id="ca88d-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="ca88d-315">Przekierowywanie problemów dla żądań http</span><span class="sxs-lookup"><span data-stu-id="ca88d-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="ca88d-316">`[HyperV <Boolean?>]`: Piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ca88d-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="ca88d-317">`[IdentityType <ManagedServiceIdentityType?>]`: typ tożsamości usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="ca88d-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="ca88d-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: lista tożsamości przypisanych do użytkownika skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="ca88d-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="ca88d-319">Odwołania do kluczy słownika tożsamości użytkownika będą ARM identyfikatorami zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="ca88d-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="ca88d-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ca88d-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ca88d-321">`[IsXenon <Boolean?>]`: Przestarzałe: piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ca88d-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="ca88d-322">`[RedundancyMode <RedundancyMode?>]`: tryb nadmiarowości witryn</span><span class="sxs-lookup"><span data-stu-id="ca88d-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="ca88d-323">`[Reserved <Boolean?>]`: <code>true</code> jeśli zarezerwowane; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ca88d-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ca88d-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="ca88d-325">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="ca88d-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="ca88d-326">`[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi aplikacji w formacie: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="ca88d-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="ca88d-327">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca88d-327">RELATED LINKS</span></span>

