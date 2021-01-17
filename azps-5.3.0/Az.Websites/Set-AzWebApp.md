---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491409"
---
# <span data-ttu-id="091f7-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="091f7-101">Set-AzWebApp</span></span>

## <span data-ttu-id="091f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="091f7-102">SYNOPSIS</span></span>
<span data-ttu-id="091f7-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="091f7-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="091f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="091f7-104">SYNTAX</span></span>

### <span data-ttu-id="091f7-105">S1</span><span class="sxs-lookup"><span data-stu-id="091f7-105">S1</span></span>
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

### <span data-ttu-id="091f7-106">S2</span><span class="sxs-lookup"><span data-stu-id="091f7-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="091f7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="091f7-107">DESCRIPTION</span></span>
<span data-ttu-id="091f7-108">Polecenie cmdlet **Set-AzWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="091f7-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="091f7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="091f7-109">EXAMPLES</span></span>

### <span data-ttu-id="091f7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="091f7-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="091f7-111">To polecenie powoduje zmianę planu appService skojarzonego z aplikacją sieci Web ContosoWebApp skojarzoną z domyślną grupą zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="091f7-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="091f7-112">Użyj tego linku, aby dowiedzieć się więcej o zmienianiu appService planu i ograniczeń z nim skojarzonych.</span><span class="sxs-lookup"><span data-stu-id="091f7-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="091f7-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="091f7-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="091f7-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="091f7-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="091f7-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="091f7-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="091f7-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="091f7-116">Example 3</span></span>

<span data-ttu-id="091f7-117">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="091f7-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="091f7-118">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="091f7-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="091f7-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="091f7-119">Example 4</span></span>

<span data-ttu-id="091f7-120">W poniższym przykładzie są tworzone parametry połączenia o nazwie Moje ConnectionString dla aplikacji sieci Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="091f7-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="091f7-121">Spowoduje to zastąpienie wszystkich istniejących ciągów połączenia dla aplikacji sieci Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="091f7-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="091f7-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="091f7-122">PARAMETERS</span></span>

### <span data-ttu-id="091f7-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="091f7-123">-AlwaysOn</span></span>
<span data-ttu-id="091f7-124">Upewnij się, że aplikacja internetowa jest ładowana przez cały czas, a nie rozładowana po okresie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="091f7-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="091f7-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="091f7-125">-AppServicePlan</span></span>
<span data-ttu-id="091f7-126">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="091f7-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="091f7-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="091f7-127">-AppSettings</span></span>
<span data-ttu-id="091f7-128">Ustawienia aplikacji HashTable.</span><span class="sxs-lookup"><span data-stu-id="091f7-128">App Settings HashTable.</span></span> <span data-ttu-id="091f7-129">Istniejące ustawienia aplikacji zostaną zastąpione, co spowoduje usunięcie wszystkich ustawień, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="091f7-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="091f7-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="091f7-130">-AsJob</span></span>
<span data-ttu-id="091f7-131">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="091f7-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="091f7-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="091f7-132">-AssignIdentity</span></span>
<span data-ttu-id="091f7-133">Włączanie/wyłączanie Instalatora MSI na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="091f7-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="091f7-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="091f7-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="091f7-135">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="091f7-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="091f7-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="091f7-136">-AzureStoragePath</span></span>
<span data-ttu-id="091f7-137">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="091f7-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="091f7-138">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="091f7-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="091f7-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="091f7-139">-ConnectionStrings</span></span>
<span data-ttu-id="091f7-140">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="091f7-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="091f7-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="091f7-141">-ContainerImageName</span></span>
<span data-ttu-id="091f7-142">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="091f7-142">Container Image Name</span></span>

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

