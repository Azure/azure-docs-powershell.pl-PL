---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051567"
---
# <span data-ttu-id="7b240-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b240-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="7b240-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b240-102">SYNOPSIS</span></span>
<span data-ttu-id="7b240-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7b240-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="7b240-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b240-104">SYNTAX</span></span>

### <span data-ttu-id="7b240-105">S1</span><span class="sxs-lookup"><span data-stu-id="7b240-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b240-106">S2</span><span class="sxs-lookup"><span data-stu-id="7b240-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b240-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7b240-107">DESCRIPTION</span></span>
<span data-ttu-id="7b240-108">Polecenie cmdlet **Set-AzWebApp** ustawia miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7b240-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="7b240-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b240-109">EXAMPLES</span></span>

### <span data-ttu-id="7b240-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b240-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="7b240-111">To polecenie powoduje zmianę planu appService skojarzonego z Slot001 na karcie aplikacji ContosoWebApp powiązanej z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="7b240-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="7b240-112">Użyj tego linku, aby dowiedzieć się więcej o zmienianiu appService planu i ograniczeń z nim skojarzonych.</span><span class="sxs-lookup"><span data-stu-id="7b240-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="7b240-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="7b240-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="7b240-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7b240-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="7b240-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla Slot001 gniazda odnoszącego się do aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="7b240-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7b240-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b240-116">PARAMETERS</span></span>

### <span data-ttu-id="7b240-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="7b240-117">-AlwaysOn</span></span>
<span data-ttu-id="7b240-118">Upewnij się, że aplikacja internetowa jest ładowana przez cały czas, a nie rozładowana po okresie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="7b240-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7b240-119">-AppServicePlan</span></span>
<span data-ttu-id="7b240-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="7b240-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="7b240-121">-AppSettings</span></span>
<span data-ttu-id="7b240-122">Ustawienia aplikacji HashTable.</span><span class="sxs-lookup"><span data-stu-id="7b240-122">App Settings HashTable.</span></span> <span data-ttu-id="7b240-123">Istniejące ustawienia aplikacji zostaną zastąpione, co spowoduje usunięcie wszystkich ustawień, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="7b240-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b240-124">-AsJob</span></span>
<span data-ttu-id="7b240-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7b240-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b240-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7b240-126">-AssignIdentity</span></span>
<span data-ttu-id="7b240-127">Włączanie/wyłączanie MSI w istniejącym gnieździe [Podgląd]</span><span class="sxs-lookup"><span data-stu-id="7b240-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="7b240-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="7b240-129">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="7b240-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="7b240-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="7b240-130">-AzureStoragePath</span></span>
<span data-ttu-id="7b240-131">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="7b240-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="7b240-132">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="7b240-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="7b240-133">-ConnectionStrings</span></span>
<span data-ttu-id="7b240-134">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="7b240-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="7b240-135">-ContainerImageName</span></span>
<span data-ttu-id="7b240-136">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="7b240-136">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="7b240-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="7b240-138">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="7b240-138">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="7b240-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="7b240-140">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="7b240-140">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="7b240-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="7b240-142">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="7b240-142">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="7b240-143">-DefaultDocuments</span></span>
<span data-ttu-id="7b240-144">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="7b240-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b240-145">-DefaultProfile</span></span>
<span data-ttu-id="7b240-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b240-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7b240-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="7b240-148">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="7b240-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="7b240-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="7b240-150">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="7b240-150">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="7b240-151">-FtpsState</span></span>
<span data-ttu-id="7b240-152">Ustaw wartość stanu FTPS dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7b240-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="7b240-153">Dozwolone wartości [AllAllowed | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="7b240-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="7b240-154">-HandlerMappings</span></span>
<span data-ttu-id="7b240-155">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="7b240-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7b240-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="7b240-157">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7b240-157">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7b240-158">-HttpsOnly</span></span>
<span data-ttu-id="7b240-159">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącym gnieździe</span><span class="sxs-lookup"><span data-stu-id="7b240-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="7b240-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="7b240-161">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="7b240-161">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7b240-162">-MinTlsVersion</span></span>
<span data-ttu-id="7b240-163">Minimalna wersja protokołu TLS wymagana w przypadku żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="7b240-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="7b240-164">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="7b240-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-165">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b240-165">-Name</span></span>
<span data-ttu-id="7b240-166">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7b240-166">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="7b240-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="7b240-168">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="7b240-168">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="7b240-169">-NumberOfWorkers</span></span>
<span data-ttu-id="7b240-170">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="7b240-170">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="7b240-171">-PhpVersion</span></span>
<span data-ttu-id="7b240-172">Wersja php</span><span class="sxs-lookup"><span data-stu-id="7b240-172">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="7b240-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="7b240-174">Wartość logiczna włączonego śledzenia żądań</span><span class="sxs-lookup"><span data-stu-id="7b240-174">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b240-175">-ResourceGroupName</span></span>
<span data-ttu-id="7b240-176">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7b240-176">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-177">-Slot</span><span class="sxs-lookup"><span data-stu-id="7b240-177">-Slot</span></span>
<span data-ttu-id="7b240-178">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="7b240-178">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="7b240-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="7b240-180">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="7b240-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-181">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7b240-181">-WebApp</span></span>
<span data-ttu-id="7b240-182">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7b240-182">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="7b240-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="7b240-184">Wartość logiczna z włączonymi gniazdami sieci Web</span><span class="sxs-lookup"><span data-stu-id="7b240-184">Web Sockets Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b240-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b240-185">CommonParameters</span></span>
<span data-ttu-id="7b240-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b240-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b240-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b240-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b240-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b240-188">INPUTS</span></span>

### <span data-ttu-id="7b240-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7b240-189">System.Int32</span></span>

### <span data-ttu-id="7b240-190">System. String</span><span class="sxs-lookup"><span data-stu-id="7b240-190">System.String</span></span>

### <span data-ttu-id="7b240-191">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="7b240-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7b240-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b240-192">OUTPUTS</span></span>

### <span data-ttu-id="7b240-193">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="7b240-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7b240-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b240-194">NOTES</span></span>

## <span data-ttu-id="7b240-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b240-195">RELATED LINKS</span></span>

[<span data-ttu-id="7b240-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b240-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="7b240-197">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b240-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="7b240-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b240-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="7b240-199">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b240-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="7b240-200">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b240-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="7b240-201">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b240-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="7b240-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7b240-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
