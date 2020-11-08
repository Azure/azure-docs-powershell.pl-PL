---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233888"
---
# <span data-ttu-id="43564-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43564-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="43564-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43564-102">SYNOPSIS</span></span>
<span data-ttu-id="43564-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="43564-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="43564-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43564-104">SYNTAX</span></span>

### <span data-ttu-id="43564-105">S1</span><span class="sxs-lookup"><span data-stu-id="43564-105">S1</span></span>
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

### <span data-ttu-id="43564-106">S2</span><span class="sxs-lookup"><span data-stu-id="43564-106">S2</span></span>
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

## <span data-ttu-id="43564-107">Opis</span><span class="sxs-lookup"><span data-stu-id="43564-107">DESCRIPTION</span></span>
<span data-ttu-id="43564-108">Polecenie cmdlet **Set-AzWebApp** ustawia miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="43564-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="43564-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43564-109">EXAMPLES</span></span>

### <span data-ttu-id="43564-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43564-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="43564-111">To polecenie powoduje zmianę planu appService skojarzonego z Slot001 na karcie aplikacji ContosoWebApp powiązanej z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="43564-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="43564-112">Użyj tego linku, aby dowiedzieć się więcej o zmienianiu appService planu i ograniczeń z nim skojarzonych.</span><span class="sxs-lookup"><span data-stu-id="43564-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="43564-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="43564-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="43564-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="43564-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="43564-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla Slot001 gniazda odnoszącego się do aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="43564-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="43564-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="43564-116">Example 3</span></span>

<span data-ttu-id="43564-117">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="43564-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="43564-118">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="43564-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="43564-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43564-119">PARAMETERS</span></span>

### <span data-ttu-id="43564-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="43564-120">-AlwaysOn</span></span>
<span data-ttu-id="43564-121">Upewnij się, że aplikacja internetowa jest ładowana przez cały czas, a nie rozładowana po okresie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="43564-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="43564-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43564-122">-AppServicePlan</span></span>
<span data-ttu-id="43564-123">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="43564-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="43564-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="43564-124">-AppSettings</span></span>
<span data-ttu-id="43564-125">Ustawienia aplikacji HashTable.</span><span class="sxs-lookup"><span data-stu-id="43564-125">App Settings HashTable.</span></span> <span data-ttu-id="43564-126">Istniejące ustawienia aplikacji zostaną zastąpione, co spowoduje usunięcie wszystkich ustawień, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="43564-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="43564-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43564-127">-AsJob</span></span>
<span data-ttu-id="43564-128">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="43564-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43564-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="43564-129">-AssignIdentity</span></span>
<span data-ttu-id="43564-130">Włączanie/wyłączanie MSI w istniejącym gnieździe [Podgląd]</span><span class="sxs-lookup"><span data-stu-id="43564-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="43564-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="43564-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="43564-132">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="43564-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="43564-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="43564-133">-AzureStoragePath</span></span>
<span data-ttu-id="43564-134">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="43564-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="43564-135">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="43564-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="43564-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="43564-136">-ConnectionStrings</span></span>
<span data-ttu-id="43564-137">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="43564-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="43564-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="43564-138">-ContainerImageName</span></span>
<span data-ttu-id="43564-139">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="43564-139">Container Image Name</span></span>

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

### <span data-ttu-id="43564-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="43564-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="43564-141">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="43564-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="43564-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="43564-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="43564-143">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="43564-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="43564-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="43564-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="43564-145">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="43564-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="43564-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="43564-146">-DefaultDocuments</span></span>
<span data-ttu-id="43564-147">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="43564-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="43564-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43564-148">-DefaultProfile</span></span>
<span data-ttu-id="43564-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43564-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43564-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="43564-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="43564-151">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="43564-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="43564-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="43564-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="43564-153">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="43564-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="43564-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="43564-154">-FtpsState</span></span>
<span data-ttu-id="43564-155">Ustaw wartość stanu FTPS dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="43564-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="43564-156">Dozwolone wartości [AllAllowed | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="43564-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="43564-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="43564-157">-HandlerMappings</span></span>
<span data-ttu-id="43564-158">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="43564-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="43564-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="43564-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="43564-160">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="43564-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="43564-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="43564-161">-HttpsOnly</span></span>
<span data-ttu-id="43564-162">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącym gnieździe</span><span class="sxs-lookup"><span data-stu-id="43564-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="43564-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="43564-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="43564-164">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="43564-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="43564-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="43564-165">-MinTlsVersion</span></span>
<span data-ttu-id="43564-166">Minimalna wersja protokołu TLS wymagana w przypadku żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="43564-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="43564-167">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="43564-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="43564-168">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43564-168">-Name</span></span>
<span data-ttu-id="43564-169">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="43564-169">WebApp Name</span></span>

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

### <span data-ttu-id="43564-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="43564-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="43564-171">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="43564-171">Net Framework Version</span></span>

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

### <span data-ttu-id="43564-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="43564-172">-NumberOfWorkers</span></span>
<span data-ttu-id="43564-173">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="43564-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="43564-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="43564-174">-PhpVersion</span></span>
<span data-ttu-id="43564-175">Wersja php</span><span class="sxs-lookup"><span data-stu-id="43564-175">Php Version</span></span>

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

### <span data-ttu-id="43564-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="43564-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="43564-177">Wartość logiczna włączonego śledzenia żądań</span><span class="sxs-lookup"><span data-stu-id="43564-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="43564-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43564-178">-ResourceGroupName</span></span>
<span data-ttu-id="43564-179">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="43564-179">Resource Group Name</span></span>

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

### <span data-ttu-id="43564-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="43564-180">-Slot</span></span>
<span data-ttu-id="43564-181">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="43564-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="43564-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="43564-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="43564-183">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="43564-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="43564-184">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="43564-184">-WebApp</span></span>
<span data-ttu-id="43564-185">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="43564-185">WebApp Object</span></span>

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

### <span data-ttu-id="43564-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="43564-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="43564-187">Wartość logiczna z włączonymi gniazdami sieci Web</span><span class="sxs-lookup"><span data-stu-id="43564-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="43564-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43564-188">CommonParameters</span></span>
<span data-ttu-id="43564-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43564-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43564-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43564-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43564-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43564-191">INPUTS</span></span>

### <span data-ttu-id="43564-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="43564-192">System.Int32</span></span>

### <span data-ttu-id="43564-193">System. String</span><span class="sxs-lookup"><span data-stu-id="43564-193">System.String</span></span>

### <span data-ttu-id="43564-194">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="43564-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="43564-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43564-195">OUTPUTS</span></span>

### <span data-ttu-id="43564-196">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="43564-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="43564-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43564-197">NOTES</span></span>

## <span data-ttu-id="43564-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43564-198">RELATED LINKS</span></span>

[<span data-ttu-id="43564-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43564-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="43564-200">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43564-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="43564-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43564-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="43564-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43564-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="43564-203">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43564-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="43564-204">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43564-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="43564-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43564-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