### <span data-ttu-id="091f7-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="091f7-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="091f7-144">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="091f7-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="091f7-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="091f7-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="091f7-146">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="091f7-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="091f7-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="091f7-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="091f7-148">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="091f7-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="091f7-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="091f7-149">-DefaultDocuments</span></span>
<span data-ttu-id="091f7-150">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="091f7-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="091f7-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091f7-151">-DefaultProfile</span></span>
<span data-ttu-id="091f7-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="091f7-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="091f7-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="091f7-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="091f7-154">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="091f7-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="091f7-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="091f7-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="091f7-156">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="091f7-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="091f7-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="091f7-157">-FtpsState</span></span>
<span data-ttu-id="091f7-158">Ustaw wartość stanu FTPS dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="091f7-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="091f7-159">Dozwolone wartości [AllAllowed | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="091f7-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="091f7-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="091f7-160">-HandlerMappings</span></span>
<span data-ttu-id="091f7-161">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="091f7-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="091f7-162">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="091f7-162">-HostNames</span></span>
<span data-ttu-id="091f7-163">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="091f7-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="091f7-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="091f7-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="091f7-165">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="091f7-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="091f7-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="091f7-166">-HttpsOnly</span></span>
<span data-ttu-id="091f7-167">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="091f7-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="091f7-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="091f7-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="091f7-169">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="091f7-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="091f7-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="091f7-170">-MinTlsVersion</span></span>
<span data-ttu-id="091f7-171">Minimalna wersja protokołu TLS wymagana w przypadku żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="091f7-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="091f7-172">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="091f7-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="091f7-173">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="091f7-173">-Name</span></span>
<span data-ttu-id="091f7-174">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="091f7-174">WebApp Name</span></span>

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

### <span data-ttu-id="091f7-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="091f7-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="091f7-176">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="091f7-176">Net Framework Version</span></span>

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

### <span data-ttu-id="091f7-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="091f7-177">-NumberOfWorkers</span></span>
<span data-ttu-id="091f7-178">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="091f7-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="091f7-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="091f7-179">-PhpVersion</span></span>
<span data-ttu-id="091f7-180">Wersja php</span><span class="sxs-lookup"><span data-stu-id="091f7-180">Php Version</span></span>

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

### <span data-ttu-id="091f7-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="091f7-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="091f7-182">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="091f7-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="091f7-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="091f7-183">-ResourceGroupName</span></span>
<span data-ttu-id="091f7-184">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="091f7-184">Resource Group Name</span></span>

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

### <span data-ttu-id="091f7-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="091f7-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="091f7-186">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="091f7-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="091f7-187">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="091f7-187">-WebApp</span></span>
<span data-ttu-id="091f7-188">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="091f7-188">WebApp Object</span></span>

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

### <span data-ttu-id="091f7-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="091f7-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="091f7-190">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="091f7-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="091f7-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091f7-191">CommonParameters</span></span>
<span data-ttu-id="091f7-192">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="091f7-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091f7-193">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="091f7-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091f7-194">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="091f7-194">INPUTS</span></span>

### <span data-ttu-id="091f7-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="091f7-195">System.Int32</span></span>

### <span data-ttu-id="091f7-196">System. String</span><span class="sxs-lookup"><span data-stu-id="091f7-196">System.String</span></span>

### <span data-ttu-id="091f7-197">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="091f7-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="091f7-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="091f7-198">OUTPUTS</span></span>

### <span data-ttu-id="091f7-199">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="091f7-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="091f7-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="091f7-200">NOTES</span></span>
<span data-ttu-id="091f7-201">Poniższe podane polecenie cmdlet ułatwi zaktualizowanie aplikacji Azure Web App do **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="091f7-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="091f7-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-Propertyobject $PropertiesObject-ResourceGroupName "Default-Web-Westname"-ResourceType Microsoft. Web/Sites/config-resourceName "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="091f7-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="091f7-203">Zamienianie wartości Default-Web-zachód na nazwę grupy zasobów aplikacji i ContosoWebApp z nazwą aplikacji.</span><span class="sxs-lookup"><span data-stu-id="091f7-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="091f7-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="091f7-204">RELATED LINKS</span></span>

[<span data-ttu-id="091f7-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="091f7-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="091f7-206">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="091f7-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="091f7-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="091f7-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="091f7-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="091f7-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="091f7-209">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="091f7-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="091f7-210">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="091f7-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="091f7-211">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="091f7-211">New-AzResource</span></span>](./New-AzResource.md)
