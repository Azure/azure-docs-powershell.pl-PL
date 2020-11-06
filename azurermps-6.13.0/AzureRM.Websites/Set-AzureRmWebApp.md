---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544724"
---
# <span data-ttu-id="fd11e-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fd11e-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="fd11e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd11e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd11e-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fd11e-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd11e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd11e-104">SYNTAX</span></span>

### <span data-ttu-id="fd11e-105">S1</span><span class="sxs-lookup"><span data-stu-id="fd11e-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd11e-106">S2</span><span class="sxs-lookup"><span data-stu-id="fd11e-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd11e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fd11e-107">DESCRIPTION</span></span>
<span data-ttu-id="fd11e-108">Polecenie cmdlet **Set-AzureRmWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fd11e-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="fd11e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd11e-109">EXAMPLES</span></span>

### <span data-ttu-id="fd11e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd11e-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="fd11e-111">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="fd11e-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="fd11e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd11e-112">PARAMETERS</span></span>

### <span data-ttu-id="fd11e-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fd11e-113">-AppServicePlan</span></span>
<span data-ttu-id="fd11e-114">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="fd11e-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="fd11e-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="fd11e-115">-AppSettings</span></span>
<span data-ttu-id="fd11e-116">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd11e-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="fd11e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd11e-117">-AsJob</span></span>
<span data-ttu-id="fd11e-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fd11e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd11e-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fd11e-119">-AssignIdentity</span></span>
<span data-ttu-id="fd11e-120">Włączanie/wyłączanie Instalatora MSI na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="fd11e-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="fd11e-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="fd11e-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="fd11e-122">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="fd11e-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="fd11e-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="fd11e-123">-ConnectionStrings</span></span>
<span data-ttu-id="fd11e-124">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="fd11e-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="fd11e-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="fd11e-125">-ContainerImageName</span></span>
<span data-ttu-id="fd11e-126">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="fd11e-126">Container Image Name</span></span>

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

### <span data-ttu-id="fd11e-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="fd11e-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="fd11e-128">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="fd11e-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="fd11e-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="fd11e-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="fd11e-130">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="fd11e-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="fd11e-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="fd11e-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="fd11e-132">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="fd11e-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="fd11e-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="fd11e-133">-DefaultDocuments</span></span>
<span data-ttu-id="fd11e-134">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="fd11e-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="fd11e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd11e-135">-DefaultProfile</span></span>
<span data-ttu-id="fd11e-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd11e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd11e-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fd11e-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="fd11e-138">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="fd11e-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="fd11e-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="fd11e-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="fd11e-140">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="fd11e-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="fd11e-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="fd11e-141">-HandlerMappings</span></span>
<span data-ttu-id="fd11e-142">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="fd11e-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="fd11e-143">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="fd11e-143">-HostNames</span></span>
<span data-ttu-id="fd11e-144">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd11e-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="fd11e-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fd11e-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="fd11e-146">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fd11e-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="fd11e-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fd11e-147">-HttpsOnly</span></span>
<span data-ttu-id="fd11e-148">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="fd11e-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="fd11e-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="fd11e-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="fd11e-150">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="fd11e-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="fd11e-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd11e-151">-Name</span></span>
<span data-ttu-id="fd11e-152">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd11e-152">WebApp Name</span></span>

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

### <span data-ttu-id="fd11e-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="fd11e-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="fd11e-154">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="fd11e-154">Net Framework Version</span></span>

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

### <span data-ttu-id="fd11e-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="fd11e-155">-NumberOfWorkers</span></span>
<span data-ttu-id="fd11e-156">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="fd11e-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="fd11e-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="fd11e-157">-PhpVersion</span></span>
<span data-ttu-id="fd11e-158">Wersja php</span><span class="sxs-lookup"><span data-stu-id="fd11e-158">Php Version</span></span>

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

### <span data-ttu-id="fd11e-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="fd11e-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="fd11e-160">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="fd11e-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="fd11e-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd11e-161">-ResourceGroupName</span></span>
<span data-ttu-id="fd11e-162">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fd11e-162">Resource Group Name</span></span>

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

### <span data-ttu-id="fd11e-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="fd11e-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="fd11e-164">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="fd11e-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="fd11e-165">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd11e-165">-WebApp</span></span>
<span data-ttu-id="fd11e-166">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd11e-166">WebApp Object</span></span>

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

### <span data-ttu-id="fd11e-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="fd11e-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="fd11e-168">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="fd11e-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="fd11e-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd11e-169">CommonParameters</span></span>
<span data-ttu-id="fd11e-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd11e-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd11e-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd11e-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd11e-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd11e-172">INPUTS</span></span>

### <span data-ttu-id="fd11e-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fd11e-173">System.Int32</span></span>
<span data-ttu-id="fd11e-174">Parametry: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd11e-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="fd11e-175">System. String</span><span class="sxs-lookup"><span data-stu-id="fd11e-175">System.String</span></span>

### <span data-ttu-id="fd11e-176">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="fd11e-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="fd11e-177">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd11e-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="fd11e-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd11e-178">OUTPUTS</span></span>

### <span data-ttu-id="fd11e-179">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="fd11e-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="fd11e-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd11e-180">NOTES</span></span>

## <span data-ttu-id="fd11e-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd11e-181">RELATED LINKS</span></span>

[<span data-ttu-id="fd11e-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fd11e-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="fd11e-183">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fd11e-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="fd11e-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fd11e-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="fd11e-185">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fd11e-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="fd11e-186">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fd11e-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="fd11e-187">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fd11e-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
