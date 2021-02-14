---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197227"
---
# <span data-ttu-id="03c2e-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-101">Set-AzWebApp</span></span>

## <span data-ttu-id="03c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="03c2e-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="03c2e-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="03c2e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03c2e-104">SYNTAX</span></span>

### <span data-ttu-id="03c2e-105">S1</span><span class="sxs-lookup"><span data-stu-id="03c2e-105">S1</span></span>
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

### <span data-ttu-id="03c2e-106">S2</span><span class="sxs-lookup"><span data-stu-id="03c2e-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03c2e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="03c2e-107">DESCRIPTION</span></span>
<span data-ttu-id="03c2e-108">Polecenie **cmdlet Set-AzWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="03c2e-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="03c2e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03c2e-109">EXAMPLES</span></span>

### <span data-ttu-id="03c2e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03c2e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="03c2e-111">To polecenie zmienia plan usługi aplikacji skojarzony z aplikacją Web App ContosoWebApp skojarzoną z grupą zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="03c2e-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="03c2e-112">Skorzystaj z tego linku, aby dowiedzieć się więcej na temat zmieniania planu usługi aplikacji i skojarzonych z nim ograniczeń.</span><span class="sxs-lookup"><span data-stu-id="03c2e-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="03c2e-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="03c2e-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="03c2e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="03c2e-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="03c2e-115">To polecenie ustawia wartość HttpLoggingEnabled na prawda dla aplikacji Web App ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="03c2e-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="03c2e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="03c2e-116">Example 3</span></span>

<span data-ttu-id="03c2e-117">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="03c2e-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="03c2e-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="03c2e-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="03c2e-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="03c2e-119">Example 4</span></span>

<span data-ttu-id="03c2e-120">Poniższy przykład tworzy ciąg połączenia o nazwie myConnectionString for Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="03c2e-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="03c2e-121">To zastąpi wszystkie istniejące parametry połączenia dla aplikacji Sieci Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="03c2e-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="03c2e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c2e-122">PARAMETERS</span></span>

### <span data-ttu-id="03c2e-123">- AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="03c2e-123">-AlwaysOn</span></span>
<span data-ttu-id="03c2e-124">Upewnij się, że aplikacja sieci Web jest ładowana cały czas, a nie zwolniona po czasie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="03c2e-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="03c2e-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="03c2e-125">-AppServicePlan</span></span>
<span data-ttu-id="03c2e-126">Nazwa planu serwisowego aplikacji</span><span class="sxs-lookup"><span data-stu-id="03c2e-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="03c2e-127">- AppSettings</span><span class="sxs-lookup"><span data-stu-id="03c2e-127">-AppSettings</span></span>
<span data-ttu-id="03c2e-128">Tabela skrótów ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03c2e-128">App Settings HashTable.</span></span> <span data-ttu-id="03c2e-129">Istniejące ustawienia aplikacji zostaną zastąpione, usuwając wszelkie ustawienia, które nie są dostępne.</span><span class="sxs-lookup"><span data-stu-id="03c2e-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="03c2e-130">— AsJob</span><span class="sxs-lookup"><span data-stu-id="03c2e-130">-AsJob</span></span>
<span data-ttu-id="03c2e-131">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03c2e-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03c2e-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="03c2e-132">-AssignIdentity</span></span>
<span data-ttu-id="03c2e-133">Włączanie/wyłączanie msi w istniejącej aplikacji Azure WebApp lub functionapp</span><span class="sxs-lookup"><span data-stu-id="03c2e-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="03c2e-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="03c2e-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="03c2e-135">Nazwa miejsca docelowego dla automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="03c2e-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="03c2e-136">— AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="03c2e-136">-AzureStoragePath</span></span>
<span data-ttu-id="03c2e-137">Magazyn platformy Azure do montażu wewnątrz aplikacji sieci Web na kontener.</span><span class="sxs-lookup"><span data-stu-id="03c2e-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="03c2e-138">Tworzenie New-AzureRmWebAppAzureStoragePath za pomocą aplikacji</span><span class="sxs-lookup"><span data-stu-id="03c2e-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="03c2e-139">- ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="03c2e-139">-ConnectionStrings</span></span>
<span data-ttu-id="03c2e-140">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="03c2e-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="03c2e-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="03c2e-141">-ContainerImageName</span></span>
<span data-ttu-id="03c2e-142">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="03c2e-142">Container Image Name</span></span>

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

