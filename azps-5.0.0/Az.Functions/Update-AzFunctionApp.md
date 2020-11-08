---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224373"
---
# <span data-ttu-id="f21b1-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="f21b1-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="f21b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f21b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f21b1-103">Aktualizuje aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-103">Updates a function app.</span></span>

## <span data-ttu-id="f21b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f21b1-104">SYNTAX</span></span>

### <span data-ttu-id="f21b1-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f21b1-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f21b1-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="f21b1-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f21b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f21b1-107">DESCRIPTION</span></span>
<span data-ttu-id="f21b1-108">Aktualizuje aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-108">Updates a function app.</span></span>

## <span data-ttu-id="f21b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f21b1-109">EXAMPLES</span></span>

### <span data-ttu-id="f21b1-110">Przykład 1: funkcja aktualizacji — plan hostingu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="f21b1-111">To polecenie aktualizuje plan hostingu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="f21b1-112">Przykład 2: Ustawianie tożsamości zarządzanej SystemAssigned dla aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="f21b1-113">To polecenie ustawia SystemAssignedą zarządzaną tożsamość dla aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="f21b1-114">Przykład 3: funkcja Aktualizacje aplikacja szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="f21b1-115">To polecenie aktualizuje informacje o funkcjach w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="f21b1-116">Przykład 3: Usuwanie zarządzanej tożsamości z aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="f21b1-117">To polecenie usuwa zarządzaną tożsamość z aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="f21b1-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f21b1-118">PARAMETERS</span></span>

### <span data-ttu-id="f21b1-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="f21b1-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="f21b1-120">Klucz Instrumentacji aplikacji, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="f21b1-120">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="f21b1-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="f21b1-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="f21b1-122">Nazwa istniejącego projektu usługi App Insights, który ma zostać dodany do aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-122">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="f21b1-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f21b1-123">-AsJob</span></span>
<span data-ttu-id="f21b1-124">Uruchamia polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="f21b1-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="f21b1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21b1-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="f21b1-126">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="f21b1-126">-IdentityID</span></span>
<span data-ttu-id="f21b1-127">Określa listę tożsamości użytkowników skojarzonych z aplikacją funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="f21b1-128">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="f21b1-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="f21b1-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f21b1-129">-IdentityType</span></span>
<span data-ttu-id="f21b1-130">Określa typ tożsamości używanej przez aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="f21b1-131">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="f21b1-132">Dopuszczalne wartości tego parametru to:-SystemAssigned-UserAssigned-none.</span><span class="sxs-lookup"><span data-stu-id="f21b1-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

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

### <span data-ttu-id="f21b1-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f21b1-133">-InputObject</span></span>
<span data-ttu-id="f21b1-134">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="f21b1-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f21b1-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f21b1-135">-Name</span></span>
<span data-ttu-id="f21b1-136">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-136">The name of the function app.</span></span>

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

### <span data-ttu-id="f21b1-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f21b1-137">-NoWait</span></span>
<span data-ttu-id="f21b1-138">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="f21b1-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="f21b1-139">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="f21b1-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f21b1-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f21b1-140">-PlanName</span></span>
<span data-ttu-id="f21b1-141">Nazwa planu usługi.</span><span class="sxs-lookup"><span data-stu-id="f21b1-141">The name of the service plan.</span></span>

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

### <span data-ttu-id="f21b1-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f21b1-142">-ResourceGroupName</span></span>
<span data-ttu-id="f21b1-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f21b1-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="f21b1-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f21b1-144">-SubscriptionId</span></span>
<span data-ttu-id="f21b1-145">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f21b1-145">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="f21b1-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="f21b1-146">-Tag</span></span>
<span data-ttu-id="f21b1-147">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f21b1-147">Resource tags.</span></span>

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

