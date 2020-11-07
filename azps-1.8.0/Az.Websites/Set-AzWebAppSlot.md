---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707259"
---
# <span data-ttu-id="23392-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23392-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="23392-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23392-102">SYNOPSIS</span></span>
<span data-ttu-id="23392-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="23392-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="23392-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23392-104">SYNTAX</span></span>

### <span data-ttu-id="23392-105">S1</span><span class="sxs-lookup"><span data-stu-id="23392-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23392-106">S2</span><span class="sxs-lookup"><span data-stu-id="23392-106">S2</span></span>
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

## <span data-ttu-id="23392-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23392-107">DESCRIPTION</span></span>
<span data-ttu-id="23392-108">Polecenie cmdlet **Set-AzWebApp** ustawia miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="23392-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="23392-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23392-109">EXAMPLES</span></span>

### <span data-ttu-id="23392-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23392-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="23392-111">To polecenie powoduje zmianę planu appService skojarzonego z Slot001 na karcie aplikacji ContosoWebApp powiązanej z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="23392-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="23392-112">Użyj tego linku, aby learm więcej informacji na temat zmieniania planu appService i powiązanych z nim ograniczeń.</span><span class="sxs-lookup"><span data-stu-id="23392-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="23392-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="23392-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="23392-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23392-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="23392-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla Slot001 gniazda odnoszącego się do aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="23392-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="23392-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23392-116">PARAMETERS</span></span>

### <span data-ttu-id="23392-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="23392-117">-AppServicePlan</span></span>
<span data-ttu-id="23392-118">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="23392-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="23392-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="23392-119">-AppSettings</span></span>
<span data-ttu-id="23392-120">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="23392-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="23392-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23392-121">-AsJob</span></span>
<span data-ttu-id="23392-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="23392-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23392-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="23392-123">-AssignIdentity</span></span>
<span data-ttu-id="23392-124">Włączanie/wyłączanie MSI w istniejącym gnieździe [Podgląd]</span><span class="sxs-lookup"><span data-stu-id="23392-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="23392-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="23392-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="23392-126">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="23392-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="23392-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="23392-127">-AzureStoragePath</span></span>
<span data-ttu-id="23392-128">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="23392-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="23392-129">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="23392-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="23392-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="23392-130">-ConnectionStrings</span></span>
<span data-ttu-id="23392-131">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="23392-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="23392-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="23392-132">-ContainerImageName</span></span>
<span data-ttu-id="23392-133">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="23392-133">Container Image Name</span></span>

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

### <span data-ttu-id="23392-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="23392-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="23392-135">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="23392-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="23392-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="23392-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="23392-137">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="23392-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="23392-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="23392-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="23392-139">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="23392-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="23392-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="23392-140">-DefaultDocuments</span></span>
<span data-ttu-id="23392-141">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="23392-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="23392-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23392-142">-DefaultProfile</span></span>
<span data-ttu-id="23392-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23392-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23392-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="23392-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="23392-145">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="23392-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="23392-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="23392-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="23392-147">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="23392-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="23392-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="23392-148">-HandlerMappings</span></span>
<span data-ttu-id="23392-149">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="23392-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="23392-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="23392-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="23392-151">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="23392-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="23392-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="23392-152">-HttpsOnly</span></span>
<span data-ttu-id="23392-153">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącym gnieździe</span><span class="sxs-lookup"><span data-stu-id="23392-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="23392-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="23392-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="23392-155">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="23392-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="23392-156">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23392-156">-Name</span></span>
<span data-ttu-id="23392-157">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="23392-157">WebApp Name</span></span>

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

### <span data-ttu-id="23392-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="23392-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="23392-159">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="23392-159">Net Framework Version</span></span>

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

### <span data-ttu-id="23392-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="23392-160">-NumberOfWorkers</span></span>
<span data-ttu-id="23392-161">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="23392-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="23392-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="23392-162">-PhpVersion</span></span>
<span data-ttu-id="23392-163">Wersja php</span><span class="sxs-lookup"><span data-stu-id="23392-163">Php Version</span></span>

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

### <span data-ttu-id="23392-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="23392-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="23392-165">Wartość logiczna włączonego śledzenia żądań</span><span class="sxs-lookup"><span data-stu-id="23392-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="23392-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23392-166">-ResourceGroupName</span></span>
<span data-ttu-id="23392-167">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="23392-167">Resource Group Name</span></span>

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

### <span data-ttu-id="23392-168">-Slot</span><span class="sxs-lookup"><span data-stu-id="23392-168">-Slot</span></span>
<span data-ttu-id="23392-169">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="23392-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="23392-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="23392-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="23392-171">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="23392-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="23392-172">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="23392-172">-WebApp</span></span>
<span data-ttu-id="23392-173">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="23392-173">WebApp Object</span></span>

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

### <span data-ttu-id="23392-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="23392-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="23392-175">Wartość logiczna z włączonymi gniazdami sieci Web</span><span class="sxs-lookup"><span data-stu-id="23392-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="23392-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23392-176">CommonParameters</span></span>
<span data-ttu-id="23392-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23392-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23392-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23392-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23392-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23392-179">INPUTS</span></span>

### <span data-ttu-id="23392-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="23392-180">System.Int32</span></span>

### <span data-ttu-id="23392-181">System. String</span><span class="sxs-lookup"><span data-stu-id="23392-181">System.String</span></span>

### <span data-ttu-id="23392-182">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="23392-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="23392-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23392-183">OUTPUTS</span></span>

### <span data-ttu-id="23392-184">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="23392-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="23392-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23392-185">NOTES</span></span>

## <span data-ttu-id="23392-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23392-186">RELATED LINKS</span></span>

[<span data-ttu-id="23392-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23392-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="23392-188">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23392-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="23392-189">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23392-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="23392-190">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23392-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="23392-191">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23392-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="23392-192">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23392-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="23392-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="23392-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
