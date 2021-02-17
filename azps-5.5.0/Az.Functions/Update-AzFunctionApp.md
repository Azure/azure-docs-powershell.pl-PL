---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188402"
---
# <span data-ttu-id="12e44-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="12e44-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="12e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e44-102">SYNOPSIS</span></span>
<span data-ttu-id="12e44-103">Aktualizuje aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-103">Updates a function app.</span></span>

## <span data-ttu-id="12e44-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12e44-104">SYNTAX</span></span>

### <span data-ttu-id="12e44-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="12e44-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12e44-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="12e44-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="12e44-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="12e44-107">DESCRIPTION</span></span>
<span data-ttu-id="12e44-108">Aktualizuje aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-108">Updates a function app.</span></span>

## <span data-ttu-id="12e44-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12e44-109">EXAMPLES</span></span>

### <span data-ttu-id="12e44-110">Przykład 1. Zaktualizuj plan hostingu aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="12e44-111">To polecenie aktualizuje plan hostingu aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="12e44-112">Przykład 2. Ustawianie tożsamości zarządzanej systemuAssigned dla aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="12e44-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="12e44-113">To polecenie ustawia tożsamość zarządzaną przypisaną przez system dla aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="12e44-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="12e44-114">Przykład 3. Aktualizowanie szczegółowych informacji aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="12e44-115">To polecenie aktualizuje szczegółowe informacje dotyczące aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="12e44-116">Przykład 3. Usuwanie tożsamości zarządzanej z aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="12e44-117">To polecenie usuwa tożsamość zarządzaną z aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="12e44-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e44-118">PARAMETERS</span></span>

### <span data-ttu-id="12e44-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="12e44-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="12e44-120">Klucz instrumentacji aplikacji do dodania.</span><span class="sxs-lookup"><span data-stu-id="12e44-120">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e44-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="12e44-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="12e44-122">Nazwa istniejącego projektu szczegółowych informacji o aplikacji, który ma zostać dodany do aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="12e44-122">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e44-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="12e44-123">-AsJob</span></span>
<span data-ttu-id="12e44-124">Uruchamia polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="12e44-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="12e44-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e44-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="12e44-126">- IdentityID</span><span class="sxs-lookup"><span data-stu-id="12e44-126">-IdentityID</span></span>
<span data-ttu-id="12e44-127">Określa listę tożsamości użytkowników skojarzonych z aplikacją funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="12e44-128">Odwołania do tożsamości użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="12e44-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e44-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="12e44-129">-IdentityType</span></span>
<span data-ttu-id="12e44-130">Określa typ tożsamości używany w aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="12e44-131">Wpisanie typu "Brak" spowoduje usunięcie wszystkich tożsamości z aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="12e44-132">Dopuszczalne wartości dla tego parametru to: - SystemAssigned - UserAssigned - None</span><span class="sxs-lookup"><span data-stu-id="12e44-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e44-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12e44-133">-InputObject</span></span>
<span data-ttu-id="12e44-134">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="12e44-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12e44-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="12e44-135">-Name</span></span>
<span data-ttu-id="12e44-136">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-136">The name of the function app.</span></span>

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

### <span data-ttu-id="12e44-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12e44-137">-NoWait</span></span>
<span data-ttu-id="12e44-138">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="12e44-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="12e44-139">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="12e44-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="12e44-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="12e44-140">-PlanName</span></span>
<span data-ttu-id="12e44-141">Nazwa planu usługi.</span><span class="sxs-lookup"><span data-stu-id="12e44-141">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e44-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e44-142">-ResourceGroupName</span></span>
<span data-ttu-id="12e44-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12e44-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="12e44-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e44-144">-SubscriptionId</span></span>
<span data-ttu-id="12e44-145">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12e44-145">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="12e44-146">— Tag</span><span class="sxs-lookup"><span data-stu-id="12e44-146">-Tag</span></span>
<span data-ttu-id="12e44-147">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="12e44-147">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e44-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12e44-148">-Confirm</span></span>
<span data-ttu-id="12e44-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="12e44-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e44-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e44-150">-WhatIf</span></span>
<span data-ttu-id="12e44-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12e44-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e44-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="12e44-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e44-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e44-153">CommonParameters</span></span>
<span data-ttu-id="12e44-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e44-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e44-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12e44-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e44-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12e44-156">INPUTS</span></span>

