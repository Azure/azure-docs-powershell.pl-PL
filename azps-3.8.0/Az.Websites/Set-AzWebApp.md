---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 75ee07a9ce74f5b2667d8197ca141883508faa1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051868"
---
# <span data-ttu-id="ad3d3-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-101">Set-AzWebApp</span></span>

## <span data-ttu-id="ad3d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3d3-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="ad3d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad3d3-104">SYNTAX</span></span>

### <span data-ttu-id="ad3d3-105">S1</span><span class="sxs-lookup"><span data-stu-id="ad3d3-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad3d3-106">S2</span><span class="sxs-lookup"><span data-stu-id="ad3d3-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad3d3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad3d3-107">DESCRIPTION</span></span>
<span data-ttu-id="ad3d3-108">Polecenie cmdlet **Set-AzWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="ad3d3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad3d3-109">EXAMPLES</span></span>

### <span data-ttu-id="ad3d3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad3d3-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="ad3d3-111">To polecenie powoduje zmianę planu appService skojarzonego z aplikacją sieci Web ContosoWebApp skojarzoną z domyślną grupą zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="ad3d3-112">Użyj tego linku, aby dowiedzieć się więcej o zmienianiu appService planu i ograniczeń z nim skojarzonych.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="ad3d3-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="ad3d3-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="ad3d3-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ad3d3-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="ad3d3-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ad3d3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad3d3-116">PARAMETERS</span></span>

### <span data-ttu-id="ad3d3-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="ad3d3-117">-AlwaysOn</span></span>
<span data-ttu-id="ad3d3-118">Upewnij się, że aplikacja internetowa jest ładowana przez cały czas, a nie rozładowana po okresie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="ad3d3-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad3d3-119">-AppServicePlan</span></span>
<span data-ttu-id="ad3d3-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="ad3d3-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ad3d3-121">-AppSettings</span></span>
<span data-ttu-id="ad3d3-122">Ustawienia aplikacji HashTable.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-122">App Settings HashTable.</span></span> <span data-ttu-id="ad3d3-123">Istniejące ustawienia aplikacji zostaną zastąpione, co spowoduje usunięcie wszystkich ustawień, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad3d3-124">-AsJob</span></span>
<span data-ttu-id="ad3d3-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ad3d3-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad3d3-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ad3d3-126">-AssignIdentity</span></span>
<span data-ttu-id="ad3d3-127">Włączanie/wyłączanie Instalatora MSI na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-127">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="ad3d3-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ad3d3-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="ad3d3-129">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="ad3d3-129">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ad3d3-130">-AzureStoragePath</span></span>
<span data-ttu-id="ad3d3-131">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="ad3d3-132">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ad3d3-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="ad3d3-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ad3d3-133">-ConnectionStrings</span></span>
<span data-ttu-id="ad3d3-134">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="ad3d3-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ad3d3-135">-ContainerImageName</span></span>
<span data-ttu-id="ad3d3-136">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="ad3d3-136">Container Image Name</span></span>

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

### <span data-ttu-id="ad3d3-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ad3d3-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ad3d3-138">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="ad3d3-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="ad3d3-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ad3d3-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ad3d3-140">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="ad3d3-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="ad3d3-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ad3d3-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="ad3d3-142">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="ad3d3-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="ad3d3-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ad3d3-143">-DefaultDocuments</span></span>
<span data-ttu-id="ad3d3-144">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="ad3d3-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3d3-145">-DefaultProfile</span></span>
<span data-ttu-id="ad3d3-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad3d3-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad3d3-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ad3d3-148">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="ad3d3-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ad3d3-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ad3d3-150">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="ad3d3-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="ad3d3-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="ad3d3-151">-FtpsState</span></span>
<span data-ttu-id="ad3d3-152">Ustaw wartość stanu FTPS dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="ad3d3-153">Dozwolone wartości [AllAllowed | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="ad3d3-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="ad3d3-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ad3d3-154">-HandlerMappings</span></span>
<span data-ttu-id="ad3d3-155">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="ad3d3-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-156">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="ad3d3-156">-HostNames</span></span>
<span data-ttu-id="ad3d3-157">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="ad3d3-157">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-158">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad3d3-158">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ad3d3-159">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad3d3-159">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-160">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ad3d3-160">-HttpsOnly</span></span>
<span data-ttu-id="ad3d3-161">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-161">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="ad3d3-162">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ad3d3-162">-ManagedPipelineMode</span></span>
<span data-ttu-id="ad3d3-163">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="ad3d3-163">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-164">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ad3d3-164">-MinTlsVersion</span></span>
<span data-ttu-id="ad3d3-165">Minimalna wersja protokołu TLS wymagana w przypadku żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-165">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="ad3d3-166">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="ad3d3-166">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="ad3d3-167">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad3d3-167">-Name</span></span>
<span data-ttu-id="ad3d3-168">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="ad3d3-168">WebApp Name</span></span>

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

### <span data-ttu-id="ad3d3-169">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ad3d3-169">-NetFrameworkVersion</span></span>
<span data-ttu-id="ad3d3-170">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="ad3d3-170">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-171">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ad3d3-171">-NumberOfWorkers</span></span>
<span data-ttu-id="ad3d3-172">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="ad3d3-172">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="ad3d3-173">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ad3d3-173">-PhpVersion</span></span>
<span data-ttu-id="ad3d3-174">Wersja php</span><span class="sxs-lookup"><span data-stu-id="ad3d3-174">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-175">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad3d3-175">-RequestTracingEnabled</span></span>
<span data-ttu-id="ad3d3-176">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="ad3d3-176">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3d3-177">-ResourceGroupName</span></span>
<span data-ttu-id="ad3d3-178">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ad3d3-178">Resource Group Name</span></span>

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

### <span data-ttu-id="ad3d3-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ad3d3-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ad3d3-180">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="ad3d3-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="ad3d3-181">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="ad3d3-181">-WebApp</span></span>
<span data-ttu-id="ad3d3-182">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="ad3d3-182">WebApp Object</span></span>

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

### <span data-ttu-id="ad3d3-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad3d3-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="ad3d3-184">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad3d3-184">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3d3-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3d3-185">CommonParameters</span></span>
<span data-ttu-id="ad3d3-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3d3-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3d3-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad3d3-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3d3-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad3d3-188">INPUTS</span></span>

### <span data-ttu-id="ad3d3-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad3d3-189">System.Int32</span></span>

### <span data-ttu-id="ad3d3-190">System. String</span><span class="sxs-lookup"><span data-stu-id="ad3d3-190">System.String</span></span>

### <span data-ttu-id="ad3d3-191">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="ad3d3-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ad3d3-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad3d3-192">OUTPUTS</span></span>

### <span data-ttu-id="ad3d3-193">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="ad3d3-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ad3d3-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad3d3-194">NOTES</span></span>

## <span data-ttu-id="ad3d3-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad3d3-195">RELATED LINKS</span></span>

[<span data-ttu-id="ad3d3-196">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-196">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ad3d3-197">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-197">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ad3d3-198">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-198">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ad3d3-199">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-199">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ad3d3-200">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-200">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ad3d3-201">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ad3d3-201">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
