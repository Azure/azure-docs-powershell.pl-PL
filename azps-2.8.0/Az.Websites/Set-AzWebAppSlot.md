---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888654"
---
# <span data-ttu-id="fa834-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa834-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="fa834-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa834-102">SYNOPSIS</span></span>
<span data-ttu-id="fa834-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fa834-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="fa834-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa834-104">SYNTAX</span></span>

### <span data-ttu-id="fa834-105">S1</span><span class="sxs-lookup"><span data-stu-id="fa834-105">S1</span></span>
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

### <span data-ttu-id="fa834-106">S2</span><span class="sxs-lookup"><span data-stu-id="fa834-106">S2</span></span>
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

## <span data-ttu-id="fa834-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa834-107">DESCRIPTION</span></span>
<span data-ttu-id="fa834-108">Polecenie cmdlet **Set-AzWebApp** ustawia miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fa834-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="fa834-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa834-109">EXAMPLES</span></span>

### <span data-ttu-id="fa834-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa834-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="fa834-111">To polecenie powoduje zmianę planu appService skojarzonego z Slot001 na karcie aplikacji ContosoWebApp powiązanej z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="fa834-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="fa834-112">Użyj tego linku, aby dowiedzieć się więcej o zmienianiu appService planu i ograniczeń z nim skojarzonych.</span><span class="sxs-lookup"><span data-stu-id="fa834-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="fa834-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="fa834-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="fa834-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fa834-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="fa834-115">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla Slot001 gniazda odnoszącego się do aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="fa834-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="fa834-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa834-116">PARAMETERS</span></span>

### <span data-ttu-id="fa834-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fa834-117">-AppServicePlan</span></span>
<span data-ttu-id="fa834-118">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="fa834-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="fa834-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="fa834-119">-AppSettings</span></span>
<span data-ttu-id="fa834-120">Ustawienia aplikacji HashTable.</span><span class="sxs-lookup"><span data-stu-id="fa834-120">App Settings HashTable.</span></span> <span data-ttu-id="fa834-121">Istniejące ustawienia aplikacji zostaną zastąpione, co spowoduje usunięcie wszystkich ustawień, które nie zostały podane.</span><span class="sxs-lookup"><span data-stu-id="fa834-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="fa834-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa834-122">-AsJob</span></span>
<span data-ttu-id="fa834-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fa834-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa834-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fa834-124">-AssignIdentity</span></span>
<span data-ttu-id="fa834-125">Włączanie/wyłączanie MSI w istniejącym gnieździe [Podgląd]</span><span class="sxs-lookup"><span data-stu-id="fa834-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="fa834-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="fa834-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="fa834-127">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="fa834-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="fa834-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="fa834-128">-AzureStoragePath</span></span>
<span data-ttu-id="fa834-129">Usługa Azure Storage do zainstalowania w aplikacji sieci Web dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="fa834-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="fa834-130">Utwórz go za pomocą New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="fa834-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="fa834-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="fa834-131">-ConnectionStrings</span></span>
<span data-ttu-id="fa834-132">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="fa834-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="fa834-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="fa834-133">-ContainerImageName</span></span>
<span data-ttu-id="fa834-134">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="fa834-134">Container Image Name</span></span>

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

### <span data-ttu-id="fa834-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="fa834-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="fa834-136">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="fa834-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="fa834-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="fa834-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="fa834-138">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="fa834-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="fa834-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="fa834-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="fa834-140">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="fa834-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="fa834-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="fa834-141">-DefaultDocuments</span></span>
<span data-ttu-id="fa834-142">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="fa834-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="fa834-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa834-143">-DefaultProfile</span></span>
<span data-ttu-id="fa834-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa834-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa834-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa834-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="fa834-146">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="fa834-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="fa834-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="fa834-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="fa834-148">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="fa834-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="fa834-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="fa834-149">-HandlerMappings</span></span>
<span data-ttu-id="fa834-150">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="fa834-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="fa834-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa834-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="fa834-152">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa834-152">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="fa834-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fa834-153">-HttpsOnly</span></span>
<span data-ttu-id="fa834-154">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącym gnieździe</span><span class="sxs-lookup"><span data-stu-id="fa834-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="fa834-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="fa834-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="fa834-156">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="fa834-156">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="fa834-157">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa834-157">-Name</span></span>
<span data-ttu-id="fa834-158">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa834-158">WebApp Name</span></span>

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

### <span data-ttu-id="fa834-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="fa834-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="fa834-160">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="fa834-160">Net Framework Version</span></span>

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

### <span data-ttu-id="fa834-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="fa834-161">-NumberOfWorkers</span></span>
<span data-ttu-id="fa834-162">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="fa834-162">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="fa834-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="fa834-163">-PhpVersion</span></span>
<span data-ttu-id="fa834-164">Wersja php</span><span class="sxs-lookup"><span data-stu-id="fa834-164">Php Version</span></span>

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

### <span data-ttu-id="fa834-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa834-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="fa834-166">Wartość logiczna włączonego śledzenia żądań</span><span class="sxs-lookup"><span data-stu-id="fa834-166">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="fa834-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa834-167">-ResourceGroupName</span></span>
<span data-ttu-id="fa834-168">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fa834-168">Resource Group Name</span></span>

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

### <span data-ttu-id="fa834-169">-Slot</span><span class="sxs-lookup"><span data-stu-id="fa834-169">-Slot</span></span>
<span data-ttu-id="fa834-170">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa834-170">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fa834-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="fa834-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="fa834-172">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="fa834-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="fa834-173">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa834-173">-WebApp</span></span>
<span data-ttu-id="fa834-174">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa834-174">WebApp Object</span></span>

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

### <span data-ttu-id="fa834-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="fa834-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="fa834-176">Wartość logiczna z włączonymi gniazdami sieci Web</span><span class="sxs-lookup"><span data-stu-id="fa834-176">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="fa834-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa834-177">CommonParameters</span></span>
<span data-ttu-id="fa834-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa834-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa834-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa834-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa834-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa834-180">INPUTS</span></span>

### <span data-ttu-id="fa834-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fa834-181">System.Int32</span></span>

### <span data-ttu-id="fa834-182">System. String</span><span class="sxs-lookup"><span data-stu-id="fa834-182">System.String</span></span>

### <span data-ttu-id="fa834-183">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="fa834-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fa834-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa834-184">OUTPUTS</span></span>

### <span data-ttu-id="fa834-185">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="fa834-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fa834-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa834-186">NOTES</span></span>

## <span data-ttu-id="fa834-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa834-187">RELATED LINKS</span></span>

[<span data-ttu-id="fa834-188">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa834-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="fa834-189">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa834-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="fa834-190">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa834-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="fa834-191">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa834-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="fa834-192">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa834-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="fa834-193">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa834-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="fa834-194">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fa834-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
