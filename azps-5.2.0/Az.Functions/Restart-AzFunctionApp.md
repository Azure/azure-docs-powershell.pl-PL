---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326760"
---
# <span data-ttu-id="90e6b-101">Restart-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="90e6b-101">Restart-AzFunctionApp</span></span>

## <span data-ttu-id="90e6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="90e6b-103">Ponowne uruchamianie aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-103">Restarts a function app.</span></span>

## <span data-ttu-id="90e6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90e6b-104">SYNTAX</span></span>

### <span data-ttu-id="90e6b-105">RestartByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="90e6b-105">RestartByName (Default)</span></span>
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90e6b-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="90e6b-106">ByObjectInput</span></span>
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90e6b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="90e6b-107">DESCRIPTION</span></span>
<span data-ttu-id="90e6b-108">Ponowne uruchamianie aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-108">Restarts a function app.</span></span>

## <span data-ttu-id="90e6b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90e6b-109">EXAMPLES</span></span>

### <span data-ttu-id="90e6b-110">Przykład 1: Uzyskaj aplikację funkcyjną według nazwy i uruchom ją ponownie.</span><span class="sxs-lookup"><span data-stu-id="90e6b-110">Example 1: Get a function app by name and restart it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

<span data-ttu-id="90e6b-111">To polecenie pobiera aplikację funkcyjną według nazwy i uruchamia ją ponownie.</span><span class="sxs-lookup"><span data-stu-id="90e6b-111">This command gets a function app by name and restarts it.</span></span>

### <span data-ttu-id="90e6b-112">Przykład 2: ponowne uruchomienie aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="90e6b-112">Example 2: Restart a function app by name.</span></span>
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="90e6b-113">To polecenie powoduje ponowne uruchomienie aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="90e6b-113">This command restarts a function app by name.</span></span>

## <span data-ttu-id="90e6b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90e6b-114">PARAMETERS</span></span>

### <span data-ttu-id="90e6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e6b-115">-DefaultProfile</span></span>
<span data-ttu-id="90e6b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90e6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e6b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="90e6b-117">-Force</span></span>
<span data-ttu-id="90e6b-118">Wymusza ponowne uruchomienie aplikacji funkcji bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90e6b-118">Forces the cmdlet to restart the function app without prompting for confirmation.</span></span>

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

### <span data-ttu-id="90e6b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90e6b-119">-InputObject</span></span>
<span data-ttu-id="90e6b-120">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="90e6b-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90e6b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90e6b-121">-Name</span></span>
<span data-ttu-id="90e6b-122">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-122">The name of function app.</span></span>

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

### <span data-ttu-id="90e6b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90e6b-123">-PassThru</span></span>
<span data-ttu-id="90e6b-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="90e6b-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="90e6b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e6b-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="90e6b-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="90e6b-126">-SubscriptionId</span></span>
<span data-ttu-id="90e6b-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90e6b-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="90e6b-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90e6b-128">-Confirm</span></span>
<span data-ttu-id="90e6b-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e6b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e6b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e6b-130">-WhatIf</span></span>
<span data-ttu-id="90e6b-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e6b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e6b-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90e6b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e6b-133">CommonParameters</span></span>
<span data-ttu-id="90e6b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e6b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90e6b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e6b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90e6b-136">INPUTS</span></span>

### <span data-ttu-id="90e6b-137">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="90e6b-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="90e6b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90e6b-138">OUTPUTS</span></span>

### <span data-ttu-id="90e6b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90e6b-139">System.Boolean</span></span>

## <span data-ttu-id="90e6b-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90e6b-140">NOTES</span></span>

<span data-ttu-id="90e6b-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="90e6b-141">ALIASES</span></span>