### <span data-ttu-id="12e44-157">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite</span><span class="sxs-lookup"><span data-stu-id="12e44-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="12e44-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12e44-158">OUTPUTS</span></span>

### <span data-ttu-id="12e44-159">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite</span><span class="sxs-lookup"><span data-stu-id="12e44-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="12e44-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12e44-160">NOTES</span></span>

<span data-ttu-id="12e44-161">ALIASY</span><span class="sxs-lookup"><span data-stu-id="12e44-161">ALIASES</span></span>

<span data-ttu-id="12e44-162">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12e44-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12e44-163">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="12e44-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12e44-164">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12e44-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12e44-165">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="12e44-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="12e44-166">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="12e44-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="12e44-167">`CloningInfoSourceWebAppId <String>`: ARM identyfikator zasobu aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="12e44-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="12e44-168">Identyfikator zasobu aplikacji to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span><span class="sxs-lookup"><span data-stu-id="12e44-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="12e44-169">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="12e44-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="12e44-170">`[Tag <IResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="12e44-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="12e44-171">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="12e44-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="12e44-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> aby włączyć ffinity klienta; aby zatrzymać wysyłanie plików cookie chętnych do sesji, które wysyłają żądania klienta w tej samej sesji <code>false</code> do tego samego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="12e44-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="12e44-173">Wartość domyślna <code>true</code> to.</span><span class="sxs-lookup"><span data-stu-id="12e44-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="12e44-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> aby włączyć uwierzytelnianie klienta (TLS mutual authentication), w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="12e44-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="12e44-175">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="12e44-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="12e44-176">`[ClientCertExclusionPath <String>]`: ścieżki wykluczeń oddzielone przecinkami uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="12e44-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="12e44-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: ustawienie aplikacji zastępuje sklonowane aplikacje.</span><span class="sxs-lookup"><span data-stu-id="12e44-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="12e44-178">Jeśli jest to określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="12e44-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="12e44-179">W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej zostaną zachowane.</span><span class="sxs-lookup"><span data-stu-id="12e44-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="12e44-180">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="12e44-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="12e44-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> aby sklonować niestandardowe nazwy hostów z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="12e44-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> aby sklonować kontrolkę źródłową z aplikacji źródłowej; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="12e44-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> w celu skonfigurowania równoważenia obciążenia dla aplikacji źródłowej i docelowej.</span><span class="sxs-lookup"><span data-stu-id="12e44-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="12e44-184">`[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania.</span><span class="sxs-lookup"><span data-stu-id="12e44-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="12e44-185">Ten identyfikator łączy wiele operacji klonowania w celu użycia tej samej migawki.</span><span class="sxs-lookup"><span data-stu-id="12e44-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="12e44-186">`[CloningInfoHostingEnvironment <String>]`: Środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="12e44-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="12e44-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> aby zastąpić aplikację docelową; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="12e44-188">`[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej, np.: Stany Zjednoczone Zachód lub Europa Północna</span><span class="sxs-lookup"><span data-stu-id="12e44-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="12e44-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM identyfikator zasobu profilu Menedżera ruchu, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="12e44-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="12e44-190">Identyfikator zasobu Menedżera ruchu to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="12e44-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="12e44-191">`[CloningInfoTrafficManagerProfileName <String>]`: nazwa profilu Menedżera ruchu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="12e44-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="12e44-192">Jest to potrzebne tylko wtedy, gdy nie istnieje jeszcze profil menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="12e44-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="12e44-193">`[Config <ISiteConfig>]`: konfiguracja aplikacji.</span><span class="sxs-lookup"><span data-stu-id="12e44-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="12e44-194">`IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy jest włączony punkt końcowy push.</span><span class="sxs-lookup"><span data-stu-id="12e44-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="12e44-195">`[ActionMinProcessExecutionTime <String>]`: minimalny czas wykonywania procesu przed podjęciem działania</span><span class="sxs-lookup"><span data-stu-id="12e44-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="12e44-196">`[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonanej czynności.</span><span class="sxs-lookup"><span data-stu-id="12e44-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="12e44-197">`[AlwaysOn <Boolean?>]`: <code>true</code> jeśli opcja Zawsze jest włączona, a w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="12e44-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-198">`[ApiDefinitionUrl <String>]`: adres URL definicji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="12e44-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="12e44-199">`[ApiManagementConfigId <String>]`: APIM-Api identyfikator.</span><span class="sxs-lookup"><span data-stu-id="12e44-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="12e44-200">`[AppCommandLine <String>]`: wiersz polecenia aplikacji do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="12e44-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="12e44-201">`[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="12e44-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="12e44-202">`[Name <String>]`: nazwa parowania.</span><span class="sxs-lookup"><span data-stu-id="12e44-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="12e44-203">`[Value <String>]`: Paruj wartość.</span><span class="sxs-lookup"><span data-stu-id="12e44-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="12e44-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> jeśli jest włączona funkcja Autosytowania, a w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="12e44-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-205">`[AutoSwapSlotName <String>]`: nazwa gniazda automatycznego zamiany.</span><span class="sxs-lookup"><span data-stu-id="12e44-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="12e44-206">`[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.</span><span class="sxs-lookup"><span data-stu-id="12e44-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="12e44-207">`[ConnectionString <String>]`: wartość parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="12e44-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="12e44-208">`[Name <String>]`: nazwa parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="12e44-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="12e44-209">`[Type <ConnectionStringType?>]`: typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="12e44-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="12e44-210">`[CorAllowedOrigin <String[]>]`: pobiera lub ustawia listę pochodzenia, z których powinno być dozwolone dzwonienie między pochodzeniem (na http://example.com:12345) przykład:</span><span class="sxs-lookup"><span data-stu-id="12e44-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="12e44-211">Aby zezwolić wszystkim, użyj "\*".</span><span class="sxs-lookup"><span data-stu-id="12e44-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="12e44-212">`[CorSupportCredentials <Boolean?>]`: Pobiera lub określa, czy żądania CORS z poświadczeniami są dozwolone.</span><span class="sxs-lookup"><span data-stu-id="12e44-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="12e44-213">Aby         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="12e44-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="12e44-214">`[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="12e44-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="12e44-215">`[CustomActionParameter <String>]`: parametry pliku wykonywalnego.</span><span class="sxs-lookup"><span data-stu-id="12e44-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="12e44-216">`[DefaultDocument <String[]>]`: dokumenty domyślne.</span><span class="sxs-lookup"><span data-stu-id="12e44-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="12e44-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> jeśli funkcja szczegółowego rejestrowania błędów jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-218">`[DocumentRoot <String>]`: katalog główny dokumentu.</span><span class="sxs-lookup"><span data-stu-id="12e44-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="12e44-219">`[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą obliczane na stronie claims użytkowników w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="12e44-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="12e44-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: lista reguł dotyczących rampy.</span><span class="sxs-lookup"><span data-stu-id="12e44-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="12e44-221">`[ActionHostName <String>]`: nazwa hosta miejsca, do którego ruch zostanie przekierowany w razie decyzji.</span><span class="sxs-lookup"><span data-stu-id="12e44-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="12e44-222">Np.</span><span class="sxs-lookup"><span data-stu-id="12e44-222">E.g.</span></span> <span data-ttu-id="12e44-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="12e44-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="12e44-224">`[ChangeDecisionCallbackUrl <String>]`: Niestandardowy algorytm decyzyjny może być podany w rozszerzeniu witryny TiPCallback, którego adres URL można określić.</span><span class="sxs-lookup"><span data-stu-id="12e44-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="12e44-225">Zobacz rozszerzenie witryny TiPCallback dla szkieletów i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="12e44-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="12e44-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="12e44-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="12e44-227">`[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach, aby ponownie określić wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="12e44-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="12e44-228">`[ChangeStep <Double?>]`: W scenariuszu automatycznego rozsuwu jest to krok, z którym należy dodać/usunąć, aż osiągnie <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="12e44-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="12e44-229">Metryki witryny są sprawdzane co N minut określonych w pliku .\nCustom decision algorithm can be provided in TiPCallback site extension (Rozszerzenie witryny TiPCallback), w którym można określić <code>ChangeIntervalInMinutes</code> adres <code>ChangeDecisionCallbackUrl</code> URL.</span><span class="sxs-lookup"><span data-stu-id="12e44-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="12e44-230">`[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="12e44-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="12e44-231">`[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której pozostanie wartość ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="12e44-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="12e44-232">`[Name <String>]`: nazwa reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="12e44-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="12e44-233">Zalecaną nazwą będzie wskaż miejsce, w którym zostanie wyświetlony ruch w eksperymencie.</span><span class="sxs-lookup"><span data-stu-id="12e44-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="12e44-234">`[ReroutePercentage <Double?>]`: procent ruchu, do którego zostanie przekierowany <code>ActionHostName</code> ruch.</span><span class="sxs-lookup"><span data-stu-id="12e44-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="12e44-235">`[FtpsState <FtpsState?>]`: stan usługi FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="12e44-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="12e44-236">`[HandlerMapping <IHandlerMapping[]>]`: mapowania programów obsługi.</span><span class="sxs-lookup"><span data-stu-id="12e44-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="12e44-237">`[Argument <String>]`: argumenty wiersza polecenia przekazywane do edytora skryptów.</span><span class="sxs-lookup"><span data-stu-id="12e44-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="12e44-238">`[Extension <String>]`: Żądania z tym rozszerzeniem będą obsługiwane przy użyciu określonej aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="12e44-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="12e44-239">`[ScriptProcessor <String>]`: ścieżka bezwzględna do aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="12e44-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="12e44-240">`[HealthCheckPath <String>]`: ścieżka kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="12e44-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="12e44-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web w celu zezwalania klientom na łączenie się przez http2.0</span><span class="sxs-lookup"><span data-stu-id="12e44-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="12e44-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> jeśli rejestrowanie HTTP jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla głównych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="12e44-244">`[Action <String>]`: Zezwalaj lub odmów dostępu dla tego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="12e44-245">`[Description <String>]`: opis reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="12e44-246">`[IPAddress <String>]`: adres IP, dla których obowiązuje ograniczenie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="12e44-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="12e44-247">Może mieć postać wyłącznie adresu ipv4 (wymagana właściwość SubnetMask) lub notacji CIDR, takiej jak ipv4/mask (wiodące dopasowanie bitów).</span><span class="sxs-lookup"><span data-stu-id="12e44-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="12e44-248">W przypadku cidru CIDR nie można określić właściwości SubnetMask.</span><span class="sxs-lookup"><span data-stu-id="12e44-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="12e44-249">`[Name <String>]`: nazwa reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="12e44-250">`[Priority <Int32?>]`: Priorytet reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="12e44-251">`[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których jest obowiązujące ograniczenie.</span><span class="sxs-lookup"><span data-stu-id="12e44-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="12e44-252">`[SubnetTrafficTag <Int32?>]`: (wewnętrzny) Tag ruchu podsieci</span><span class="sxs-lookup"><span data-stu-id="12e44-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="12e44-253">`[Tag <IPFilterTag?>]`: określa, do czego będzie używany ten filtr IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="12e44-254">Ma to na celu obsługę filtrowania adresów IP w serwerach proxy.</span><span class="sxs-lookup"><span data-stu-id="12e44-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="12e44-255">`[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="12e44-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="12e44-256">`[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci Vnet</span><span class="sxs-lookup"><span data-stu-id="12e44-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="12e44-257">`[JavaContainer <String>]`: kontener języka Java.</span><span class="sxs-lookup"><span data-stu-id="12e44-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="12e44-258">`[JavaContainerVersion <String>]`: wersja kontenera języka Java.</span><span class="sxs-lookup"><span data-stu-id="12e44-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="12e44-259">`[JavaVersion <String>]`: wersja Java.</span><span class="sxs-lookup"><span data-stu-id="12e44-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="12e44-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalny dozwolony rozmiar dysku w MB.</span><span class="sxs-lookup"><span data-stu-id="12e44-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="12e44-261">`[LimitMaxMemoryInMb <Int64?>]`: Maksymalna dozwolona ilość pamięci w MB.</span><span class="sxs-lookup"><span data-stu-id="12e44-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="12e44-262">`[LimitMaxPercentageCpu <Double?>]`: Maksymalna dozwolona wartość procentowa użycia procesora.</span><span class="sxs-lookup"><span data-stu-id="12e44-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="12e44-263">`[LinuxFxVersion <String>]`: Linux App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="12e44-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="12e44-264">`[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.</span><span class="sxs-lookup"><span data-stu-id="12e44-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="12e44-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> aby włączyć lokalną funkcję MySQL; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-266">`[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogu dzienników HTTP.</span><span class="sxs-lookup"><span data-stu-id="12e44-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="12e44-267">`[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="12e44-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="12e44-268">`[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="12e44-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="12e44-269">`[MachineKeyValidation <String>]`: Sprawdzanie poprawności klucza maszynowego.</span><span class="sxs-lookup"><span data-stu-id="12e44-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="12e44-270">`[MachineKeyValidationKey <String>]`: klucz sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="12e44-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="12e44-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: tryb zarządzanych potoków.</span><span class="sxs-lookup"><span data-stu-id="12e44-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="12e44-272">`[ManagedServiceIdentityId <Int32?>]`: Identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="12e44-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="12e44-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję protokołu TLS wymaganą dla żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="12e44-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="12e44-274">`[NetFrameworkVersion <String>]`: wersja programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="12e44-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="12e44-275">`[NodeVersion <String>]`: wersja Node.js.</span><span class="sxs-lookup"><span data-stu-id="12e44-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="12e44-276">`[NumberOfWorker <Int32?>]`: Liczba pracowników.</span><span class="sxs-lookup"><span data-stu-id="12e44-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="12e44-277">`[PhpVersion <String>]`: Wersja PHP.</span><span class="sxs-lookup"><span data-stu-id="12e44-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="12e44-278">`[PowerShellVersion <String>]`: wersja programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="12e44-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="12e44-279">`[PreWarmedInstanceCount <Int32?>]`: liczba prewarmed instances.</span><span class="sxs-lookup"><span data-stu-id="12e44-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="12e44-280">To ustawienie dotyczy tylko planów zużycia i elastyczności</span><span class="sxs-lookup"><span data-stu-id="12e44-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="12e44-281">`[PublishingUsername <String>]`: nazwa użytkownika publikowania.</span><span class="sxs-lookup"><span data-stu-id="12e44-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="12e44-282">`[PushKind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="12e44-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="12e44-283">`[PythonVersion <String>]`: Wersja języka Python.</span><span class="sxs-lookup"><span data-stu-id="12e44-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="12e44-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> jeśli debugowanie zdalne jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-285">`[RemoteDebuggingVersion <String>]`: Wersja debugowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="12e44-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="12e44-286">`[RequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="12e44-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="12e44-287">`[RequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="12e44-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="12e44-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> jeśli śledzenie żądania jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-289">`[RequestTracingExpirationTime <DateTime?>]`: Zażądaj czasu wygaśnięcia śledzenia.</span><span class="sxs-lookup"><span data-stu-id="12e44-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="12e44-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm.</span><span class="sxs-lookup"><span data-stu-id="12e44-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="12e44-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm do używania głównych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="12e44-292">`[ScmType <ScmType?>]`: typ SCM.</span><span class="sxs-lookup"><span data-stu-id="12e44-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="12e44-293">`[SlowRequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="12e44-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="12e44-294">`[SlowRequestTimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="12e44-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="12e44-295">`[SlowRequestTimeTaken <String>]`: Czas trwania.</span><span class="sxs-lookup"><span data-stu-id="12e44-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="12e44-296">`[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są na liście na białej liście do użycia w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="12e44-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="12e44-297">`[TagsRequiringAuth <String>]`: pobiera lub ustawia ciąg JSON zawierający listę tagów wymagających uwierzytelniania użytkownika w punkcie końcowym wypychania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="12e44-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="12e44-298">Tagi mogą składać się ze znaków alfanumerycznych i następujących znaków: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="12e44-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="12e44-299">Sprawdzanie poprawności należy przeprowadzić na stronie PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="12e44-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="12e44-300">`[TracingOption <String>]`: Opcje śledzenia.</span><span class="sxs-lookup"><span data-stu-id="12e44-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="12e44-301">`[TriggerPrivateBytesInKb <Int32?>]`: reguła oparta na bajtach prywatnych.</span><span class="sxs-lookup"><span data-stu-id="12e44-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="12e44-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: reguła oparta na kodach stanów.</span><span class="sxs-lookup"><span data-stu-id="12e44-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="12e44-303">`[Count <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="12e44-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="12e44-304">`[Status <Int32?>]`: kod stanu HTTP.</span><span class="sxs-lookup"><span data-stu-id="12e44-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="12e44-305">`[SubStatus <Int32?>]`: Zażądaj stanu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="12e44-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="12e44-306">`[TimeInterval <String>]`: interwał czasu.</span><span class="sxs-lookup"><span data-stu-id="12e44-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="12e44-307">`[Win32Status <Int32?>]`: Kod błędu win32.</span><span class="sxs-lookup"><span data-stu-id="12e44-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="12e44-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> aby użyć 32-bitowego procesu pracownika; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-309">`[VirtualApplication <IVirtualApplication[]>]`: aplikacje wirtualne.</span><span class="sxs-lookup"><span data-stu-id="12e44-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="12e44-310">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="12e44-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="12e44-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> jeśli wstępne ładowanie jest włączone; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="12e44-312">`[VirtualDirectory <IVirtualDirectory[]>]`: katalogi wirtualne dla aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="12e44-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="12e44-313">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="12e44-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="12e44-314">`[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="12e44-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="12e44-315">`[VirtualPath <String>]`: Ścieżka wirtualna.</span><span class="sxs-lookup"><span data-stu-id="12e44-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="12e44-316">`[VnetName <String>]`: nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="12e44-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="12e44-317">`[WebSocketsEnabled <Boolean?>]`: jeśli jest włączona funkcja <code>true</code> WebSocket; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="12e44-318">`[WindowsFxVersion <String>]`: Xenon App Framework i wersja</span><span class="sxs-lookup"><span data-stu-id="12e44-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="12e44-319">`[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="12e44-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="12e44-320">`[ContainerSize <Int32?>]`: rozmiar kontenera funkcji.</span><span class="sxs-lookup"><span data-stu-id="12e44-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="12e44-321">`[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony dzienny przydział czasu pamięci (obowiązuje tylko w przypadku aplikacji dynamicznych).</span><span class="sxs-lookup"><span data-stu-id="12e44-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="12e44-322">`[Enabled <Boolean?>]`: <code>true</code> jeśli aplikacja jest włączona; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="12e44-323">Ustawienie wartości fałsz powoduje wyłączenie aplikacji (przenosi ją do trybu offline).</span><span class="sxs-lookup"><span data-stu-id="12e44-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="12e44-324">`[HostNameSslState <IHostNameSslState[]>]`: Stany SSL o nazwie hosta służą do zarządzania powiązaniami SSL dla nazw hostów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="12e44-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="12e44-325">`[HostType <HostType?>]`: wskazuje, czy nazwa hosta jest standardową, czy nazwą hosta repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12e44-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="12e44-326">`[Name <String>]`: Nazwa hosta.</span><span class="sxs-lookup"><span data-stu-id="12e44-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="12e44-327">`[SslState <SslState?>]`: typ SSL.</span><span class="sxs-lookup"><span data-stu-id="12e44-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="12e44-328">`[Thumbprint <String>]`: Thumbprint certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="12e44-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="12e44-329">`[ToUpdate <Boolean?>]`: ustaw, <code>true</code> aby zaktualizować istniejącą nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="12e44-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="12e44-330">`[VirtualIP <String>]`: wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na adresie IP.</span><span class="sxs-lookup"><span data-stu-id="12e44-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="12e44-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="12e44-332">Jeśli, <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="12e44-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="12e44-333">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="12e44-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="12e44-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web tak, aby akceptowała tylko żądania https.</span><span class="sxs-lookup"><span data-stu-id="12e44-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="12e44-335">Przekierowywanie problemów dla żądań http</span><span class="sxs-lookup"><span data-stu-id="12e44-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="12e44-336">`[HyperV <Boolean?>]`: Piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="12e44-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="12e44-337">`[IdentityType <ManagedServiceIdentityType?>]`: typ tożsamości usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="12e44-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="12e44-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: lista tożsamości przypisanych do użytkownika skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="12e44-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="12e44-339">Odwołania do kluczy słownika tożsamości użytkownika będą ARM identyfikatorami zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="12e44-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="12e44-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="12e44-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="12e44-341">`[IsXenon <Boolean?>]`: Przestarzałe: piaskownica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="12e44-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="12e44-342">`[RedundancyMode <RedundancyMode?>]`: tryb nadmiarowości witryn</span><span class="sxs-lookup"><span data-stu-id="12e44-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="12e44-343">`[Reserved <Boolean?>]`: <code>true</code> jeśli jest zarezerwowana; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="12e44-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana; w przeciwnym <code>false</code> razie.</span><span class="sxs-lookup"><span data-stu-id="12e44-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="12e44-345">Wartość domyślna <code>false</code> to.</span><span class="sxs-lookup"><span data-stu-id="12e44-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="12e44-346">`[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi aplikacji w formacie: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="12e44-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="12e44-347">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12e44-347">RELATED LINKS</span></span>