### <span data-ttu-id="03c2e-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="03c2e-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="03c2e-144">Hasło do rejestru dla kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="03c2e-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="03c2e-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="03c2e-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="03c2e-146">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="03c2e-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="03c2e-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="03c2e-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="03c2e-148">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="03c2e-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="03c2e-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="03c2e-149">-DefaultDocuments</span></span>
<span data-ttu-id="03c2e-150">Domyślna tablica ciągów dokumentów</span><span class="sxs-lookup"><span data-stu-id="03c2e-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="03c2e-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c2e-151">-DefaultProfile</span></span>
<span data-ttu-id="03c2e-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03c2e-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03c2e-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="03c2e-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="03c2e-154">Szczegółowa funkcja rejestrowania błędów włączona wartość logiczna</span><span class="sxs-lookup"><span data-stu-id="03c2e-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="03c2e-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="03c2e-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="03c2e-156">Włączenie/wyłączenie kontenera ciągłego wdrożenia sieci Web</span><span class="sxs-lookup"><span data-stu-id="03c2e-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="03c2e-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="03c2e-157">-FtpsState</span></span>
<span data-ttu-id="03c2e-158">Ustaw wartość stanu Ftps dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03c2e-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="03c2e-159">Dozwolone wartości [Wszystkiewszystkie | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="03c2e-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="03c2e-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="03c2e-160">-HandlerMappings</span></span>
<span data-ttu-id="03c2e-161">Lista IList mapowań obsługi</span><span class="sxs-lookup"><span data-stu-id="03c2e-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="03c2e-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="03c2e-162">-HostNames</span></span>
<span data-ttu-id="03c2e-163">Tablica ciągów nazw hostów aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="03c2e-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="03c2e-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="03c2e-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="03c2e-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="03c2e-166">—httpsOnly</span><span class="sxs-lookup"><span data-stu-id="03c2e-166">-HttpsOnly</span></span>
<span data-ttu-id="03c2e-167">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącej aplikacji Azure WebApp lub FunctionApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="03c2e-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="03c2e-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="03c2e-169">Nazwa trybu zarządzanego potoku</span><span class="sxs-lookup"><span data-stu-id="03c2e-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="03c2e-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="03c2e-170">-MinTlsVersion</span></span>
<span data-ttu-id="03c2e-171">Minimalna wersja protokołu TLS wymagana dla żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="03c2e-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="03c2e-172">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="03c2e-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="03c2e-173">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03c2e-173">-Name</span></span>
<span data-ttu-id="03c2e-174">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-174">WebApp Name</span></span>

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

### <span data-ttu-id="03c2e-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="03c2e-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="03c2e-176">Wersja programu Net Framework</span><span class="sxs-lookup"><span data-stu-id="03c2e-176">Net Framework Version</span></span>

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

### <span data-ttu-id="03c2e-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="03c2e-177">-NumberOfWorkers</span></span>
<span data-ttu-id="03c2e-178">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="03c2e-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="03c2e-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="03c2e-179">-PhpVersion</span></span>
<span data-ttu-id="03c2e-180">Wersja Php</span><span class="sxs-lookup"><span data-stu-id="03c2e-180">Php Version</span></span>

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

### <span data-ttu-id="03c2e-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="03c2e-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="03c2e-182">Włączone śledzenie żądania</span><span class="sxs-lookup"><span data-stu-id="03c2e-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="03c2e-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c2e-183">-ResourceGroupName</span></span>
<span data-ttu-id="03c2e-184">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="03c2e-184">Resource Group Name</span></span>

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

### <span data-ttu-id="03c2e-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="03c2e-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="03c2e-186">Użyj wartości logicznych 32-bitowej procesów roboczych</span><span class="sxs-lookup"><span data-stu-id="03c2e-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="03c2e-187">- WebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-187">-WebApp</span></span>
<span data-ttu-id="03c2e-188">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-188">WebApp Object</span></span>

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

### <span data-ttu-id="03c2e-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="03c2e-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="03c2e-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="03c2e-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="03c2e-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c2e-191">CommonParameters</span></span>
<span data-ttu-id="03c2e-192">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c2e-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c2e-193">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c2e-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c2e-194">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03c2e-194">INPUTS</span></span>

### <span data-ttu-id="03c2e-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="03c2e-195">System.Int32</span></span>

### <span data-ttu-id="03c2e-196">System.String</span><span class="sxs-lookup"><span data-stu-id="03c2e-196">System.String</span></span>

### <span data-ttu-id="03c2e-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="03c2e-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="03c2e-198">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03c2e-198">OUTPUTS</span></span>

### <span data-ttu-id="03c2e-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="03c2e-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="03c2e-200">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03c2e-200">NOTES</span></span>
<span data-ttu-id="03c2e-201">Poniższe polecenie cmdlet pomoże zaktualizować usługę Azure Web App do **dotnetcore**</span><span class="sxs-lookup"><span data-stu-id="03c2e-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="03c2e-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="03c2e-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="03c2e-203">Zamień wartości Default-Web-WestUS na nazwę grupy zasobów webapp i contosowebapp na nazwę webapp.</span><span class="sxs-lookup"><span data-stu-id="03c2e-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="03c2e-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03c2e-204">RELATED LINKS</span></span>

[<span data-ttu-id="03c2e-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="03c2e-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="03c2e-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="03c2e-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="03c2e-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="03c2e-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03c2e-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="03c2e-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="03c2e-211">New-AzResource</span></span>](./New-AzResource.md)