### <span data-ttu-id="f21b1-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f21b1-148">-Confirm</span></span>
<span data-ttu-id="f21b1-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f21b1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f21b1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f21b1-150">-WhatIf</span></span>
<span data-ttu-id="f21b1-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f21b1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f21b1-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f21b1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f21b1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21b1-153">CommonParameters</span></span>
<span data-ttu-id="f21b1-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f21b1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21b1-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f21b1-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21b1-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f21b1-156">INPUTS</span></span>

### <span data-ttu-id="f21b1-157">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="f21b1-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="f21b1-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f21b1-158">OUTPUTS</span></span>

### <span data-ttu-id="f21b1-159">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="f21b1-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="f21b1-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f21b1-160">NOTES</span></span>

<span data-ttu-id="f21b1-161">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f21b1-161">ALIASES</span></span>

<span data-ttu-id="f21b1-162">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f21b1-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f21b1-163">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f21b1-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f21b1-164">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f21b1-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f21b1-165">INPUTobject <ISite> :</span><span class="sxs-lookup"><span data-stu-id="f21b1-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="f21b1-166">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f21b1-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="f21b1-167">`CloningInfoSourceWebAppId <String>`: Identyfikator zasobu ARM aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="f21b1-168">Identyfikator zasobu aplikacji ma postać/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} dla gniazd produkcyjnych i/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} dla innych gniazd.</span><span class="sxs-lookup"><span data-stu-id="f21b1-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="f21b1-169">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="f21b1-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="f21b1-170">`[Tag <IResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f21b1-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f21b1-171">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="f21b1-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f21b1-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> Aby włączyć koligację klienta <code>false</code> , zatrzymywanie wysyłania plików cookie koligacji sesji, które umożliwiają kierowanie żądań klientów w tej samej sesji do tego samego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="f21b1-173">Wartość domyślna to <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="f21b1-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> Aby włączyć uwierzytelnianie certyfikatu klienta (uwierzytelnianie obustronne TLS); w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="f21b1-175">Wartość domyślna to <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="f21b1-176">`[ClientCertExclusionPath <String>]`: uwierzytelnianie certyfikatu klienta ścieżki wykluczeń rozdzielanych przecinkami</span><span class="sxs-lookup"><span data-stu-id="f21b1-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="f21b1-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Ustawienia aplikacji zastępują dla sklonowanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="f21b1-178">Jeśli to ustawienie zostanie określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="f21b1-179">W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej są zachowywane.</span><span class="sxs-lookup"><span data-stu-id="f21b1-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="f21b1-180">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="f21b1-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f21b1-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> Aby sklonować niestandardowe nazwy hostów z aplikacji źródłowej; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f21b1-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> Aby sklonować kontrolę źródła z aplikacji źródłowej, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f21b1-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> Aby skonfigurować równoważenie obciążenia dla aplikacji źródłowej i docelowej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="f21b1-184">`[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania.</span><span class="sxs-lookup"><span data-stu-id="f21b1-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="f21b1-185">Ten identyfikator polega na wielu operacjach klonowania razem, aby użyć tej samej migawki.</span><span class="sxs-lookup"><span data-stu-id="f21b1-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="f21b1-186">`[CloningInfoHostingEnvironment <String>]`: Środowisko App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="f21b1-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="f21b1-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> Aby zastąpić aplikację docelową, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f21b1-188">`[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej: Zachodnia USA lub Europa Północna</span><span class="sxs-lookup"><span data-stu-id="f21b1-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="f21b1-189">`[CloningInfoTrafficManagerProfileId <String>]`: Identyfikator zasobu ARM profilu usługi Traffic Manager, który ma być używany, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="f21b1-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="f21b1-190">Identyfikator zasobu usługi Traffic Manager ma postać/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="f21b1-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="f21b1-191">`[CloningInfoTrafficManagerProfileName <String>]`: Nazwa profilu usługi Traffic Manager do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="f21b1-192">Jest to potrzebne tylko wtedy, gdy profil w usłudze Traffic Manager już nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="f21b1-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="f21b1-193">`[Config <ISiteConfig>]`: Konfiguracja aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="f21b1-194">`IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy punkt końcowy jest włączony.</span><span class="sxs-lookup"><span data-stu-id="f21b1-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="f21b1-195">`[ActionMinProcessExecutionTime <String>]`: Minimalny czas przetwarzania procesu przed wykonaniem akcji</span><span class="sxs-lookup"><span data-stu-id="f21b1-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="f21b1-196">`[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonania.</span><span class="sxs-lookup"><span data-stu-id="f21b1-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="f21b1-197">`[AlwaysOn <Boolean?>]`: <code>true</code> Jeśli funkcja zawsze włączony jest włączona, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-198">`[ApiDefinitionUrl <String>]`: Adres URL definicji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f21b1-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="f21b1-199">`[ApiManagementConfigId <String>]`: Identyfikator APIM-Api.</span><span class="sxs-lookup"><span data-stu-id="f21b1-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="f21b1-200">`[AppCommandLine <String>]`: Wiersz polecenia aplikacji, który ma zostać uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="f21b1-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="f21b1-201">`[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="f21b1-202">`[Name <String>]`: Nazwa pary.</span><span class="sxs-lookup"><span data-stu-id="f21b1-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="f21b1-203">`[Value <String>]`: Wartość pary.</span><span class="sxs-lookup"><span data-stu-id="f21b1-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="f21b1-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Jeśli funkcja automatycznego dopasowywania jest włączona, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-205">`[AutoSwapSlotName <String>]`: Automatyczne zamienianie nazwy gniazda.</span><span class="sxs-lookup"><span data-stu-id="f21b1-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="f21b1-206">`[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="f21b1-207">`[ConnectionString <String>]`: Wartość parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="f21b1-208">`[Name <String>]`: Nazwa ciągu połączenia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="f21b1-209">`[Type <ConnectionStringType?>]`: Typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f21b1-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="f21b1-210">`[CorAllowedOrigin <String[]>]`: Pobiera lub ustawia listę źródeł, którym należy zezwolić na nawiązywanie połączeń między pochodzeniu (na przykład: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="f21b1-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="f21b1-211">Użyj znaku "\*", aby zezwolić wszystkim.</span><span class="sxs-lookup"><span data-stu-id="f21b1-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="f21b1-212">`[CorSupportCredentials <Boolean?>]`: Pobiera lub ustawia, czy żądania CORS z poświadczeniami są dozwolone.</span><span class="sxs-lookup"><span data-stu-id="f21b1-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="f21b1-213"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="f21b1-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="f21b1-214">`[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="f21b1-215">`[CustomActionParameter <String>]`: Parametry pliku wykonywalnego.</span><span class="sxs-lookup"><span data-stu-id="f21b1-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="f21b1-216">`[DefaultDocument <String[]>]`: Dokumenty domyślne.</span><span class="sxs-lookup"><span data-stu-id="f21b1-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="f21b1-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Jeśli jest włączony szczegółowy dziennik błędów; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-218">`[DocumentRoot <String>]`: Katalog główny dokumentu.</span><span class="sxs-lookup"><span data-stu-id="f21b1-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="f21b1-219">`[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą oceniane na podstawie oświadczeń użytkownika w punkcie końcowym rejestracji wypychanej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="f21b1-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista reguł dopełnienia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="f21b1-221">`[ActionHostName <String>]`: Nazwa hosta gniazda, do którego będzie przekierowywany ruch w przypadku podjęcia decyzji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="f21b1-222">Przykład.</span><span class="sxs-lookup"><span data-stu-id="f21b1-222">E.g.</span></span> <span data-ttu-id="f21b1-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="f21b1-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="f21b1-224">`[ChangeDecisionCallbackUrl <String>]`: W rozszerzeniu witryny programu TiPCallback można podać adres URL, który może być określony.</span><span class="sxs-lookup"><span data-stu-id="f21b1-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="f21b1-225">Zobacz rozszerzenie witryny TiPCallback dla szkieletu i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="f21b1-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="f21b1-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="f21b1-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="f21b1-227">`[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach w celu przeszacowania ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="f21b1-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="f21b1-228">`[ChangeStep <Double?>]`: W scenariuszu automatycznego zwiększania poziomu w górę jest to krok do dodania/usunięcia, <code>ReroutePercentage</code> dopóki nie osiągnie on \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="f21b1-229">Metryki witryn są sprawdzane co N minut określonych w <code>ChangeIntervalInMinutes</code> .\nCustom algorytm decyzyjny może być podany w TiPCallback rozszerzeniu witryny, w którym można określić adres URL <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="f21b1-230">`[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której ReroutePercentage pozostanie.</span><span class="sxs-lookup"><span data-stu-id="f21b1-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="f21b1-231">`[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której ReroutePercentage będzie się utrzymywać.</span><span class="sxs-lookup"><span data-stu-id="f21b1-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="f21b1-232">`[Name <String>]`: Nazwa reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="f21b1-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="f21b1-233">Zalecaną nazwą będzie wskazanie gniazda, które otrzyma dane doświadczenie.</span><span class="sxs-lookup"><span data-stu-id="f21b1-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="f21b1-234">`[ReroutePercentage <Double?>]`: Procent ruchu, do którego będzie przekierowywany <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="f21b1-235">`[FtpsState <FtpsState?>]`: Stan usługi FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="f21b1-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="f21b1-236">`[HandlerMapping <IHandlerMapping[]>]`: Mapowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="f21b1-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="f21b1-237">`[Argument <String>]`: Argumenty wiersza polecenia, które mają być przekazywane do procesora skryptów.</span><span class="sxs-lookup"><span data-stu-id="f21b1-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="f21b1-238">`[Extension <String>]`: Żądania dotyczące tego rozszerzenia będą obsługiwane przy użyciu określonej aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="f21b1-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="f21b1-239">`[ScriptProcessor <String>]`: Ścieżka bezwzględna do aplikacji FastCGI.</span><span class="sxs-lookup"><span data-stu-id="f21b1-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="f21b1-240">`[HealthCheckPath <String>]`: Ścieżka kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="f21b1-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="f21b1-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web, aby umożliwić klientom nawiązywanie połączenia za pośrednictwem protokołu HTTP 2.0</span><span class="sxs-lookup"><span data-stu-id="f21b1-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="f21b1-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Jeśli rejestrowanie http jest włączone; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Ograniczenia zabezpieczeń IP dla głównego.</span><span class="sxs-lookup"><span data-stu-id="f21b1-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="f21b1-244">`[Action <String>]`: Zezwalanie na dostęp lub odmawianie dostępu do tego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="f21b1-245">`[Description <String>]`: Opis reguły ograniczeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="f21b1-246">`[IPAddress <String>]`: Adres IP obowiązuje ograniczenie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f21b1-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="f21b1-247">Może być w formie czystych adresów IPv4 (wymaganej właściwości maska_podsieci) lub notacji CIDR, takiej jak IPv4/Maska (z wiodącym dopasowaniem bitów).</span><span class="sxs-lookup"><span data-stu-id="f21b1-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="f21b1-248">W przypadku CIDR nie wolno określać właściwości maska_podsieci.</span><span class="sxs-lookup"><span data-stu-id="f21b1-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="f21b1-249">`[Name <String>]`: Nazwa reguły ograniczania adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="f21b1-250">`[Priority <Int32?>]`: Priorytet reguły ograniczenia IP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="f21b1-251">`[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których obowiązuje ograniczenie.</span><span class="sxs-lookup"><span data-stu-id="f21b1-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="f21b1-252">`[SubnetTrafficTag <Int32?>]`: (wewnętrzny) znacznik ruchu podsieci</span><span class="sxs-lookup"><span data-stu-id="f21b1-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="f21b1-253">`[Tag <IPFilterTag?>]`: Określa, do czego będzie stosowany ten filtr IP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="f21b1-254">Jest to obsługa filtrowania adresów IP na serwerach proxy.</span><span class="sxs-lookup"><span data-stu-id="f21b1-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="f21b1-255">`[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f21b1-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="f21b1-256">`[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci VNET</span><span class="sxs-lookup"><span data-stu-id="f21b1-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="f21b1-257">`[JavaContainer <String>]`: Kontener Java.</span><span class="sxs-lookup"><span data-stu-id="f21b1-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="f21b1-258">`[JavaContainerVersion <String>]`: Wersja kontenera Java.</span><span class="sxs-lookup"><span data-stu-id="f21b1-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="f21b1-259">`[JavaVersion <String>]`: Wersja Java.</span><span class="sxs-lookup"><span data-stu-id="f21b1-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="f21b1-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalne dozwolone użycie rozmiaru dysku (w MB).</span><span class="sxs-lookup"><span data-stu-id="f21b1-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="f21b1-261">`[LimitMaxMemoryInMb <Int64?>]`: Maksymalne dozwolone użycie pamięci w MB.</span><span class="sxs-lookup"><span data-stu-id="f21b1-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="f21b1-262">`[LimitMaxPercentageCpu <Double?>]`: Maksymalny dozwolony procent użycia procesora CPU.</span><span class="sxs-lookup"><span data-stu-id="f21b1-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="f21b1-263">`[LinuxFxVersion <String>]`: Struktura i wersja aplikacji Linux</span><span class="sxs-lookup"><span data-stu-id="f21b1-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="f21b1-264">`[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.</span><span class="sxs-lookup"><span data-stu-id="f21b1-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="f21b1-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> Aby włączyć lokalną MySQL; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-266">`[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogu dziennika HTTP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="f21b1-267">`[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.</span><span class="sxs-lookup"><span data-stu-id="f21b1-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="f21b1-268">`[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowujący.</span><span class="sxs-lookup"><span data-stu-id="f21b1-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="f21b1-269">`[MachineKeyValidation <String>]`: MachineKey sprawdzanie poprawności.</span><span class="sxs-lookup"><span data-stu-id="f21b1-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="f21b1-270">`[MachineKeyValidationKey <String>]`: Klucz sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="f21b1-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="f21b1-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Zarządzany tryb potokowy.</span><span class="sxs-lookup"><span data-stu-id="f21b1-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="f21b1-272">`[ManagedServiceIdentityId <Int32?>]`: Zarządzany identyfikator tożsamości usługi</span><span class="sxs-lookup"><span data-stu-id="f21b1-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="f21b1-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję TLS wymaganą dla żądań SSL</span><span class="sxs-lookup"><span data-stu-id="f21b1-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="f21b1-274">`[NetFrameworkVersion <String>]`: Wersja programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f21b1-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="f21b1-275">`[NodeVersion <String>]`: Wersja programu Node.js.</span><span class="sxs-lookup"><span data-stu-id="f21b1-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="f21b1-276">`[NumberOfWorker <Int32?>]`: Liczba pracowników.</span><span class="sxs-lookup"><span data-stu-id="f21b1-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="f21b1-277">`[PhpVersion <String>]`: Wersja programu PHP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="f21b1-278">`[PowerShellVersion <String>]`: Wersja programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f21b1-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="f21b1-279">`[PreWarmedInstanceCount <Int32?>]`: Liczba przedgrzanych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="f21b1-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="f21b1-280">To ustawienie dotyczy tylko planów zużycia i elastyczności</span><span class="sxs-lookup"><span data-stu-id="f21b1-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="f21b1-281">`[PublishingUsername <String>]`: Publikowanie nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f21b1-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="f21b1-282">`[PushKind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="f21b1-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="f21b1-283">`[PythonVersion <String>]`: Wersja języka Python.</span><span class="sxs-lookup"><span data-stu-id="f21b1-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="f21b1-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Jeśli debugowanie zdalne jest włączone, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-285">`[RemoteDebuggingVersion <String>]`: Zdalna wersja debugowania.</span><span class="sxs-lookup"><span data-stu-id="f21b1-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="f21b1-286">`[RequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="f21b1-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="f21b1-287">`[RequestTimeInterval <String>]`: Interwał czasowy.</span><span class="sxs-lookup"><span data-stu-id="f21b1-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="f21b1-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> Jeśli śledzenie żądań jest włączone, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-289">`[RequestTracingExpirationTime <DateTime?>]`: Czas wygaśnięcia śledzenia żądań.</span><span class="sxs-lookup"><span data-stu-id="f21b1-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="f21b1-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Ograniczenia zabezpieczeń IP dla SCM.</span><span class="sxs-lookup"><span data-stu-id="f21b1-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="f21b1-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Ograniczenia zabezpieczeń IP dla SCM umożliwiają korzystanie z głównego.</span><span class="sxs-lookup"><span data-stu-id="f21b1-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="f21b1-292">`[ScmType <ScmType?>]`: Typ SCM.</span><span class="sxs-lookup"><span data-stu-id="f21b1-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="f21b1-293">`[SlowRequestCount <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="f21b1-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="f21b1-294">`[SlowRequestTimeInterval <String>]`: Interwał czasowy.</span><span class="sxs-lookup"><span data-stu-id="f21b1-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="f21b1-295">`[SlowRequestTimeTaken <String>]`: Czas trwania.</span><span class="sxs-lookup"><span data-stu-id="f21b1-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="f21b1-296">`[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są whitelisted do użytku w punkcie końcowym rejestracji wypychanej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="f21b1-297">`[TagsRequiringAuth <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które wymagają uwierzytelnienia użytkownika do użycia w punkcie końcowym rejestracji wypychanej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="f21b1-298">Tagi mogą składać się z znaków alfanumerycznych i następujących elementów: _, "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="f21b1-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="f21b1-299">Sprawdzanie poprawności należy przeprowadzić na PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="f21b1-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="f21b1-300">`[TracingOption <String>]`: Opcje śledzenia.</span><span class="sxs-lookup"><span data-stu-id="f21b1-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="f21b1-301">`[TriggerPrivateBytesInKb <Int32?>]`: Reguła oparta na bajtach prywatnych.</span><span class="sxs-lookup"><span data-stu-id="f21b1-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="f21b1-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Reguła oparta na kodach statusu.</span><span class="sxs-lookup"><span data-stu-id="f21b1-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="f21b1-303">`[Count <Int32?>]`: Liczba żądań.</span><span class="sxs-lookup"><span data-stu-id="f21b1-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="f21b1-304">`[Status <Int32?>]`: Kod stanu HTTP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="f21b1-305">`[SubStatus <Int32?>]`: Żądanie podrzędne o statusie.</span><span class="sxs-lookup"><span data-stu-id="f21b1-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="f21b1-306">`[TimeInterval <String>]`: Interwał czasowy.</span><span class="sxs-lookup"><span data-stu-id="f21b1-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="f21b1-307">`[Win32Status <Int32?>]`: Kod błędu Win32.</span><span class="sxs-lookup"><span data-stu-id="f21b1-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="f21b1-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> Aby używać usługi 32-bitowego procesu roboczego, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-309">`[VirtualApplication <IVirtualApplication[]>]`: Aplikacje wirtualne.</span><span class="sxs-lookup"><span data-stu-id="f21b1-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="f21b1-310">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="f21b1-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="f21b1-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> Jeśli wstępne ładowanie jest włączone; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="f21b1-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Katalogi wirtualne aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="f21b1-313">`[PhysicalPath <String>]`: Ścieżka fizyczna.</span><span class="sxs-lookup"><span data-stu-id="f21b1-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="f21b1-314">`[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="f21b1-315">`[VirtualPath <String>]`: Ścieżka wirtualna.</span><span class="sxs-lookup"><span data-stu-id="f21b1-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="f21b1-316">`[VnetName <String>]`: Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f21b1-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="f21b1-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> Jeśli protokół WebSocket jest włączony; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f21b1-318">`[WindowsFxVersion <String>]`: Struktura i wersja aplikacji Xenon</span><span class="sxs-lookup"><span data-stu-id="f21b1-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="f21b1-319">`[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="f21b1-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="f21b1-320">`[ContainerSize <Int32?>]`: Rozmiar kontenera funkcji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="f21b1-321">`[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony przydział czasu na pamięć (dotyczy tylko aplikacji dynamicznych).</span><span class="sxs-lookup"><span data-stu-id="f21b1-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="f21b1-322">`[Enabled <Boolean?>]`: <code>true</code> Jeśli aplikacja jest włączona, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="f21b1-323">Ustawienie tej wartości na wartość FAŁSZ wyłącza aplikację (Pobiera aplikację w trybie offline).</span><span class="sxs-lookup"><span data-stu-id="f21b1-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="f21b1-324">`[HostNameSslState <IHostNameSslState[]>]`: Stany SSL hosta służą do zarządzania powiązaniami protokołu SSL dla hostów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f21b1-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="f21b1-325">`[HostType <HostType?>]`: Wskazuje, czy nazwa hosta jest nazwą hosta standardowego, czy repozytorium.</span><span class="sxs-lookup"><span data-stu-id="f21b1-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="f21b1-326">`[Name <String>]`Nazwą.</span><span class="sxs-lookup"><span data-stu-id="f21b1-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="f21b1-327">`[SslState <SslState?>]`: Typ protokołu SSL.</span><span class="sxs-lookup"><span data-stu-id="f21b1-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="f21b1-328">`[Thumbprint <String>]`: Odcisk palca certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="f21b1-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="f21b1-329">`[ToUpdate <Boolean?>]`: Ustawienie w celu <code>true</code> zaktualizowania istniejącej nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="f21b1-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="f21b1-330">`[VirtualIP <String>]`: Wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na protokole IP.</span><span class="sxs-lookup"><span data-stu-id="f21b1-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="f21b1-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> Aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="f21b1-332">Jeśli <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f21b1-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="f21b1-333">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu środowiska App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="f21b1-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="f21b1-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web w celu akceptowania tylko żądań HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f21b1-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="f21b1-335">Problemy z przekierowaniem dla żądań http</span><span class="sxs-lookup"><span data-stu-id="f21b1-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="f21b1-336">`[HyperV <Boolean?>]`: Piaskownica funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f21b1-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="f21b1-337">`[IdentityType <ManagedServiceIdentityType?>]`: Typ zarządzanej tożsamości usługi.</span><span class="sxs-lookup"><span data-stu-id="f21b1-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="f21b1-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Lista tożsamości przypisanych użytkownikowi skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="f21b1-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="f21b1-339">Odwołania do kluczy słownika tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="f21b1-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="f21b1-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="f21b1-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f21b1-341">`[IsXenon <Boolean?>]`: Przestarzałe: Piaskownica funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f21b1-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="f21b1-342">`[RedundancyMode <RedundancyMode?>]`: Tryb nadmiarowości witryny</span><span class="sxs-lookup"><span data-stu-id="f21b1-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="f21b1-343">`[Reserved <Boolean?>]`: <code>true</code> Jeśli jest zarezerwowany; w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f21b1-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> Aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana, w przeciwnym razie <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="f21b1-345">Wartość domyślna to <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f21b1-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="f21b1-346">`[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi App Service, sformatowana jako: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="f21b1-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="f21b1-347">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f21b1-347">RELATED LINKS</span></span>