<span data-ttu-id="90e6b-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90e6b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90e6b-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="90e6b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90e6b-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90e6b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90e6b-145">INPUTobject <ISite> :</span><span class="sxs-lookup"><span data-stu-id="90e6b-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="90e6b-146">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="90e6b-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="90e6b-147">`CloningInfoSourceWebAppId <String>`: Identyfikator zasobu ARM aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="90e6b-148">Identyfikator zasobu aplikacji ma postać/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} dla gniazd produkcyjnych i/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} dla innych gniazd.</span><span class="sxs-lookup"><span data-stu-id="90e6b-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="90e6b-149">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="90e6b-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="90e6b-150">`[Tag <IResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="90e6b-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="90e6b-151">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="90e6b-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="90e6b-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> Aby włączyć koligację klienta <code>false</code> , zatrzymywanie wysyłania plików cookie koligacji sesji, które umożliwiają kierowanie żądań klientów w tej samej sesji do tego samego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="90e6b-153">Wartość domyślna to <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="90e6b-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> Aby włączyć uwierzytelnianie certyfikatu klienta (uwierzytelnianie obustronne TLS); w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="90e6b-155">Wartość domyślna to <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="90e6b-156">`[ClientCertExclusionPath <String>]`: uwierzytelnianie certyfikatu klienta ścieżki wykluczeń rozdzielanych przecinkami</span><span class="sxs-lookup"><span data-stu-id="90e6b-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="90e6b-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Ustawienia aplikacji zastępują dla sklonowanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="90e6b-158">Jeśli to ustawienie zostanie określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="90e6b-159">W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej są zachowywane.</span><span class="sxs-lookup"><span data-stu-id="90e6b-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="90e6b-160">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="90e6b-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="90e6b-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> Aby sklonować niestandardowe nazwy hostów z aplikacji źródłowej; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="90e6b-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> Aby sklonować kontrolę źródła z aplikacji źródłowej, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="90e6b-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> Aby skonfigurować równoważenie obciążenia dla aplikacji źródłowej i docelowej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="90e6b-164">`[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania.</span><span class="sxs-lookup"><span data-stu-id="90e6b-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="90e6b-165">Ten identyfikator polega na wielu operacjach klonowania razem, aby użyć tej samej migawki.</span><span class="sxs-lookup"><span data-stu-id="90e6b-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="90e6b-166">`[CloningInfoHostingEnvironment <String>]`: Środowisko App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="90e6b-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="90e6b-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> Aby zastąpić aplikację docelową, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="90e6b-168">`[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej: Zachodnia USA lub Europa Północna</span><span class="sxs-lookup"><span data-stu-id="90e6b-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="90e6b-169">`[CloningInfoTrafficManagerProfileId <String>]`: Identyfikator zasobu ARM profilu usługi Traffic Manager, który ma być używany, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="90e6b-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="90e6b-170">Identyfikator zasobu usługi Traffic Manager ma postać/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="90e6b-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="90e6b-171">`[CloningInfoTrafficManagerProfileName <String>]`: Nazwa profilu usługi Traffic Manager do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="90e6b-172">Jest to potrzebne tylko wtedy, gdy profil w usłudze Traffic Manager już nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="90e6b-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="90e6b-173">`[Config <ISiteConfig>]`: Konfiguracja aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="90e6b-174">`IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy punkt końcowy jest włączony.</span><span class="sxs-lookup"><span data-stu-id="90e6b-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="90e6b-175">`[ActionMinProcessExecutionTime <String>]`: Minimalny czas przetwarzania procesu przed wykonaniem akcji</span><span class="sxs-lookup"><span data-stu-id="90e6b-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="90e6b-176">`[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonania.</span><span class="sxs-lookup"><span data-stu-id="90e6b-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="90e6b-177">`[AlwaysOn <Boolean?>]`: <code>true</code> Jeśli funkcja zawsze włączony jest włączona, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-178">`[ApiDefinitionUrl <String>]`: Adres URL definicji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="90e6b-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="90e6b-179">`[ApiManagementConfigId <String>]`: Identyfikator APIM-Api.</span><span class="sxs-lookup"><span data-stu-id="90e6b-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="90e6b-180">`[AppCommandLine <String>]`: Wiersz polecenia aplikacji, który ma zostać uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="90e6b-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="90e6b-181">`[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="90e6b-182">`[Name <String>]`: Nazwa pary.</span><span class="sxs-lookup"><span data-stu-id="90e6b-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="90e6b-183">`[Value <String>]`: Wartość pary.</span><span class="sxs-lookup"><span data-stu-id="90e6b-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="90e6b-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Jeśli funkcja automatycznego dopasowywania jest włączona, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-185">`[AutoSwapSlotName <String>]`: Automatyczne zamienianie nazwy gniazda.</span><span class="sxs-lookup"><span data-stu-id="90e6b-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="90e6b-186">`[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="90e6b-187">`[ConnectionString <String>]`: Wartość parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="90e6b-188">`[Name <String>]`: Nazwa ciągu połączenia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="90e6b-189">`[Type <ConnectionStringType?>]`: Typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="90e6b-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="90e6b-190">`[CorAllowedOrigin <String[]>]`: Pobiera lub ustawia listę źródeł, którym należy zezwolić na nawiązywanie połączeń między pochodzeniu (na przykład: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="90e6b-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="90e6b-191">Użyj znaku "\*", aby zezwolić wszystkim.</span><span class="sxs-lookup"><span data-stu-id="90e6b-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="90e6b-192">`[CorSupportCredentials <Boolean?>]`: Pobiera lub ustawia, czy żądania CORS z poświadczeniami są dozwolone.</span><span class="sxs-lookup"><span data-stu-id="90e6b-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="90e6b-193"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="90e6b-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="90e6b-194">`[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="90e6b-195">`[CustomActionParameter <String>]`: Parametry pliku wykonywalnego.</span><span class="sxs-lookup"><span data-stu-id="90e6b-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="90e6b-196">`[DefaultDocument <String[]>]`: Dokumenty domyślne.</span><span class="sxs-lookup"><span data-stu-id="90e6b-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="90e6b-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Jeśli jest włączony szczegółowy dziennik błędów; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-198">`[DocumentRoot <String>]`: Katalog główny dokumentu.</span><span class="sxs-lookup"><span data-stu-id="90e6b-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="90e6b-199">`[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą oceniane na podstawie oświadczeń użytkownika w punkcie końcowym rejestracji wypychanej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="90e6b-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista reguł dopełnienia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="90e6b-201">`[ActionHostName <String>]`: Nazwa hosta gniazda, do którego będzie przekierowywany ruch w przypadku podjęcia decyzji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="90e6b-202">Przykład.</span><span class="sxs-lookup"><span data-stu-id="90e6b-202">E.g.</span></span> <span data-ttu-id="90e6b-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="90e6b-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="90e6b-204">`[ChangeDecisionCallbackUrl <String>]`: W rozszerzeniu witryny programu TiPCallback można podać adres URL, który może być określony.</span><span class="sxs-lookup"><span data-stu-id="90e6b-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="90e6b-205">Zobacz rozszerzenie witryny TiPCallback dla szkieletu i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="90e6b-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="90e6b-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="90e6b-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="90e6b-207">`[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach w celu przeszacowania ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="90e6b-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="90e6b-208">`[ChangeStep <Double?>]`: W scenariuszu automatycznego zwiększania poziomu w górę jest to krok do dodania/usunięcia, <code>ReroutePercentage</code> dopóki nie osiągnie on \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="90e6b-209">Metryki witryn są sprawdzane co N minut określonych w <code>ChangeIntervalInMinutes</code> .\nCustom algorytm decyzyjny może być podany w TiPCallback rozszerzeniu witryny, w którym można określić adres URL <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="90e6b-210">`[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której ReroutePercentage pozostanie.</span><span class="sxs-lookup"><span data-stu-id="90e6b-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="90e6b-211">`[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której ReroutePercentage będzie się utrzymywać.</span><span class="sxs-lookup"><span data-stu-id="90e6b-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="90e6b-212">`[Name <String>]`: Nazwa reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="90e6b-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="90e6b-213">Zalecaną nazwą będzie wskazanie gniazda, które otrzyma dane doświadczenie.</span><span class="sxs-lookup"><span data-stu-id="90e6b-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="90e6b-214">`[ReroutePercentage <Double?>]`: Procent ruchu, do którego będzie przekierowywany <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="90e6b-215">`[FtpsState <FtpsState?>]`: Stan usługi FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="90e6b-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="90e6b-216">`[HandlerMapping <IHandlerMapping[]>]`: Mapowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="90e6b-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="90e6b-217">`[Argument <String>]`: Argumenty wiersza polecenia, które mają być przekazywane do procesora skryptów.</span><span class="sxs-lookup"><span data-stu-id="90e6b-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="90e6b-218">`[Extension <String>]`: Żądania dotyczące tego rozszerzenia będą obsługiwane przy użyciu określonej aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="90e6b-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="90e6b-219">`[ScriptProcessor <String>]`: Ścieżka bezwzględna do aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="90e6b-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="90e6b-220">`[HealthCheckPath <String>]`: Ścieżka kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="90e6b-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="90e6b-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web, aby umożliwić klientom nawiązywanie połączenia za pośrednictwem protokołu HTTP 2.0</span><span class="sxs-lookup"><span data-stu-id="90e6b-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="90e6b-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Jeśli rejestrowanie http jest włączone; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Ograniczenia zabezpieczeń IP dla głównego.</span><span class="sxs-lookup"><span data-stu-id="90e6b-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="90e6b-224">`[Action <String>]`: Zezwalanie na dostęp lub odmawianie dostępu do tego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="90e6b-225">`[Description <String>]`: Opis reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="90e6b-226">`[IPAddress <String>]`: Adres IP obowiązuje ograniczenie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="90e6b-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="90e6b-227">Może być w formie czystych adresów IPv4 (wymaganej właściwości maska_podsieci) lub notacji CIDR, takiej jak IPv4/Maska (z wiodącym dopasowaniem bitów).</span><span class="sxs-lookup"><span data-stu-id="90e6b-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="90e6b-228">W przypadku CIDR nie wolno określać właściwości maska_podsieci.</span><span class="sxs-lookup"><span data-stu-id="90e6b-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="90e6b-229">`[Name <String>]`: Nazwa reguły ograniczania adresu IP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="90e6b-230">`[Priority <Int32?>]`: Priorytet reguły ograniczenia IP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="90e6b-231">`[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których obowiązuje ograniczenie.</span><span class="sxs-lookup"><span data-stu-id="90e6b-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="90e6b-232">`[SubnetTrafficTag <Int32?>]`: (wewnętrzny) znacznik ruchu podsieci</span><span class="sxs-lookup"><span data-stu-id="90e6b-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="90e6b-233">`[Tag <IPFilterTag?>]`: Określa, do czego będzie stosowany ten filtr IP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="90e6b-234">Jest to obsługa filtrowania adresów IP na serwerach proxy.</span><span class="sxs-lookup"><span data-stu-id="90e6b-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="90e6b-235">`[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="90e6b-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="90e6b-236">`[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci VNET</span><span class="sxs-lookup"><span data-stu-id="90e6b-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="90e6b-237">`[JavaContainer <String>]`: Kontener Java.</span><span class="sxs-lookup"><span data-stu-id="90e6b-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="90e6b-238">`[JavaContainerVersion <String>]`: Wersja kontenera Java.</span><span class="sxs-lookup"><span data-stu-id="90e6b-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="90e6b-239">`[JavaVersion <String>]`: Wersja Java.</span><span class="sxs-lookup"><span data-stu-id="90e6b-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="90e6b-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalne dozwolone użycie rozmiaru dysku (w MB).</span><span class="sxs-lookup"><span data-stu-id="90e6b-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="90e6b-241">`[LimitMaxMemoryInMb <Int64?>]`: Maksymalne dozwolone użycie pamięci w MB.</span><span class="sxs-lookup"><span data-stu-id="90e6b-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="90e6b-242">`[LimitMaxPercentageCpu <Double?>]`: Maksymalny dozwolony procent użycia procesora CPU.</span><span class="sxs-lookup"><span data-stu-id="90e6b-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="90e6b-243">`[LinuxFxVersion <String>]`: Struktura i wersja aplikacji Linux</span><span class="sxs-lookup"><span data-stu-id="90e6b-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="90e6b-244">`[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.</span><span class="sxs-lookup"><span data-stu-id="90e6b-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="90e6b-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> Aby włączyć lokalną MySQL; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-246">`[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogu dziennika HTTP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="90e6b-247">`[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="90e6b-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="90e6b-248">`[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowujący.</span><span class="sxs-lookup"><span data-stu-id="90e6b-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="90e6b-249">`[MachineKeyValidation <String>]`: MachineKey sprawdzanie poprawności.</span><span class="sxs-lookup"><span data-stu-id="90e6b-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="90e6b-250">`[MachineKeyValidationKey <String>]`: Klucz sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="90e6b-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="90e6b-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Zarządzany tryb potokowy.</span><span class="sxs-lookup"><span data-stu-id="90e6b-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="90e6b-252">`[ManagedServiceIdentityId <Int32?>]`: Zarządzany identyfikator tożsamości usługi</span><span class="sxs-lookup"><span data-stu-id="90e6b-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="90e6b-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję TLS wymaganą dla żądań SSL</span><span class="sxs-lookup"><span data-stu-id="90e6b-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="90e6b-254">`[NetFrameworkVersion <String>]`: Wersja programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="90e6b-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="90e6b-255">`[NodeVersion <String>]`: Wersja programu Node.js.</span><span class="sxs-lookup"><span data-stu-id="90e6b-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="90e6b-256">`[NumberOfWorker <Int32?>]`: Liczba pracowników.</span><span class="sxs-lookup"><span data-stu-id="90e6b-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="90e6b-257">`[PhpVersion <String>]`: Wersja programu PHP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="90e6b-258">`[PowerShellVersion <String>]`: Wersja programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="90e6b-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="90e6b-259">`[PreWarmedInstanceCount <Int32?>]`: Liczba przedgrzanych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="90e6b-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="90e6b-260">To ustawienie dotyczy tylko planów zużycia i elastyczności</span><span class="sxs-lookup"><span data-stu-id="90e6b-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="90e6b-261">`[PublishingUsername <String>]`: Publikowanie nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="90e6b-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="90e6b-262">`[PushKind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="90e6b-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="90e6b-263">`[PythonVersion <String>]`: Wersja języka Python.</span><span class="sxs-lookup"><span data-stu-id="90e6b-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="90e6b-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Jeśli debugowanie zdalne jest włączone, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-265">`[RemoteDebuggingVersion <String>]`: Zdalna wersja debugowania.</span><span class="sxs-lookup"><span data-stu-id="90e6b-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="90e6b-266">`[RequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="90e6b-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="90e6b-267">`[RequestTimeInterval <String>]`: Interwał czasowy.</span><span class="sxs-lookup"><span data-stu-id="90e6b-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="90e6b-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> Jeśli śledzenie żądań jest włączone, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-269">`[RequestTracingExpirationTime <DateTime?>]`: Czas wygaśnięcia śledzenia żądań.</span><span class="sxs-lookup"><span data-stu-id="90e6b-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="90e6b-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Ograniczenia zabezpieczeń IP dla SCM.</span><span class="sxs-lookup"><span data-stu-id="90e6b-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="90e6b-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Ograniczenia zabezpieczeń IP dla SCM umożliwiają korzystanie z głównego.</span><span class="sxs-lookup"><span data-stu-id="90e6b-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="90e6b-272">`[ScmType <ScmType?>]`: Typ SCM.</span><span class="sxs-lookup"><span data-stu-id="90e6b-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="90e6b-273">`[SlowRequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="90e6b-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="90e6b-274">`[SlowRequestTimeInterval <String>]`: Interwał czasowy.</span><span class="sxs-lookup"><span data-stu-id="90e6b-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="90e6b-275">`[SlowRequestTimeTaken <String>]`: Czas trwania.</span><span class="sxs-lookup"><span data-stu-id="90e6b-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="90e6b-276">`[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są whitelisted do użytku w punkcie końcowym rejestracji wypychanej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="90e6b-277">`[TagsRequiringAuth <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które wymagają uwierzytelnienia użytkownika do użycia w punkcie końcowym rejestracji wypychanej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="90e6b-278">Tagi mogą składać się z znaków alfanumerycznych i następujących elementów: _, "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="90e6b-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="90e6b-279">Sprawdzanie poprawności należy przeprowadzić na PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="90e6b-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="90e6b-280">`[TracingOption <String>]`: Opcje śledzenia.</span><span class="sxs-lookup"><span data-stu-id="90e6b-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="90e6b-281">`[TriggerPrivateBytesInKb <Int32?>]`: Reguła oparta na bajtach prywatnych.</span><span class="sxs-lookup"><span data-stu-id="90e6b-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="90e6b-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Reguła oparta na kodach statusu.</span><span class="sxs-lookup"><span data-stu-id="90e6b-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="90e6b-283">`[Count <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="90e6b-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="90e6b-284">`[Status <Int32?>]`: Kod stanu HTTP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="90e6b-285">`[SubStatus <Int32?>]`: Żądanie podrzędne o statusie.</span><span class="sxs-lookup"><span data-stu-id="90e6b-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="90e6b-286">`[TimeInterval <String>]`: Interwał czasowy.</span><span class="sxs-lookup"><span data-stu-id="90e6b-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="90e6b-287">`[Win32Status <Int32?>]`: Kod błędu Win32.</span><span class="sxs-lookup"><span data-stu-id="90e6b-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="90e6b-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> Aby używać usługi 32-bitowego procesu roboczego, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-289">`[VirtualApplication <IVirtualApplication[]>]`: Aplikacje wirtualne.</span><span class="sxs-lookup"><span data-stu-id="90e6b-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="90e6b-290">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="90e6b-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="90e6b-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> Jeśli wstępne ładowanie jest włączone; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="90e6b-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Katalogi wirtualne aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="90e6b-293">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="90e6b-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="90e6b-294">`[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="90e6b-295">`[VirtualPath <String>]`: Ścieżka wirtualna.</span><span class="sxs-lookup"><span data-stu-id="90e6b-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="90e6b-296">`[VnetName <String>]`: Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90e6b-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="90e6b-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> Jeśli protokół WebSocket jest włączony; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="90e6b-298">`[WindowsFxVersion <String>]`: Struktura i wersja aplikacji Xenon</span><span class="sxs-lookup"><span data-stu-id="90e6b-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="90e6b-299">`[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="90e6b-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="90e6b-300">`[ContainerSize <Int32?>]`: Rozmiar kontenera funkcji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="90e6b-301">`[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony przydział czasu na pamięć (dotyczy tylko aplikacji dynamicznych).</span><span class="sxs-lookup"><span data-stu-id="90e6b-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="90e6b-302">`[Enabled <Boolean?>]`: <code>true</code> Jeśli aplikacja jest włączona, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="90e6b-303">Ustawienie tej wartości na wartość FAŁSZ wyłącza aplikację (Pobiera aplikację w trybie offline).</span><span class="sxs-lookup"><span data-stu-id="90e6b-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="90e6b-304">`[HostNameSslState <IHostNameSslState[]>]`: Stany SSL hosta służą do zarządzania powiązaniami protokołu SSL dla hostów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90e6b-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="90e6b-305">`[HostType <HostType?>]`: Wskazuje, czy nazwa hosta jest nazwą hosta standardowego, czy repozytorium.</span><span class="sxs-lookup"><span data-stu-id="90e6b-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="90e6b-306">`[Name <String>]`Nazwą.</span><span class="sxs-lookup"><span data-stu-id="90e6b-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="90e6b-307">`[SslState <SslState?>]`: Typ protokołu SSL.</span><span class="sxs-lookup"><span data-stu-id="90e6b-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="90e6b-308">`[Thumbprint <String>]`: Odcisk palca certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="90e6b-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="90e6b-309">`[ToUpdate <Boolean?>]`: Ustawienie w celu <code>true</code> zaktualizowania istniejącej nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="90e6b-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="90e6b-310">`[VirtualIP <String>]`: Wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na protokole IP.</span><span class="sxs-lookup"><span data-stu-id="90e6b-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="90e6b-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> Aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="90e6b-312">Jeśli <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="90e6b-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="90e6b-313">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu środowiska App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="90e6b-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="90e6b-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web w celu akceptowania tylko żądań HTTPS.</span><span class="sxs-lookup"><span data-stu-id="90e6b-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="90e6b-315">Problemy z przekierowaniem dla żądań http</span><span class="sxs-lookup"><span data-stu-id="90e6b-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="90e6b-316">`[HyperV <Boolean?>]`: Piaskownica funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="90e6b-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="90e6b-317">`[IdentityType <ManagedServiceIdentityType?>]`: Typ zarządzanej tożsamości usługi.</span><span class="sxs-lookup"><span data-stu-id="90e6b-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="90e6b-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Lista tożsamości przypisanych użytkownikowi skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="90e6b-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="90e6b-319">Odwołania do kluczy słownika tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="90e6b-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="90e6b-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="90e6b-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="90e6b-321">`[IsXenon <Boolean?>]`: Przestarzałe: Piaskownica funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="90e6b-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="90e6b-322">`[RedundancyMode <RedundancyMode?>]`: Tryb nadmiarowości witryny</span><span class="sxs-lookup"><span data-stu-id="90e6b-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="90e6b-323">`[Reserved <Boolean?>]`: <code>true</code> Jeśli jest zarezerwowany; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="90e6b-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> Aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="90e6b-325">Wartość domyślna to <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="90e6b-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="90e6b-326">`[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi App Service, sformatowana jako: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="90e6b-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="90e6b-327">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90e6b-327">RELATED LINKS</span></span>

