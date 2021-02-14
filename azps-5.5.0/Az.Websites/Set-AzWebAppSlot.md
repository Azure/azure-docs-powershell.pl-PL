---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197218"
---
# <span data-ttu-id="8aa6f-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="8aa6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa6f-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa6f-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="8aa6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8aa6f-104">SYNTAX</span></span>

### <span data-ttu-id="8aa6f-105">S1</span><span class="sxs-lookup"><span data-stu-id="8aa6f-105">S1</span></span>
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

### <span data-ttu-id="8aa6f-106">S2</span><span class="sxs-lookup"><span data-stu-id="8aa6f-106">S2</span></span>
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

## <span data-ttu-id="8aa6f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8aa6f-107">DESCRIPTION</span></span>
<span data-ttu-id="8aa6f-108">Polecenie **cmdlet Set-AzWebApp** ustawia slot aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="8aa6f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8aa6f-109">EXAMPLES</span></span>

### <span data-ttu-id="8aa6f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8aa6f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="8aa6f-111">To polecenie zmienia plan usługi aplikacji skojarzony z aplikacją Slot001 w aplikacji Webapp ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="8aa6f-112">Skorzystaj z tego linku, aby dowiedzieć się więcej na temat zmieniania planu usługi aplikacji i skojarzonych z nim ograniczeń.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="8aa6f-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="8aa6f-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="8aa6f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8aa6f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="8aa6f-115">To polecenie ustawia wartość HttpLoggingEnabled na prawda dla typu Slot Slot001 odnoszącego się do aplikacji Web App ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="8aa6f-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="8aa6f-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8aa6f-116">Example 3</span></span>

<span data-ttu-id="8aa6f-117">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="8aa6f-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="8aa6f-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="8aa6f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aa6f-119">PARAMETERS</span></span>

