---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 24a74380fe6930c730357476792cea81ebaf7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990284"
---
# <span data-ttu-id="ff662-101">Update-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="ff662-101">Update-AzFunctionAppSetting</span></span>

## <span data-ttu-id="ff662-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff662-102">SYNOPSIS</span></span>
<span data-ttu-id="ff662-103">Dodaje lub aktualizuje ustawienia aplikacji w aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ff662-103">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="ff662-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff662-104">SYNTAX</span></span>

### <span data-ttu-id="ff662-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="ff662-105">ByName (Default)</span></span>
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff662-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="ff662-106">ByObjectInput</span></span>
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff662-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff662-107">DESCRIPTION</span></span>
<span data-ttu-id="ff662-108">Dodaje lub aktualizuje ustawienia aplikacji w aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ff662-108">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="ff662-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff662-109">EXAMPLES</span></span>

### <span data-ttu-id="ff662-110">Przykład 1. Dodawanie nowego ustawienia aplikacji w aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ff662-110">Example 1: Add a new app setting in a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

<span data-ttu-id="ff662-111">To polecenie powoduje dodanie nowego ustawienia aplikacji w aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="ff662-111">This command adds a new app setting in a function app.</span></span>

## <span data-ttu-id="ff662-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff662-112">PARAMETERS</span></span>

