---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489674"
---
# <span data-ttu-id="be59f-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="be59f-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="be59f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be59f-102">SYNOPSIS</span></span>
<span data-ttu-id="be59f-103">Tworzy aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-103">Creates a function app.</span></span>

## <span data-ttu-id="be59f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be59f-104">SYNTAX</span></span>

### <span data-ttu-id="be59f-105">Zużycie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="be59f-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be59f-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="be59f-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be59f-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="be59f-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be59f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="be59f-108">DESCRIPTION</span></span>
<span data-ttu-id="be59f-109">Tworzy aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-109">Creates a function app.</span></span>

## <span data-ttu-id="be59f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be59f-110">EXAMPLES</span></span>

### <span data-ttu-id="be59f-111">Przykład 1: Tworzenie aplikacji do obsługi funkcji programu PowerShell w centrum Central my.</span><span class="sxs-lookup"><span data-stu-id="be59f-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="be59f-112">To polecenie tworzy aplikację funkcji programu PowerShell w centrum Central my.</span><span class="sxs-lookup"><span data-stu-id="be59f-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="be59f-113">Przykład 2: Tworzenie aplikacji funkcji programu PowerShell, która będzie hostowana w planie usługi.</span><span class="sxs-lookup"><span data-stu-id="be59f-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="be59f-114">To polecenie tworzy aplikację funkcji programu PowerShell, która będzie hostowana w planie usług.</span><span class="sxs-lookup"><span data-stu-id="be59f-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="be59f-115">Przykład 3: Tworzenie aplikacji funkcji przy użyciu prywatnego obrazu ACR.</span><span class="sxs-lookup"><span data-stu-id="be59f-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="be59f-116">To polecenie tworzy aplikację funkcji przy użyciu obrazu prywatnego ACR.</span><span class="sxs-lookup"><span data-stu-id="be59f-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="be59f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be59f-117">PARAMETERS</span></span>

### <span data-ttu-id="be59f-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="be59f-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="be59f-119">Klucz Instrumentacji aplikacji, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="be59f-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="be59f-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="be59f-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="be59f-121">Nazwa istniejącego projektu usługi App Insights, który ma zostać dodany do aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="be59f-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="be59f-122">-AppSetting</span></span>
<span data-ttu-id="be59f-123">Ustawienia aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-123">Function app settings.</span></span>

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

### <span data-ttu-id="be59f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be59f-124">-AsJob</span></span>
<span data-ttu-id="be59f-125">Uruchamia polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="be59f-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="be59f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be59f-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="be59f-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="be59f-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="be59f-128">Wyłączenie tworzenia zasobu usługi Application Insights podczas tworzenia aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="be59f-129">Żadne dzienniki nie będą dostępne.</span><span class="sxs-lookup"><span data-stu-id="be59f-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="be59f-130">-DockerImageName</span></span>
<span data-ttu-id="be59f-131">Tylko Linux.</span><span class="sxs-lookup"><span data-stu-id="be59f-131">Linux only.</span></span>
<span data-ttu-id="be59f-132">Nazwa obrazu kontenera z rejestru dokowania, na przykład "Publisher/Image-Name": znacznik.</span><span class="sxs-lookup"><span data-stu-id="be59f-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="be59f-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="be59f-134">Nazwa użytkownika i hasło rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="be59f-134">The container registry user name and password.</span></span>
<span data-ttu-id="be59f-135">Wymagane w przypadku prywatnych kancelarii.</span><span class="sxs-lookup"><span data-stu-id="be59f-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="be59f-136">-FunctionsVersion</span></span>
<span data-ttu-id="be59f-137">Wersja funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="be59f-138">-IdentityID</span></span>
<span data-ttu-id="be59f-139">Określa listę tożsamości użytkowników skojarzonych z aplikacją funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="be59f-140">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="be59f-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="be59f-141">-IdentityType</span></span>
<span data-ttu-id="be59f-142">Określa typ tożsamości używanej przez aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="be59f-143">Dopuszczalne wartości tego parametru to:-SystemAssigned-UserAssigned</span><span class="sxs-lookup"><span data-stu-id="be59f-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="be59f-144">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="be59f-144">-Location</span></span>
<span data-ttu-id="be59f-145">Lokalizacja planu zużycia.</span><span class="sxs-lookup"><span data-stu-id="be59f-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be59f-146">-Name</span></span>
<span data-ttu-id="be59f-147">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-147">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="be59f-148">-NoWait</span></span>
<span data-ttu-id="be59f-149">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="be59f-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="be59f-150">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="be59f-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="be59f-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="be59f-151">-OSType</span></span>
<span data-ttu-id="be59f-152">System operacyjny do obsługi aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be59f-153">-PassThru</span></span>
<span data-ttu-id="be59f-154">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="be59f-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="be59f-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="be59f-155">-PlanName</span></span>
<span data-ttu-id="be59f-156">Nazwa planu usługi.</span><span class="sxs-lookup"><span data-stu-id="be59f-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be59f-157">-ResourceGroupName</span></span>
<span data-ttu-id="be59f-158">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be59f-158">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="be59f-159">-Runtime</span></span>
<span data-ttu-id="be59f-160">Środowisko uruchomieniowe funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="be59f-161">-RuntimeVersion</span></span>
<span data-ttu-id="be59f-162">Środowisko uruchomieniowe funkcji.</span><span class="sxs-lookup"><span data-stu-id="be59f-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="be59f-163">-StorageAccountName</span></span>
<span data-ttu-id="be59f-164">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="be59f-164">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-165">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="be59f-165">-SubscriptionId</span></span>
<span data-ttu-id="be59f-166">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be59f-166">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be59f-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="be59f-167">-Tag</span></span>
<span data-ttu-id="be59f-168">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="be59f-168">Resource tags.</span></span>

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

### <span data-ttu-id="be59f-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be59f-169">-Confirm</span></span>
<span data-ttu-id="be59f-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be59f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be59f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be59f-171">-WhatIf</span></span>
<span data-ttu-id="be59f-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be59f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be59f-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="be59f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be59f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be59f-174">CommonParameters</span></span>
<span data-ttu-id="be59f-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be59f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be59f-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be59f-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be59f-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be59f-177">INPUTS</span></span>

## <span data-ttu-id="be59f-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be59f-178">OUTPUTS</span></span>

### <span data-ttu-id="be59f-179">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="be59f-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="be59f-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be59f-180">NOTES</span></span>

<span data-ttu-id="be59f-181">PISUJE</span><span class="sxs-lookup"><span data-stu-id="be59f-181">ALIASES</span></span>

## <span data-ttu-id="be59f-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be59f-182">RELATED LINKS</span></span>