### <span data-ttu-id="8aa6f-120">- AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="8aa6f-120">-AlwaysOn</span></span>
<span data-ttu-id="8aa6f-121">Upewnij się, że aplikacja sieci Web jest ładowana cały czas, a nie zwalniana po czasie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="8aa6f-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8aa6f-122">-AppServicePlan</span></span>
<span data-ttu-id="8aa6f-123">Nazwa planu serwisowego aplikacji</span><span class="sxs-lookup"><span data-stu-id="8aa6f-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="8aa6f-124">- AppSettings</span><span class="sxs-lookup"><span data-stu-id="8aa6f-124">-AppSettings</span></span>
<span data-ttu-id="8aa6f-125">Tabela skrótów ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-125">App Settings HashTable.</span></span> <span data-ttu-id="8aa6f-126">Istniejące ustawienia aplikacji zostaną zastąpione, usuwając wszelkie ustawienia, które nie są dostępne.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="8aa6f-127">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8aa6f-127">-AsJob</span></span>
<span data-ttu-id="8aa6f-128">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8aa6f-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8aa6f-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8aa6f-129">-AssignIdentity</span></span>
<span data-ttu-id="8aa6f-130">Włączanie/wyłączanie msi w istniejącym miejscu [WERSJA PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="8aa6f-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="8aa6f-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="8aa6f-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="8aa6f-132">Nazwa miejsca docelowego dla automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="8aa6f-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="8aa6f-133">— AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8aa6f-133">-AzureStoragePath</span></span>
<span data-ttu-id="8aa6f-134">Magazyn platformy Azure do montażu wewnątrz aplikacji sieci Web na kontener.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="8aa6f-135">Tworzenie New-AzureRmWebAppAzureStoragePath za pomocą aplikacji</span><span class="sxs-lookup"><span data-stu-id="8aa6f-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="8aa6f-136">- ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="8aa6f-136">-ConnectionStrings</span></span>
<span data-ttu-id="8aa6f-137">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="8aa6f-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="8aa6f-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="8aa6f-138">-ContainerImageName</span></span>
<span data-ttu-id="8aa6f-139">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="8aa6f-139">Container Image Name</span></span>

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

### <span data-ttu-id="8aa6f-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8aa6f-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8aa6f-141">Hasło do rejestru dla kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="8aa6f-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8aa6f-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8aa6f-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8aa6f-143">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="8aa6f-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8aa6f-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8aa6f-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="8aa6f-145">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="8aa6f-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8aa6f-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="8aa6f-146">-DefaultDocuments</span></span>
<span data-ttu-id="8aa6f-147">Domyślna tablica ciągów dokumentów</span><span class="sxs-lookup"><span data-stu-id="8aa6f-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="8aa6f-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa6f-148">-DefaultProfile</span></span>
<span data-ttu-id="8aa6f-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aa6f-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8aa6f-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="8aa6f-151">Szczegółowe informacje o włączonej wartości logicznych rejestrowania błędów</span><span class="sxs-lookup"><span data-stu-id="8aa6f-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="8aa6f-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8aa6f-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8aa6f-153">Włączenie/wyłączenie kontenera ciągłego wdrożenia sieci Web</span><span class="sxs-lookup"><span data-stu-id="8aa6f-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8aa6f-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="8aa6f-154">-FtpsState</span></span>
<span data-ttu-id="8aa6f-155">Ustaw wartość stanu Ftps dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="8aa6f-156">Dozwolone wartości [Wszystkiewszystkie | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="8aa6f-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="8aa6f-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="8aa6f-157">-HandlerMappings</span></span>
<span data-ttu-id="8aa6f-158">Lista IList mapowań obsługi</span><span class="sxs-lookup"><span data-stu-id="8aa6f-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="8aa6f-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8aa6f-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="8aa6f-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="8aa6f-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="8aa6f-161">—httpsOnly</span><span class="sxs-lookup"><span data-stu-id="8aa6f-161">-HttpsOnly</span></span>
<span data-ttu-id="8aa6f-162">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącym miejscu</span><span class="sxs-lookup"><span data-stu-id="8aa6f-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="8aa6f-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="8aa6f-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="8aa6f-164">Nazwa trybu zarządzanego potoku</span><span class="sxs-lookup"><span data-stu-id="8aa6f-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="8aa6f-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8aa6f-165">-MinTlsVersion</span></span>
<span data-ttu-id="8aa6f-166">Minimalna wersja protokołu TLS wymagana dla żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="8aa6f-167">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="8aa6f-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="8aa6f-168">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8aa6f-168">-Name</span></span>
<span data-ttu-id="8aa6f-169">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8aa6f-169">WebApp Name</span></span>

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

### <span data-ttu-id="8aa6f-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="8aa6f-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="8aa6f-171">Wersja programu Net Framework</span><span class="sxs-lookup"><span data-stu-id="8aa6f-171">Net Framework Version</span></span>

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

### <span data-ttu-id="8aa6f-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="8aa6f-172">-NumberOfWorkers</span></span>
<span data-ttu-id="8aa6f-173">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="8aa6f-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="8aa6f-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="8aa6f-174">-PhpVersion</span></span>
<span data-ttu-id="8aa6f-175">Wersja Php</span><span class="sxs-lookup"><span data-stu-id="8aa6f-175">Php Version</span></span>

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

### <span data-ttu-id="8aa6f-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="8aa6f-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="8aa6f-177">Wartość logiczna z włączoną śledzeniem żądania</span><span class="sxs-lookup"><span data-stu-id="8aa6f-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="8aa6f-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa6f-178">-ResourceGroupName</span></span>
<span data-ttu-id="8aa6f-179">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8aa6f-179">Resource Group Name</span></span>

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

### <span data-ttu-id="8aa6f-180">— Slot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-180">-Slot</span></span>
<span data-ttu-id="8aa6f-181">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8aa6f-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8aa6f-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="8aa6f-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="8aa6f-183">Użyj wartości logicznych 32-bitowej procesów roboczych</span><span class="sxs-lookup"><span data-stu-id="8aa6f-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="8aa6f-184">— WebApp</span><span class="sxs-lookup"><span data-stu-id="8aa6f-184">-WebApp</span></span>
<span data-ttu-id="8aa6f-185">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="8aa6f-185">WebApp Object</span></span>

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

### <span data-ttu-id="8aa6f-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="8aa6f-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="8aa6f-187">Wartość logiczna z włączoną obsługą gniazd sieci Web</span><span class="sxs-lookup"><span data-stu-id="8aa6f-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="8aa6f-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa6f-188">CommonParameters</span></span>
<span data-ttu-id="8aa6f-189">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa6f-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aa6f-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa6f-191">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aa6f-191">INPUTS</span></span>

### <span data-ttu-id="8aa6f-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8aa6f-192">System.Int32</span></span>

### <span data-ttu-id="8aa6f-193">System.String</span><span class="sxs-lookup"><span data-stu-id="8aa6f-193">System.String</span></span>

### <span data-ttu-id="8aa6f-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8aa6f-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8aa6f-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8aa6f-195">OUTPUTS</span></span>

### <span data-ttu-id="8aa6f-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8aa6f-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8aa6f-197">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8aa6f-197">NOTES</span></span>

## <span data-ttu-id="8aa6f-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aa6f-198">RELATED LINKS</span></span>

[<span data-ttu-id="8aa6f-199">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8aa6f-200">New-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8aa6f-201">Remove-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8aa6f-202">Restart-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8aa6f-203">Start-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8aa6f-204">Stop-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8aa6f-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8aa6f-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8aa6f-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