### <span data-ttu-id="ff662-113">— AppSetting</span><span class="sxs-lookup"><span data-stu-id="ff662-113">-AppSetting</span></span>
<span data-ttu-id="ff662-114">Tabela skrótów z klawiszami i wartościami opisuje ustawienia aplikacji, które mają zostać dodane lub zaktualizowane w aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ff662-114">Hashtable with keys and values describe the app settings to be added or updated in the function app.</span></span>
<span data-ttu-id="ff662-115">Na przykład: @{"myappsetting"="123"}</span><span class="sxs-lookup"><span data-stu-id="ff662-115">For example: @{"myappsetting"="123"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff662-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff662-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="ff662-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ff662-117">-Force</span></span>
<span data-ttu-id="ff662-118">Wymusza zaktualizowanie ustawienia aplikacji funkcji przez polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ff662-118">Forces the cmdlet to update function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ff662-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff662-119">-InputObject</span></span>
<span data-ttu-id="ff662-120">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="ff662-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff662-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff662-121">-Name</span></span>
<span data-ttu-id="ff662-122">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="ff662-122">Name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff662-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff662-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff662-124">Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="ff662-124">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff662-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff662-125">-SubscriptionId</span></span>
<span data-ttu-id="ff662-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff662-126">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff662-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff662-127">-Confirm</span></span>
<span data-ttu-id="ff662-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ff662-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff662-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff662-129">-WhatIf</span></span>
<span data-ttu-id="ff662-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff662-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff662-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ff662-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff662-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff662-132">CommonParameters</span></span>
<span data-ttu-id="ff662-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff662-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff662-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff662-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff662-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff662-135">INPUTS</span></span>

### <span data-ttu-id="ff662-136">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite</span><span class="sxs-lookup"><span data-stu-id="ff662-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="ff662-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff662-137">OUTPUTS</span></span>

### <span data-ttu-id="ff662-138">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="ff662-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="ff662-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff662-139">NOTES</span></span>

<span data-ttu-id="ff662-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ff662-140">ALIASES</span></span>

<span data-ttu-id="ff662-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff662-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff662-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ff662-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff662-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff662-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff662-144">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="ff662-144">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="ff662-145">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff662-145">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="ff662-146">`CloningInfoSourceWebAppId <String>`: ARM identyfikator zasobu aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="ff662-146">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="ff662-147">Identyfikator zasobu aplikacji to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span><span class="sxs-lookup"><span data-stu-id="ff662-147">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="ff662-148">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff662-148">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="ff662-149">`[Tag <IResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff662-149">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ff662-150">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ff662-150">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ff662-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> aby włączyć ffinity klienta; aby zatrzymać wysyłanie plików cookie chętnych do sesji, które wysyłają żądania klienta w tej samej sesji <code>false</code> do tego samego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ff662-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="ff662-152">Wartość domyślna <code>true</code> to.</span><span class="sxs-lookup"><span data-stu-id="ff662-152">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="ff662-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> aby włączyć uwierzytelnianie klienta (TLS, mutual authentication), w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="ff662-154">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="ff662-154">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="ff662-155">`[ClientCertExclusionPath <String>]`: ścieżki wykluczeń oddzielone przecinkami uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="ff662-155">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="ff662-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: ustawienie aplikacji zastępuje sklonowane aplikacje.</span><span class="sxs-lookup"><span data-stu-id="ff662-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="ff662-157">Jeśli jest to określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="ff662-157">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="ff662-158">W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej zostaną zachowane.</span><span class="sxs-lookup"><span data-stu-id="ff662-158">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="ff662-159">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ff662-159">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ff662-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> aby sklonować niestandardowe nazwy hosta z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ff662-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> aby sklonować kontrolkę źródłową z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ff662-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> aby skonfigurować równoważenie obciążenia dla aplikacji źródłowej i docelowej.</span><span class="sxs-lookup"><span data-stu-id="ff662-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="ff662-163">`[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania.</span><span class="sxs-lookup"><span data-stu-id="ff662-163">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="ff662-164">Ten identyfikator łączy wiele operacji klonowania w celu użycia tej samej migawki.</span><span class="sxs-lookup"><span data-stu-id="ff662-164">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="ff662-165">`[CloningInfoHostingEnvironment <String>]`: Środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff662-165">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="ff662-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> aby zastąpić aplikację docelową; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ff662-167">`[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej, np.: Stany Zjednoczone Zachód lub Europa Północna</span><span class="sxs-lookup"><span data-stu-id="ff662-167">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="ff662-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM identyfikator zasobu profilu Menedżera ruchu, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="ff662-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="ff662-169">Identyfikator zasobu Menedżera ruchu to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="ff662-169">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="ff662-170">`[CloningInfoTrafficManagerProfileName <String>]`: nazwa profilu Menedżera ruchu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ff662-170">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="ff662-171">Jest to potrzebne tylko wtedy, gdy nie istnieje jeszcze profil menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="ff662-171">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="ff662-172">`[Config <ISiteConfig>]`: konfiguracja aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff662-172">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="ff662-173">`IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy punkt końcowy push jest włączony.</span><span class="sxs-lookup"><span data-stu-id="ff662-173">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="ff662-174">`[ActionMinProcessExecutionTime <String>]`: minimalny czas wykonywania procesu przed podjęciem działania</span><span class="sxs-lookup"><span data-stu-id="ff662-174">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="ff662-175">`[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonanego działania.</span><span class="sxs-lookup"><span data-stu-id="ff662-175">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="ff662-176">`[AlwaysOn <Boolean?>]`: <code>true</code> jeśli opcja Zawsze jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-176">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-177">`[ApiDefinitionUrl <String>]`: adres URL definicji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ff662-177">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="ff662-178">`[ApiManagementConfigId <String>]`: APIM-Api identyfikator.</span><span class="sxs-lookup"><span data-stu-id="ff662-178">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="ff662-179">`[AppCommandLine <String>]`: wiersz polecenia aplikacji do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="ff662-179">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="ff662-180">`[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff662-180">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="ff662-181">`[Name <String>]`: nazwa parowania.</span><span class="sxs-lookup"><span data-stu-id="ff662-181">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="ff662-182">`[Value <String>]`: Paruj wartość.</span><span class="sxs-lookup"><span data-stu-id="ff662-182">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="ff662-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> jeśli jest włączona funkcja Autosytowania, a w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="ff662-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-184">`[AutoSwapSlotName <String>]`: nazwa gniazda automatycznego zamiany.</span><span class="sxs-lookup"><span data-stu-id="ff662-184">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="ff662-185">`[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.</span><span class="sxs-lookup"><span data-stu-id="ff662-185">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="ff662-186">`[ConnectionString <String>]`: wartość parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="ff662-186">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="ff662-187">`[Name <String>]`: nazwa parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="ff662-187">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="ff662-188">`[Type <ConnectionStringType?>]`: typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ff662-188">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="ff662-189">`[CorAllowedOrigin <String[]>]`: pobiera lub ustawia listę pochodzenia, z których powinno być dozwolone dzwonienie między pochodzeniem (na http://example.com:12345) przykład:</span><span class="sxs-lookup"><span data-stu-id="ff662-189">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="ff662-190">Aby zezwolić wszystkim, użyj "\*".</span><span class="sxs-lookup"><span data-stu-id="ff662-190">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="ff662-191">`[CorSupportCredentials <Boolean?>]`: Pobiera lub określa, czy żądania CORS z poświadczeniami są dozwolone.</span><span class="sxs-lookup"><span data-stu-id="ff662-191">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="ff662-192">Aby         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="ff662-192">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="ff662-193">`[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="ff662-193">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="ff662-194">`[CustomActionParameter <String>]`: parametry pliku wykonywalnego.</span><span class="sxs-lookup"><span data-stu-id="ff662-194">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="ff662-195">`[DefaultDocument <String[]>]`: dokumenty domyślne.</span><span class="sxs-lookup"><span data-stu-id="ff662-195">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="ff662-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> jeśli funkcja szczegółowego rejestrowania błędów jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-197">`[DocumentRoot <String>]`: katalog główny dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ff662-197">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="ff662-198">`[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą obliczane na stronie claims użytkowników w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ff662-198">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="ff662-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: lista reguł dotyczących rampy.</span><span class="sxs-lookup"><span data-stu-id="ff662-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="ff662-200">`[ActionHostName <String>]`: nazwa hosta miejsca, do którego ruch zostanie przekierowany w razie decyzji.</span><span class="sxs-lookup"><span data-stu-id="ff662-200">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="ff662-201">Np.</span><span class="sxs-lookup"><span data-stu-id="ff662-201">E.g.</span></span> <span data-ttu-id="ff662-202">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ff662-202">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="ff662-203">`[ChangeDecisionCallbackUrl <String>]`: Niestandardowy algorytm decyzyjny może być podany w rozszerzeniu witryny TiPCallback, którego adres URL można określić.</span><span class="sxs-lookup"><span data-stu-id="ff662-203">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="ff662-204">Zobacz rozszerzenie witryny TiPCallback dla szkieletów i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="ff662-204">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="ff662-205"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="ff662-205">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="ff662-206">`[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach, aby ponownie określić wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="ff662-206">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="ff662-207">`[ChangeStep <Double?>]`: W scenariuszu automatycznego rozsuwu jest to krok, z którym należy dodać/usunąć, aż osiągnie <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="ff662-207">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="ff662-208">Metryki witryny są sprawdzane co N minut określonych w pliku .\nCustom decision algorithm can be provided in TiPCallback site extension (Rozszerzenie <code>ChangeIntervalInMinutes</code> witryny TiPCallback), którego adres URL można określić <code>ChangeDecisionCallbackUrl</code> w .</span><span class="sxs-lookup"><span data-stu-id="ff662-208">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="ff662-209">`[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="ff662-209">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="ff662-210">`[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="ff662-210">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="ff662-211">`[Name <String>]`: nazwa reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="ff662-211">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="ff662-212">Zalecaną nazwą będzie wskaż miejsce, w którym zostanie wyświetlony ruch w eksperymencie.</span><span class="sxs-lookup"><span data-stu-id="ff662-212">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="ff662-213">`[ReroutePercentage <Double?>]`: procent ruchu, do którego zostanie przekierowany <code>ActionHostName</code> ruch.</span><span class="sxs-lookup"><span data-stu-id="ff662-213">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="ff662-214">`[FtpsState <FtpsState?>]`: stan usługi FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="ff662-214">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="ff662-215">`[HandlerMapping <IHandlerMapping[]>]`: mapowania programów obsługi.</span><span class="sxs-lookup"><span data-stu-id="ff662-215">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="ff662-216">`[Argument <String>]`: argumenty wiersza polecenia przekazywane do edytora skryptów.</span><span class="sxs-lookup"><span data-stu-id="ff662-216">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="ff662-217">`[Extension <String>]`: Żądania z tym rozszerzeniem będą obsługiwane przy użyciu określonej aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="ff662-217">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="ff662-218">`[ScriptProcessor <String>]`: ścieżka bezwzględna do aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="ff662-218">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="ff662-219">`[HealthCheckPath <String>]`: ścieżka kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="ff662-219">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="ff662-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web w celu zezwalania klientom na łączenie się przez http2.0</span><span class="sxs-lookup"><span data-stu-id="ff662-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="ff662-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> jeśli rejestrowanie HTTP jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla głównych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ff662-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="ff662-223">`[Action <String>]`: Zezwalaj lub odmów dostępu dla tego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ff662-223">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="ff662-224">`[Description <String>]`: opis reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ff662-224">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="ff662-225">`[IPAddress <String>]`: adres IP, dla których obowiązuje ograniczenie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ff662-225">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="ff662-226">Może mieć postać wyłącznie adresu ipv4 (wymagana właściwość SubnetMask) lub notacji CIDR, takiej jak ipv4/mask (wiodące dopasowanie bitów).</span><span class="sxs-lookup"><span data-stu-id="ff662-226">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="ff662-227">W przypadku cidru CIDR nie można określić właściwości SubnetMask.</span><span class="sxs-lookup"><span data-stu-id="ff662-227">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="ff662-228">`[Name <String>]`: nazwa reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ff662-228">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="ff662-229">`[Priority <Int32?>]`: Priorytet reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ff662-229">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="ff662-230">`[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których jest obowiązujące ograniczenie.</span><span class="sxs-lookup"><span data-stu-id="ff662-230">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="ff662-231">`[SubnetTrafficTag <Int32?>]`: (wewnętrzny) Tag ruchu podsieci</span><span class="sxs-lookup"><span data-stu-id="ff662-231">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="ff662-232">`[Tag <IPFilterTag?>]`: określa, do czego będzie używany ten filtr IP.</span><span class="sxs-lookup"><span data-stu-id="ff662-232">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="ff662-233">Ma to na celu obsługę filtrowania adresów IP w serwerach proxy.</span><span class="sxs-lookup"><span data-stu-id="ff662-233">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="ff662-234">`[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ff662-234">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="ff662-235">`[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci Vnet</span><span class="sxs-lookup"><span data-stu-id="ff662-235">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="ff662-236">`[JavaContainer <String>]`: kontener języka Java.</span><span class="sxs-lookup"><span data-stu-id="ff662-236">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="ff662-237">`[JavaContainerVersion <String>]`: wersja kontenera języka Java.</span><span class="sxs-lookup"><span data-stu-id="ff662-237">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="ff662-238">`[JavaVersion <String>]`: wersja Java.</span><span class="sxs-lookup"><span data-stu-id="ff662-238">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="ff662-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalny dozwolony rozmiar dysku w MB.</span><span class="sxs-lookup"><span data-stu-id="ff662-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="ff662-240">`[LimitMaxMemoryInMb <Int64?>]`: Maksymalna dozwolona ilość pamięci w MB.</span><span class="sxs-lookup"><span data-stu-id="ff662-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="ff662-241">`[LimitMaxPercentageCpu <Double?>]`: Maksymalna dozwolona wartość procentowa użycia procesora.</span><span class="sxs-lookup"><span data-stu-id="ff662-241">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="ff662-242">`[LinuxFxVersion <String>]`: Linux App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="ff662-242">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="ff662-243">`[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.</span><span class="sxs-lookup"><span data-stu-id="ff662-243">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="ff662-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> w celu włączenia lokalnego mysql; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-245">`[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogów dzienników HTTP.</span><span class="sxs-lookup"><span data-stu-id="ff662-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="ff662-246">`[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="ff662-246">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="ff662-247">`[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="ff662-247">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="ff662-248">`[MachineKeyValidation <String>]`: Sprawdzanie poprawności klucza maszynowego.</span><span class="sxs-lookup"><span data-stu-id="ff662-248">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="ff662-249">`[MachineKeyValidationKey <String>]`: klucz sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="ff662-249">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="ff662-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: tryb zarządzanych potoków.</span><span class="sxs-lookup"><span data-stu-id="ff662-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="ff662-251">`[ManagedServiceIdentityId <Int32?>]`: Identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="ff662-251">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="ff662-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję protokołu TLS wymaganą dla żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="ff662-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="ff662-253">`[NetFrameworkVersion <String>]`: .NET Framework wersji.</span><span class="sxs-lookup"><span data-stu-id="ff662-253">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="ff662-254">`[NodeVersion <String>]`: wersja Node.js.</span><span class="sxs-lookup"><span data-stu-id="ff662-254">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="ff662-255">`[NumberOfWorker <Int32?>]`: Liczba pracowników.</span><span class="sxs-lookup"><span data-stu-id="ff662-255">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="ff662-256">`[PhpVersion <String>]`: Wersja PHP.</span><span class="sxs-lookup"><span data-stu-id="ff662-256">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="ff662-257">`[PowerShellVersion <String>]`: wersja programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff662-257">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="ff662-258">`[PreWarmedInstanceCount <Int32?>]`: liczba prewarmed instances.</span><span class="sxs-lookup"><span data-stu-id="ff662-258">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="ff662-259">To ustawienie dotyczy tylko planów zużycia i elastyczności</span><span class="sxs-lookup"><span data-stu-id="ff662-259">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="ff662-260">`[PublishingUsername <String>]`: nazwa użytkownika publikowania.</span><span class="sxs-lookup"><span data-stu-id="ff662-260">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="ff662-261">`[PushKind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff662-261">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="ff662-262">`[PythonVersion <String>]`: Wersja języka Python.</span><span class="sxs-lookup"><span data-stu-id="ff662-262">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="ff662-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> jeśli debugowanie zdalne jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-264">`[RemoteDebuggingVersion <String>]`: Wersja debugowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="ff662-264">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="ff662-265">`[RequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="ff662-265">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="ff662-266">`[RequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="ff662-266">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="ff662-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> jeśli śledzenie żądania jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-268">`[RequestTracingExpirationTime <DateTime?>]`: Zażądaj czasu wygaśnięcia śledzenia.</span><span class="sxs-lookup"><span data-stu-id="ff662-268">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="ff662-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm.</span><span class="sxs-lookup"><span data-stu-id="ff662-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="ff662-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm do używania głównych.</span><span class="sxs-lookup"><span data-stu-id="ff662-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="ff662-271">`[ScmType <ScmType?>]`: typ SCM.</span><span class="sxs-lookup"><span data-stu-id="ff662-271">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="ff662-272">`[SlowRequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="ff662-272">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="ff662-273">`[SlowRequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="ff662-273">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="ff662-274">`[SlowRequestTimeTaken <String>]`: Czas trwania.</span><span class="sxs-lookup"><span data-stu-id="ff662-274">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="ff662-275">`[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są na liście na białej liście do użycia w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ff662-275">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="ff662-276">`[TagsRequiringAuth <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które wymagają uwierzytelniania użytkownika w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ff662-276">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="ff662-277">Tagi mogą składać się ze znaków alfanumerycznych i następujących znaków: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="ff662-277">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="ff662-278">Sprawdzanie poprawności należy przeprowadzić na stronie PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="ff662-278">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="ff662-279">`[TracingOption <String>]`: Opcje śledzenia.</span><span class="sxs-lookup"><span data-stu-id="ff662-279">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="ff662-280">`[TriggerPrivateBytesInKb <Int32?>]`: reguła oparta na bajtach prywatnych.</span><span class="sxs-lookup"><span data-stu-id="ff662-280">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="ff662-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: reguła oparta na kodach stanów.</span><span class="sxs-lookup"><span data-stu-id="ff662-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="ff662-282">`[Count <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="ff662-282">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="ff662-283">`[Status <Int32?>]`: kod stanu HTTP.</span><span class="sxs-lookup"><span data-stu-id="ff662-283">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="ff662-284">`[SubStatus <Int32?>]`: Zażądaj stanu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="ff662-284">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="ff662-285">`[TimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="ff662-285">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="ff662-286">`[Win32Status <Int32?>]`: Kod błędu win32.</span><span class="sxs-lookup"><span data-stu-id="ff662-286">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="ff662-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> aby użyć 32-bitowego procesu pracownika; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-288">`[VirtualApplication <IVirtualApplication[]>]`: aplikacje wirtualne.</span><span class="sxs-lookup"><span data-stu-id="ff662-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="ff662-289">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="ff662-289">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="ff662-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> jeśli wstępne ładowanie jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="ff662-291">`[VirtualDirectory <IVirtualDirectory[]>]`: katalogi wirtualne dla aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff662-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="ff662-292">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="ff662-292">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="ff662-293">`[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff662-293">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="ff662-294">`[VirtualPath <String>]`: Ścieżka wirtualna.</span><span class="sxs-lookup"><span data-stu-id="ff662-294">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="ff662-295">`[VnetName <String>]`: nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff662-295">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="ff662-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> jeśli funkcja WebSocket jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="ff662-297">`[WindowsFxVersion <String>]`: Xenon App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="ff662-297">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="ff662-298">`[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="ff662-298">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="ff662-299">`[ContainerSize <Int32?>]`: rozmiar kontenera funkcji.</span><span class="sxs-lookup"><span data-stu-id="ff662-299">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="ff662-300">`[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony dzienny przydział czasu pamięci (obowiązuje tylko w przypadku aplikacji dynamicznych).</span><span class="sxs-lookup"><span data-stu-id="ff662-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="ff662-301">`[Enabled <Boolean?>]`: <code>true</code> jeśli aplikacja jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-301">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="ff662-302">Ustawienie wartości fałsz powoduje wyłączenie aplikacji (przenosi ją do trybu offline).</span><span class="sxs-lookup"><span data-stu-id="ff662-302">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="ff662-303">`[HostNameSslState <IHostNameSslState[]>]`: Stany SSL o nazwie hosta służą do zarządzania powiązaniami SSL dla nazw hostów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff662-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="ff662-304">`[HostType <HostType?>]`: wskazuje, czy nazwa hosta jest standardową, czy nazwą hosta repozytorium.</span><span class="sxs-lookup"><span data-stu-id="ff662-304">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="ff662-305">`[Name <String>]`: Nazwa hosta.</span><span class="sxs-lookup"><span data-stu-id="ff662-305">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="ff662-306">`[SslState <SslState?>]`: typ SSL.</span><span class="sxs-lookup"><span data-stu-id="ff662-306">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="ff662-307">`[Thumbprint <String>]`: Thumbprint certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="ff662-307">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="ff662-308">`[ToUpdate <Boolean?>]`: ustaw, <code>true</code> aby zaktualizować istniejącą nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="ff662-308">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="ff662-309">`[VirtualIP <String>]`: wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na adresie IP.</span><span class="sxs-lookup"><span data-stu-id="ff662-309">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="ff662-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="ff662-311">Jeśli, <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ff662-311">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="ff662-312">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff662-312">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="ff662-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web tak, aby akceptowała tylko żądania https.</span><span class="sxs-lookup"><span data-stu-id="ff662-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="ff662-314">Przekierowywanie problemów dla żądań http</span><span class="sxs-lookup"><span data-stu-id="ff662-314">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="ff662-315">`[HyperV <Boolean?>]`: Piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ff662-315">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="ff662-316">`[IdentityType <ManagedServiceIdentityType?>]`: typ tożsamości usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="ff662-316">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="ff662-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: lista tożsamości przypisanych do użytkownika skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="ff662-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="ff662-318">Odwołania do kluczy słownika tożsamości użytkownika będą ARM identyfikatorami zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="ff662-318">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="ff662-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ff662-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ff662-320">`[IsXenon <Boolean?>]`: Przestarzałe: piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ff662-320">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="ff662-321">`[RedundancyMode <RedundancyMode?>]`: tryb nadmiarowości witryn</span><span class="sxs-lookup"><span data-stu-id="ff662-321">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="ff662-322">`[Reserved <Boolean?>]`: <code>true</code> jeśli zarezerwowane; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-322">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="ff662-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="ff662-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="ff662-324">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="ff662-324">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="ff662-325">`[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi aplikacji w formacie: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="ff662-325">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="ff662-326">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff662-326">RELATED LINKS</span></span>

