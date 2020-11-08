---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063765"
---
# <span data-ttu-id="0ea8b-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-101">Set-AzWebApp</span></span>

## <span data-ttu-id="0ea8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ea8b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea8b-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="0ea8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ea8b-104">SYNTAX</span></span>

### <span data-ttu-id="0ea8b-105">S1</span><span class="sxs-lookup"><span data-stu-id="0ea8b-105">S1</span></span>
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

### <span data-ttu-id="0ea8b-106">S2</span><span class="sxs-lookup"><span data-stu-id="0ea8b-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ea8b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0ea8b-107">DESCRIPTION</span></span>
<span data-ttu-id="0ea8b-108">Polecenie cmdlet **Set-AzWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="0ea8b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ea8b-109">EXAMPLES</span></span>

### <span data-ttu-id="0ea8b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ea8b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="0ea8b-111">To polecenie powoduje zmianę planu appService skojarzonego z aplikacją sieci Web ContosoWebApp skojarzoną z domyślną grupą zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="0ea8b-112">Użyj tego linku, aby dowiedzieć się więcej o zmienianiu appService planu i ograniczeń z nim skojarzonych.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="0ea8b-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="0ea8b-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="0ea8b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0ea8b-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="0ea8b-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="0ea8b-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0ea8b-116">Example 3</span></span>

<span data-ttu-id="0ea8b-117">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="0ea8b-118">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="0ea8b-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="0ea8b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ea8b-119">PARAMETERS</span></span>

### <span data-ttu-id="0ea8b-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="0ea8b-120">-AlwaysOn</span></span>
<span data-ttu-id="0ea8b-121">Upewnij się, że aplikacja internetowa jest ładowana przez cały czas, a nie rozładowana po okresie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="0ea8b-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea8b-122">-AppServicePlan</span></span>
<span data-ttu-id="0ea8b-123">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="0ea8b-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="0ea8b-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="0ea8b-124">-AppSettings</span></span>
<span data-ttu-id="0ea8b-125">Ustawienia aplikacji HashTable.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-125">App Settings HashTable.</span></span> <span data-ttu-id="0ea8b-126">Istniejące ustawienia aplikacji zostaną zastąpione, co spowoduje usunięcie wszystkich ustawień, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="0ea8b-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ea8b-127">-AsJob</span></span>
<span data-ttu-id="0ea8b-128">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0ea8b-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ea8b-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0ea8b-129">-AssignIdentity</span></span>
<span data-ttu-id="0ea8b-130">Włączanie/wyłączanie Instalatora MSI na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="0ea8b-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="0ea8b-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="0ea8b-132">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="0ea8b-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="0ea8b-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="0ea8b-133">-AzureStoragePath</span></span>
<span data-ttu-id="0ea8b-134">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="0ea8b-135">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="0ea8b-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="0ea8b-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="0ea8b-136">-ConnectionStrings</span></span>
<span data-ttu-id="0ea8b-137">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="0ea8b-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="0ea8b-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="0ea8b-138">-ContainerImageName</span></span>
<span data-ttu-id="0ea8b-139">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="0ea8b-139">Container Image Name</span></span>

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

