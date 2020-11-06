---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546292"
---
# <span data-ttu-id="80713-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80713-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="80713-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80713-102">SYNOPSIS</span></span>
<span data-ttu-id="80713-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="80713-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80713-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80713-104">SYNTAX</span></span>

### <span data-ttu-id="80713-105">S1</span><span class="sxs-lookup"><span data-stu-id="80713-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80713-106">S2</span><span class="sxs-lookup"><span data-stu-id="80713-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80713-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80713-107">DESCRIPTION</span></span>
<span data-ttu-id="80713-108">Polecenie cmdlet **Set-AzureRmWebApp** ustawia miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="80713-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="80713-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80713-109">EXAMPLES</span></span>

### <span data-ttu-id="80713-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80713-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="80713-111">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla Slot001 gniazda odnoszącego się do aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="80713-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="80713-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80713-112">PARAMETERS</span></span>

### <span data-ttu-id="80713-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="80713-113">-AppServicePlan</span></span>
<span data-ttu-id="80713-114">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="80713-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="80713-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="80713-115">-AppSettings</span></span>
<span data-ttu-id="80713-116">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="80713-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="80713-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80713-117">-AsJob</span></span>
<span data-ttu-id="80713-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="80713-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80713-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="80713-119">-AssignIdentity</span></span>
<span data-ttu-id="80713-120">Włączanie/wyłączanie MSI w istniejącym gnieździe [Podgląd]</span><span class="sxs-lookup"><span data-stu-id="80713-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="80713-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="80713-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="80713-122">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="80713-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="80713-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="80713-123">-ConnectionStrings</span></span>
<span data-ttu-id="80713-124">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="80713-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="80713-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="80713-125">-ContainerImageName</span></span>
<span data-ttu-id="80713-126">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="80713-126">Container Image Name</span></span>

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

### <span data-ttu-id="80713-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="80713-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="80713-128">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="80713-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="80713-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="80713-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="80713-130">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="80713-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="80713-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="80713-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="80713-132">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="80713-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="80713-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="80713-133">-DefaultDocuments</span></span>
<span data-ttu-id="80713-134">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="80713-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="80713-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80713-135">-DefaultProfile</span></span>
<span data-ttu-id="80713-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80713-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80713-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="80713-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="80713-138">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="80713-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="80713-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="80713-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="80713-140">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="80713-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="80713-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="80713-141">-HandlerMappings</span></span>
<span data-ttu-id="80713-142">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="80713-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="80713-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="80713-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="80713-144">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="80713-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="80713-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="80713-145">-HttpsOnly</span></span>
<span data-ttu-id="80713-146">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącym gnieździe</span><span class="sxs-lookup"><span data-stu-id="80713-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="80713-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="80713-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="80713-148">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="80713-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="80713-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80713-149">-Name</span></span>
<span data-ttu-id="80713-150">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="80713-150">WebApp Name</span></span>

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

### <span data-ttu-id="80713-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="80713-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="80713-152">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="80713-152">Net Framework Version</span></span>

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

### <span data-ttu-id="80713-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="80713-153">-NumberOfWorkers</span></span>
<span data-ttu-id="80713-154">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="80713-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="80713-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="80713-155">-PhpVersion</span></span>
<span data-ttu-id="80713-156">Wersja php</span><span class="sxs-lookup"><span data-stu-id="80713-156">Php Version</span></span>

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

### <span data-ttu-id="80713-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="80713-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="80713-158">Wartość logiczna włączonego śledzenia żądań</span><span class="sxs-lookup"><span data-stu-id="80713-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="80713-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80713-159">-ResourceGroupName</span></span>
<span data-ttu-id="80713-160">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="80713-160">Resource Group Name</span></span>

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

### <span data-ttu-id="80713-161">-Slot</span><span class="sxs-lookup"><span data-stu-id="80713-161">-Slot</span></span>
<span data-ttu-id="80713-162">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="80713-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="80713-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="80713-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="80713-164">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="80713-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="80713-165">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="80713-165">-WebApp</span></span>
<span data-ttu-id="80713-166">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="80713-166">WebApp Object</span></span>

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

### <span data-ttu-id="80713-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="80713-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="80713-168">Wartość logiczna z włączonymi gniazdami sieci Web</span><span class="sxs-lookup"><span data-stu-id="80713-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="80713-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80713-169">CommonParameters</span></span>
<span data-ttu-id="80713-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80713-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80713-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80713-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80713-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80713-172">INPUTS</span></span>

### <span data-ttu-id="80713-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="80713-173">System.Int32</span></span>
<span data-ttu-id="80713-174">Parametry: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80713-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="80713-175">System. String</span><span class="sxs-lookup"><span data-stu-id="80713-175">System.String</span></span>

### <span data-ttu-id="80713-176">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="80713-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="80713-177">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80713-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="80713-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80713-178">OUTPUTS</span></span>

### <span data-ttu-id="80713-179">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="80713-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="80713-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80713-180">NOTES</span></span>

## <span data-ttu-id="80713-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80713-181">RELATED LINKS</span></span>

[<span data-ttu-id="80713-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80713-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="80713-183">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80713-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="80713-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80713-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="80713-185">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80713-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="80713-186">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80713-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="80713-187">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80713-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="80713-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="80713-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
