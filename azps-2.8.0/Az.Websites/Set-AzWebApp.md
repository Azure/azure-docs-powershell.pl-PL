---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888065"
---
# <span data-ttu-id="637be-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="637be-101">Set-AzWebApp</span></span>

## <span data-ttu-id="637be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="637be-102">SYNOPSIS</span></span>
<span data-ttu-id="637be-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="637be-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="637be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="637be-104">SYNTAX</span></span>

### <span data-ttu-id="637be-105">S1</span><span class="sxs-lookup"><span data-stu-id="637be-105">S1</span></span>
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
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="637be-106">S2</span><span class="sxs-lookup"><span data-stu-id="637be-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="637be-107">Opis</span><span class="sxs-lookup"><span data-stu-id="637be-107">DESCRIPTION</span></span>
<span data-ttu-id="637be-108">Polecenie cmdlet **Set-AzWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="637be-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="637be-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="637be-109">EXAMPLES</span></span>

### <span data-ttu-id="637be-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="637be-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="637be-111">To polecenie powoduje zmianę planu appService skojarzonego z aplikacją sieci Web ContosoWebApp skojarzoną z domyślną grupą zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="637be-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="637be-112">Użyj tego linku, aby dowiedzieć się więcej o zmienianiu appService planu i ograniczeń z nim skojarzonych.</span><span class="sxs-lookup"><span data-stu-id="637be-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="637be-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="637be-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="637be-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="637be-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="637be-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="637be-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="637be-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="637be-116">PARAMETERS</span></span>

### <span data-ttu-id="637be-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="637be-117">-AppServicePlan</span></span>
<span data-ttu-id="637be-118">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="637be-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="637be-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="637be-119">-AppSettings</span></span>
<span data-ttu-id="637be-120">Ustawienia aplikacji HashTable.</span><span class="sxs-lookup"><span data-stu-id="637be-120">App Settings HashTable.</span></span> <span data-ttu-id="637be-121">Istniejące ustawienia aplikacji zostaną zastąpione, co spowoduje usunięcie wszystkich ustawień, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="637be-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="637be-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="637be-122">-AsJob</span></span>
<span data-ttu-id="637be-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="637be-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="637be-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="637be-124">-AssignIdentity</span></span>
<span data-ttu-id="637be-125">Włączanie/wyłączanie Instalatora MSI na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="637be-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="637be-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="637be-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="637be-127">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="637be-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="637be-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="637be-128">-AzureStoragePath</span></span>
<span data-ttu-id="637be-129">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="637be-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="637be-130">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="637be-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="637be-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="637be-131">-ConnectionStrings</span></span>
<span data-ttu-id="637be-132">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="637be-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="637be-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="637be-133">-ContainerImageName</span></span>
<span data-ttu-id="637be-134">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="637be-134">Container Image Name</span></span>

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

### <span data-ttu-id="637be-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="637be-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="637be-136">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="637be-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="637be-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="637be-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="637be-138">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="637be-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="637be-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="637be-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="637be-140">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="637be-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="637be-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="637be-141">-DefaultDocuments</span></span>
<span data-ttu-id="637be-142">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="637be-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="637be-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637be-143">-DefaultProfile</span></span>
<span data-ttu-id="637be-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="637be-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="637be-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="637be-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="637be-146">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="637be-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="637be-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="637be-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="637be-148">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="637be-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="637be-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="637be-149">-HandlerMappings</span></span>
<span data-ttu-id="637be-150">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="637be-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="637be-151">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="637be-151">-HostNames</span></span>
<span data-ttu-id="637be-152">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="637be-152">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="637be-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="637be-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="637be-154">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="637be-154">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="637be-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="637be-155">-HttpsOnly</span></span>
<span data-ttu-id="637be-156">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="637be-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="637be-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="637be-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="637be-158">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="637be-158">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="637be-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="637be-159">-Name</span></span>
<span data-ttu-id="637be-160">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="637be-160">WebApp Name</span></span>

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

### <span data-ttu-id="637be-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="637be-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="637be-162">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="637be-162">Net Framework Version</span></span>

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

### <span data-ttu-id="637be-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="637be-163">-NumberOfWorkers</span></span>
<span data-ttu-id="637be-164">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="637be-164">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="637be-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="637be-165">-PhpVersion</span></span>
<span data-ttu-id="637be-166">Wersja php</span><span class="sxs-lookup"><span data-stu-id="637be-166">Php Version</span></span>

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

### <span data-ttu-id="637be-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="637be-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="637be-168">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="637be-168">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="637be-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="637be-169">-ResourceGroupName</span></span>
<span data-ttu-id="637be-170">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="637be-170">Resource Group Name</span></span>

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

### <span data-ttu-id="637be-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="637be-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="637be-172">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="637be-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="637be-173">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="637be-173">-WebApp</span></span>
<span data-ttu-id="637be-174">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="637be-174">WebApp Object</span></span>

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

### <span data-ttu-id="637be-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="637be-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="637be-176">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="637be-176">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="637be-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637be-177">CommonParameters</span></span>
<span data-ttu-id="637be-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="637be-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637be-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="637be-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637be-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="637be-180">INPUTS</span></span>

### <span data-ttu-id="637be-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="637be-181">System.Int32</span></span>

### <span data-ttu-id="637be-182">System. String</span><span class="sxs-lookup"><span data-stu-id="637be-182">System.String</span></span>

### <span data-ttu-id="637be-183">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="637be-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="637be-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="637be-184">OUTPUTS</span></span>

### <span data-ttu-id="637be-185">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="637be-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="637be-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="637be-186">NOTES</span></span>

## <span data-ttu-id="637be-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="637be-187">RELATED LINKS</span></span>

[<span data-ttu-id="637be-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="637be-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="637be-189">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="637be-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="637be-190">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="637be-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="637be-191">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="637be-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="637be-192">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="637be-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="637be-193">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="637be-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
