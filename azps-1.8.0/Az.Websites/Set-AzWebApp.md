---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707264"
---
# <span data-ttu-id="d6f60-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6f60-101">Set-AzWebApp</span></span>



## <span data-ttu-id="d6f60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6f60-102">SYNOPSIS</span></span>

<span data-ttu-id="d6f60-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d6f60-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="d6f60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6f60-104">SYNTAX</span></span>



### <span data-ttu-id="d6f60-105">S1</span><span class="sxs-lookup"><span data-stu-id="d6f60-105">S1</span></span>

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



### <span data-ttu-id="d6f60-106">S2</span><span class="sxs-lookup"><span data-stu-id="d6f60-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="d6f60-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6f60-107">DESCRIPTION</span></span>

<span data-ttu-id="d6f60-108">Polecenie cmdlet **Set-AzWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d6f60-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="d6f60-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6f60-109">EXAMPLES</span></span>



### <span data-ttu-id="d6f60-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6f60-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="d6f60-111">To polecenie powoduje zmianę planu appService skojarzonego z aplikacją sieci Web ContosoWebApp skojarzoną z domyślną grupą zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d6f60-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d6f60-112">Użyj tego linku, aby learm więcej informacji na temat zmieniania planu appService i powiązanych z nim ograniczeń.</span><span class="sxs-lookup"><span data-stu-id="d6f60-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="d6f60-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d6f60-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="d6f60-114">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="d6f60-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="d6f60-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6f60-115">PARAMETERS</span></span>



### <span data-ttu-id="d6f60-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d6f60-116">-AppServicePlan</span></span>

<span data-ttu-id="d6f60-117">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="d6f60-117">App Service Plan Name</span></span>



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



### <span data-ttu-id="d6f60-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d6f60-118">-AppSettings</span></span>

<span data-ttu-id="d6f60-119">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="d6f60-119">App Settings HashTable</span></span>



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



### <span data-ttu-id="d6f60-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f60-120">-AsJob</span></span>

<span data-ttu-id="d6f60-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d6f60-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="d6f60-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d6f60-122">-AssignIdentity</span></span>

<span data-ttu-id="d6f60-123">Włączanie/wyłączanie Instalatora MSI na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="d6f60-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="d6f60-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d6f60-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="d6f60-125">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="d6f60-125">Destination slot name for auto swap</span></span>



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



### <span data-ttu-id="d6f60-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="d6f60-126">-AzureStoragePath</span></span>

<span data-ttu-id="d6f60-127">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6f60-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="d6f60-128">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="d6f60-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



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



### <span data-ttu-id="d6f60-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="d6f60-129">-ConnectionStrings</span></span>

<span data-ttu-id="d6f60-130">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="d6f60-130">Connection Strings HashTable</span></span>



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



### <span data-ttu-id="d6f60-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="d6f60-131">-ContainerImageName</span></span>

<span data-ttu-id="d6f60-132">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="d6f60-132">Container Image Name</span></span>



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



### <span data-ttu-id="d6f60-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="d6f60-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="d6f60-134">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="d6f60-134">Private Container Registry Password</span></span>



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



### <span data-ttu-id="d6f60-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="d6f60-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="d6f60-136">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="d6f60-136">Private Container Registry Server Url</span></span>



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



### <span data-ttu-id="d6f60-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="d6f60-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="d6f60-138">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="d6f60-138">Private Container Registry Username</span></span>



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



### <span data-ttu-id="d6f60-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="d6f60-139">-DefaultDocuments</span></span>

<span data-ttu-id="d6f60-140">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="d6f60-140">Default Documents String Array</span></span>



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



### <span data-ttu-id="d6f60-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f60-141">-DefaultProfile</span></span>

<span data-ttu-id="d6f60-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f60-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="d6f60-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d6f60-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="d6f60-144">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="d6f60-144">Detailed Error Logging Enabled Boolean</span></span>



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



### <span data-ttu-id="d6f60-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="d6f60-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="d6f60-146">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="d6f60-146">Enables/Disables container continuous deployment webhook</span></span>



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



### <span data-ttu-id="d6f60-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d6f60-147">-HandlerMappings</span></span>

<span data-ttu-id="d6f60-148">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="d6f60-148">Handler Mappings IList</span></span>



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



### <span data-ttu-id="d6f60-149">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="d6f60-149">-HostNames</span></span>

<span data-ttu-id="d6f60-150">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="d6f60-150">WebApp HostNames String Array</span></span>



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



### <span data-ttu-id="d6f60-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d6f60-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="d6f60-152">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d6f60-152">HttpLoggingEnabled Boolean</span></span>



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



### <span data-ttu-id="d6f60-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d6f60-153">-HttpsOnly</span></span>

<span data-ttu-id="d6f60-154">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="d6f60-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="d6f60-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d6f60-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="d6f60-156">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="d6f60-156">Managed Pipeline Mode Name</span></span>



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



### <span data-ttu-id="d6f60-157">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6f60-157">-Name</span></span>

<span data-ttu-id="d6f60-158">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="d6f60-158">WebApp Name</span></span>



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



### <span data-ttu-id="d6f60-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d6f60-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="d6f60-160">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="d6f60-160">Net Framework Version</span></span>



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



### <span data-ttu-id="d6f60-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="d6f60-161">-NumberOfWorkers</span></span>

<span data-ttu-id="d6f60-162">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="d6f60-162">The number of workers to be allocated</span></span>



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



### <span data-ttu-id="d6f60-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d6f60-163">-PhpVersion</span></span>

<span data-ttu-id="d6f60-164">Wersja php</span><span class="sxs-lookup"><span data-stu-id="d6f60-164">Php Version</span></span>



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



### <span data-ttu-id="d6f60-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d6f60-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="d6f60-166">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="d6f60-166">Request Tracing Enabled</span></span>



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



### <span data-ttu-id="d6f60-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f60-167">-ResourceGroupName</span></span>

<span data-ttu-id="d6f60-168">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d6f60-168">Resource Group Name</span></span>



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



### <span data-ttu-id="d6f60-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d6f60-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="d6f60-170">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="d6f60-170">Use 32-bit Worker Process Boolean</span></span>



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



### <span data-ttu-id="d6f60-171">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="d6f60-171">-WebApp</span></span>

<span data-ttu-id="d6f60-172">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="d6f60-172">WebApp Object</span></span>



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



### <span data-ttu-id="d6f60-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d6f60-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="d6f60-174">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d6f60-174">WebSocketsEnabled Boolean</span></span>



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



### <span data-ttu-id="d6f60-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f60-175">CommonParameters</span></span>

<span data-ttu-id="d6f60-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f60-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f60-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f60-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="d6f60-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f60-178">INPUTS</span></span>



### <span data-ttu-id="d6f60-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d6f60-179">System.Int32</span></span>



### <span data-ttu-id="d6f60-180">System. String</span><span class="sxs-lookup"><span data-stu-id="d6f60-180">System.String</span></span>



### <span data-ttu-id="d6f60-181">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="d6f60-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="d6f60-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6f60-182">OUTPUTS</span></span>



### <span data-ttu-id="d6f60-183">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="d6f60-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="d6f60-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6f60-184">NOTES</span></span>



## <span data-ttu-id="d6f60-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6f60-185">RELATED LINKS</span></span>



[<span data-ttu-id="d6f60-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6f60-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="d6f60-187">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6f60-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="d6f60-188">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6f60-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="d6f60-189">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6f60-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="d6f60-190">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6f60-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="d6f60-191">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6f60-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