### <span data-ttu-id="0ea8b-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="0ea8b-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="0ea8b-141">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="0ea8b-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="0ea8b-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="0ea8b-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="0ea8b-143">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="0ea8b-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="0ea8b-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="0ea8b-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="0ea8b-145">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="0ea8b-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="0ea8b-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="0ea8b-146">-DefaultDocuments</span></span>
<span data-ttu-id="0ea8b-147">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="0ea8b-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="0ea8b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea8b-148">-DefaultProfile</span></span>
<span data-ttu-id="0ea8b-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea8b-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ea8b-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="0ea8b-151">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="0ea8b-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="0ea8b-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="0ea8b-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="0ea8b-153">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="0ea8b-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="0ea8b-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="0ea8b-154">-FtpsState</span></span>
<span data-ttu-id="0ea8b-155">Ustaw wartość stanu FTPS dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="0ea8b-156">Dozwolone wartości [AllAllowed | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="0ea8b-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="0ea8b-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="0ea8b-157">-HandlerMappings</span></span>
<span data-ttu-id="0ea8b-158">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="0ea8b-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="0ea8b-159">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="0ea8b-159">-HostNames</span></span>
<span data-ttu-id="0ea8b-160">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea8b-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="0ea8b-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ea8b-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="0ea8b-162">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ea8b-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="0ea8b-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0ea8b-163">-HttpsOnly</span></span>
<span data-ttu-id="0ea8b-164">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="0ea8b-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="0ea8b-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="0ea8b-166">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="0ea8b-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="0ea8b-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0ea8b-167">-MinTlsVersion</span></span>
<span data-ttu-id="0ea8b-168">Minimalna wersja protokołu TLS wymagana w przypadku żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="0ea8b-169">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="0ea8b-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="0ea8b-170">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ea8b-170">-Name</span></span>
<span data-ttu-id="0ea8b-171">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea8b-171">WebApp Name</span></span>

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

### <span data-ttu-id="0ea8b-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="0ea8b-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="0ea8b-173">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="0ea8b-173">Net Framework Version</span></span>

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

### <span data-ttu-id="0ea8b-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="0ea8b-174">-NumberOfWorkers</span></span>
<span data-ttu-id="0ea8b-175">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="0ea8b-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="0ea8b-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="0ea8b-176">-PhpVersion</span></span>
<span data-ttu-id="0ea8b-177">Wersja php</span><span class="sxs-lookup"><span data-stu-id="0ea8b-177">Php Version</span></span>

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

### <span data-ttu-id="0ea8b-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ea8b-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="0ea8b-179">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="0ea8b-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="0ea8b-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea8b-180">-ResourceGroupName</span></span>
<span data-ttu-id="0ea8b-181">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0ea8b-181">Resource Group Name</span></span>

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

### <span data-ttu-id="0ea8b-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="0ea8b-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="0ea8b-183">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="0ea8b-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="0ea8b-184">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea8b-184">-WebApp</span></span>
<span data-ttu-id="0ea8b-185">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea8b-185">WebApp Object</span></span>

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

### <span data-ttu-id="0ea8b-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="0ea8b-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="0ea8b-187">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="0ea8b-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="0ea8b-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea8b-188">CommonParameters</span></span>
<span data-ttu-id="0ea8b-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea8b-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ea8b-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea8b-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ea8b-191">INPUTS</span></span>

### <span data-ttu-id="0ea8b-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0ea8b-192">System.Int32</span></span>

### <span data-ttu-id="0ea8b-193">System. String</span><span class="sxs-lookup"><span data-stu-id="0ea8b-193">System.String</span></span>

### <span data-ttu-id="0ea8b-194">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="0ea8b-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0ea8b-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ea8b-195">OUTPUTS</span></span>

### <span data-ttu-id="0ea8b-196">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="0ea8b-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0ea8b-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ea8b-197">NOTES</span></span>
<span data-ttu-id="0ea8b-198">Poniższe podane polecenie cmdlet ułatwi zaktualizowanie aplikacji Azure Web App do **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="0ea8b-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="0ea8b-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-Propertyobject $PropertiesObject-ResourceGroupName "Default-Web-Westname"-ResourceType Microsoft. Web/Sites/config-resourceName "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="0ea8b-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="0ea8b-200">Zamienianie wartości Default-Web-zachód na nazwę grupy zasobów aplikacji i ContosoWebApp z nazwą aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ea8b-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="0ea8b-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ea8b-201">RELATED LINKS</span></span>

[<span data-ttu-id="0ea8b-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0ea8b-203">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0ea8b-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0ea8b-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0ea8b-206">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0ea8b-207">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ea8b-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="0ea8b-208">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="0ea8b-208">New-AzResource</span></span>](./New-AzResource.md)
