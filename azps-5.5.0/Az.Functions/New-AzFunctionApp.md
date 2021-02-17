---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196290"
---
# <span data-ttu-id="d2f9b-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d2f9b-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="d2f9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f9b-103">Tworzy aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-103">Creates a function app.</span></span>

## <span data-ttu-id="d2f9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2f9b-104">SYNTAX</span></span>

### <span data-ttu-id="d2f9b-105">Zużycie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d2f9b-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2f9b-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d2f9b-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2f9b-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="d2f9b-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2f9b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2f9b-108">DESCRIPTION</span></span>
<span data-ttu-id="d2f9b-109">Tworzy aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-109">Creates a function app.</span></span>

## <span data-ttu-id="d2f9b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2f9b-110">EXAMPLES</span></span>

### <span data-ttu-id="d2f9b-111">Przykład 1. Tworzenie aplikacji funkcyjnej PowerShell w Środkowych Usach.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="d2f9b-112">To polecenie tworzy w Centrum Stanów Zjednoczonych aplikację funkcji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="d2f9b-113">Przykład 2. Tworzenie aplikacji funkcji programu PowerShell, która będzie hostowana w planie usługi.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="d2f9b-114">To polecenie tworzy aplikację funkcji programu PowerShell, która będzie hostowana w planie usługi.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="d2f9b-115">Przykład 3. Tworzenie aplikacji funkcji przy użyciu prywatnego obrazu ACR.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="d2f9b-116">To polecenie umożliwia utworzenie aplikacji funkcji przy użyciu prywatnego obrazu ACR.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="d2f9b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2f9b-117">PARAMETERS</span></span>

### <span data-ttu-id="d2f9b-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="d2f9b-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="d2f9b-119">Klucz instrumentacji aplikacji do dodania.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="d2f9b-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="d2f9b-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="d2f9b-121">Nazwa istniejącego projektu szczegółowych informacji o aplikacji, który ma zostać dodany do aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="d2f9b-122">- AppSetting</span><span class="sxs-lookup"><span data-stu-id="d2f9b-122">-AppSetting</span></span>
<span data-ttu-id="d2f9b-123">Ustawienia aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-123">Function app settings.</span></span>

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

### <span data-ttu-id="d2f9b-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d2f9b-124">-AsJob</span></span>
<span data-ttu-id="d2f9b-125">Uruchamia polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="d2f9b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f9b-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="d2f9b-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d2f9b-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="d2f9b-128">Wyłącz tworzenie zasobu szczegółowych informacji o aplikacji podczas tworzenia aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="d2f9b-129">Dzienniki nie będą dostępne.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-129">No logs will be available.</span></span>

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

### <span data-ttu-id="d2f9b-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="d2f9b-130">-DockerImageName</span></span>
<span data-ttu-id="d2f9b-131">Tylko system Linux.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-131">Linux only.</span></span>
<span data-ttu-id="d2f9b-132">Nazwa obrazu kontenera z rejestru dockera, na przykład publisher/image-name:tag.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

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

### <span data-ttu-id="d2f9b-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d2f9b-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="d2f9b-134">Nazwa użytkownika i hasło rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-134">The container registry user name and password.</span></span>
<span data-ttu-id="d2f9b-135">Wymagane w przypadku rejestrów prywatnych.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-135">Required for private registries.</span></span>

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

### <span data-ttu-id="d2f9b-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="d2f9b-136">-FunctionsVersion</span></span>
<span data-ttu-id="d2f9b-137">Wersja funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-137">The Functions version.</span></span>

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

### <span data-ttu-id="d2f9b-138">- IdentityID</span><span class="sxs-lookup"><span data-stu-id="d2f9b-138">-IdentityID</span></span>
<span data-ttu-id="d2f9b-139">Określa listę tożsamości użytkowników skojarzonych z aplikacją funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="d2f9b-140">Odwołania do tożsamości użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="d2f9b-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="d2f9b-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d2f9b-141">-IdentityType</span></span>
<span data-ttu-id="d2f9b-142">Określa typ tożsamości używany w aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="d2f9b-143">Dopuszczalne wartości dla tego parametru to: - SystemAssigned - UserAssigned</span><span class="sxs-lookup"><span data-stu-id="d2f9b-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="d2f9b-144">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d2f9b-144">-Location</span></span>
<span data-ttu-id="d2f9b-145">Lokalizacja planu zużycia.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-145">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="d2f9b-146">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2f9b-146">-Name</span></span>
<span data-ttu-id="d2f9b-147">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-147">The name of the function app.</span></span>

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

### <span data-ttu-id="d2f9b-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2f9b-148">-NoWait</span></span>
<span data-ttu-id="d2f9b-149">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="d2f9b-150">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d2f9b-151">- OSType</span><span class="sxs-lookup"><span data-stu-id="d2f9b-151">-OSType</span></span>
<span data-ttu-id="d2f9b-152">System operacyjny do hostować aplikację funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-152">The OS to host the function app.</span></span>

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

### <span data-ttu-id="d2f9b-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2f9b-153">-PassThru</span></span>
<span data-ttu-id="d2f9b-154">Zwraca wartość true, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="d2f9b-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d2f9b-155">-PlanName</span></span>
<span data-ttu-id="d2f9b-156">Nazwa planu usługi.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-156">The name of the service plan.</span></span>

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

### <span data-ttu-id="d2f9b-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f9b-157">-ResourceGroupName</span></span>
<span data-ttu-id="d2f9b-158">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="d2f9b-159">— Środowisko uruchomieniowe</span><span class="sxs-lookup"><span data-stu-id="d2f9b-159">-Runtime</span></span>
<span data-ttu-id="d2f9b-160">Środowisko uruchomieniowe funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-160">The function runtime.</span></span>

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

### <span data-ttu-id="d2f9b-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="d2f9b-161">-RuntimeVersion</span></span>
<span data-ttu-id="d2f9b-162">Środowisko uruchomieniowe funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-162">The function runtime.</span></span>

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

### <span data-ttu-id="d2f9b-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2f9b-163">-StorageAccountName</span></span>
<span data-ttu-id="d2f9b-164">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="d2f9b-165">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2f9b-165">-SubscriptionId</span></span>
<span data-ttu-id="d2f9b-166">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d2f9b-167">— Tag</span><span class="sxs-lookup"><span data-stu-id="d2f9b-167">-Tag</span></span>
<span data-ttu-id="d2f9b-168">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-168">Resource tags.</span></span>

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

### <span data-ttu-id="d2f9b-169">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2f9b-169">-Confirm</span></span>
<span data-ttu-id="d2f9b-170">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f9b-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f9b-171">-WhatIf</span></span>
<span data-ttu-id="d2f9b-172">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f9b-173">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f9b-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f9b-174">CommonParameters</span></span>
<span data-ttu-id="d2f9b-175">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f9b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f9b-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2f9b-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f9b-177">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2f9b-177">INPUTS</span></span>

## <span data-ttu-id="d2f9b-178">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2f9b-178">OUTPUTS</span></span>

### <span data-ttu-id="d2f9b-179">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite</span><span class="sxs-lookup"><span data-stu-id="d2f9b-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="d2f9b-180">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2f9b-180">NOTES</span></span>

<span data-ttu-id="d2f9b-181">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d2f9b-181">ALIASES</span></span>

## <span data-ttu-id="d2f9b-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2f9b-182">RELATED LINKS</span></span>

