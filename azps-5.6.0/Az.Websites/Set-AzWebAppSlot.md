---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d07d85aa9747982f223d45c40fc8897a0b0e3e73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011105"
---
# <span data-ttu-id="73f44-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="73f44-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="73f44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73f44-102">SYNOPSIS</span></span>
<span data-ttu-id="73f44-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="73f44-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="73f44-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73f44-104">SYNTAX</span></span>

### <span data-ttu-id="73f44-105">S1</span><span class="sxs-lookup"><span data-stu-id="73f44-105">S1</span></span>
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

### <span data-ttu-id="73f44-106">S2</span><span class="sxs-lookup"><span data-stu-id="73f44-106">S2</span></span>
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

## <span data-ttu-id="73f44-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="73f44-107">DESCRIPTION</span></span>
<span data-ttu-id="73f44-108">Polecenie **cmdlet Set-AzWebApp** ustawia slot aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="73f44-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="73f44-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73f44-109">EXAMPLES</span></span>

### <span data-ttu-id="73f44-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73f44-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="73f44-111">To polecenie zmienia plan usługi aplikacji skojarzony z aplikacją Slot001 w aplikacji Webapp ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="73f44-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="73f44-112">Skorzystaj z tego linku, aby dowiedzieć się więcej na temat zmieniania planu usługi aplikacji i skojarzonych z nim ograniczeń.</span><span class="sxs-lookup"><span data-stu-id="73f44-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="73f44-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="73f44-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="73f44-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="73f44-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="73f44-115">To polecenie ustawia wartość HttpLoggingEnabled na prawda dla typu Slot Slot001 odnoszącego się do aplikacji Web App ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="73f44-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="73f44-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="73f44-116">Example 3</span></span>

<span data-ttu-id="73f44-117">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="73f44-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="73f44-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="73f44-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="73f44-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73f44-119">PARAMETERS</span></span>

### <span data-ttu-id="73f44-120">- AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="73f44-120">-AlwaysOn</span></span>
<span data-ttu-id="73f44-121">Upewnij się, że aplikacja sieci Web jest ładowana cały czas, a nie zwolniona po czasie bezczynności.</span><span class="sxs-lookup"><span data-stu-id="73f44-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="73f44-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="73f44-122">-AppServicePlan</span></span>
<span data-ttu-id="73f44-123">Nazwa planu serwisowego aplikacji</span><span class="sxs-lookup"><span data-stu-id="73f44-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="73f44-124">- AppSettings</span><span class="sxs-lookup"><span data-stu-id="73f44-124">-AppSettings</span></span>
<span data-ttu-id="73f44-125">Tabela skrótów ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="73f44-125">App Settings HashTable.</span></span> <span data-ttu-id="73f44-126">Istniejące ustawienia aplikacji zostaną zastąpione, usuwając wszelkie ustawienia, które nie są dostępne.</span><span class="sxs-lookup"><span data-stu-id="73f44-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="73f44-127">— AsJob</span><span class="sxs-lookup"><span data-stu-id="73f44-127">-AsJob</span></span>
<span data-ttu-id="73f44-128">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="73f44-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73f44-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="73f44-129">-AssignIdentity</span></span>
<span data-ttu-id="73f44-130">Włączanie/wyłączanie msi w istniejącym miejscu [WERSJA PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="73f44-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="73f44-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="73f44-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="73f44-132">Nazwa miejsca docelowego dla automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="73f44-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="73f44-133">— AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="73f44-133">-AzureStoragePath</span></span>
<span data-ttu-id="73f44-134">Magazyn platformy Azure do montażu wewnątrz aplikacji sieci Web na kontener.</span><span class="sxs-lookup"><span data-stu-id="73f44-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="73f44-135">Tworzenie New-AzureRmWebAppAzureStoragePath za pomocą aplikacji</span><span class="sxs-lookup"><span data-stu-id="73f44-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="73f44-136">- ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="73f44-136">-ConnectionStrings</span></span>
<span data-ttu-id="73f44-137">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="73f44-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="73f44-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="73f44-138">-ContainerImageName</span></span>
<span data-ttu-id="73f44-139">Nazwa obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="73f44-139">Container Image Name</span></span>

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

### <span data-ttu-id="73f44-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="73f44-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="73f44-141">Hasło do rejestru dla kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="73f44-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="73f44-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="73f44-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="73f44-143">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="73f44-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="73f44-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="73f44-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="73f44-145">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="73f44-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="73f44-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="73f44-146">-DefaultDocuments</span></span>
<span data-ttu-id="73f44-147">Domyślna tablica ciągów dokumentów</span><span class="sxs-lookup"><span data-stu-id="73f44-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="73f44-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f44-148">-DefaultProfile</span></span>
<span data-ttu-id="73f44-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73f44-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73f44-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="73f44-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="73f44-151">Szczegółowa funkcja rejestrowania błędów włączona wartość logiczna</span><span class="sxs-lookup"><span data-stu-id="73f44-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="73f44-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="73f44-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="73f44-153">Włączenie/wyłączenie kontenera ciągłego wdrożenia sieci Web</span><span class="sxs-lookup"><span data-stu-id="73f44-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="73f44-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="73f44-154">-FtpsState</span></span>
<span data-ttu-id="73f44-155">Ustaw wartość stanu Ftps dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="73f44-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="73f44-156">Dozwolone wartości [Wszystkiewszystkie | Wyłączone | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="73f44-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="73f44-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="73f44-157">-HandlerMappings</span></span>
<span data-ttu-id="73f44-158">Lista IList mapowań obsługi</span><span class="sxs-lookup"><span data-stu-id="73f44-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="73f44-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="73f44-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="73f44-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="73f44-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="73f44-161">—httpsOnly</span><span class="sxs-lookup"><span data-stu-id="73f44-161">-HttpsOnly</span></span>
<span data-ttu-id="73f44-162">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS w istniejącym miejscu</span><span class="sxs-lookup"><span data-stu-id="73f44-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="73f44-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="73f44-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="73f44-164">Nazwa trybu zarządzanego potoku</span><span class="sxs-lookup"><span data-stu-id="73f44-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="73f44-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="73f44-165">-MinTlsVersion</span></span>
<span data-ttu-id="73f44-166">Minimalna wersja protokołu TLS wymagana dla żądań SSL.</span><span class="sxs-lookup"><span data-stu-id="73f44-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="73f44-167">Dozwolone wartości [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="73f44-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="73f44-168">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73f44-168">-Name</span></span>
<span data-ttu-id="73f44-169">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="73f44-169">WebApp Name</span></span>

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

### <span data-ttu-id="73f44-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="73f44-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="73f44-171">Wersja programu Net Framework</span><span class="sxs-lookup"><span data-stu-id="73f44-171">Net Framework Version</span></span>

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

### <span data-ttu-id="73f44-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="73f44-172">-NumberOfWorkers</span></span>
<span data-ttu-id="73f44-173">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="73f44-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="73f44-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="73f44-174">-PhpVersion</span></span>
<span data-ttu-id="73f44-175">Wersja Php</span><span class="sxs-lookup"><span data-stu-id="73f44-175">Php Version</span></span>

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

### <span data-ttu-id="73f44-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="73f44-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="73f44-177">Wartość logiczna z włączoną śledzeniem żądania</span><span class="sxs-lookup"><span data-stu-id="73f44-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="73f44-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f44-178">-ResourceGroupName</span></span>
<span data-ttu-id="73f44-179">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="73f44-179">Resource Group Name</span></span>

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

### <span data-ttu-id="73f44-180">— Slot</span><span class="sxs-lookup"><span data-stu-id="73f44-180">-Slot</span></span>
<span data-ttu-id="73f44-181">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="73f44-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="73f44-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="73f44-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="73f44-183">Użyj wartości logicznych 32-bitowej procesów roboczych</span><span class="sxs-lookup"><span data-stu-id="73f44-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="73f44-184">- WebApp</span><span class="sxs-lookup"><span data-stu-id="73f44-184">-WebApp</span></span>
<span data-ttu-id="73f44-185">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="73f44-185">WebApp Object</span></span>

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

### <span data-ttu-id="73f44-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="73f44-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="73f44-187">Wartość logiczna z włączoną obsługą gniazd sieci Web</span><span class="sxs-lookup"><span data-stu-id="73f44-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="73f44-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f44-188">CommonParameters</span></span>
<span data-ttu-id="73f44-189">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f44-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f44-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73f44-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f44-191">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73f44-191">INPUTS</span></span>

### <span data-ttu-id="73f44-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="73f44-192">System.Int32</span></span>

### <span data-ttu-id="73f44-193">System.String</span><span class="sxs-lookup"><span data-stu-id="73f44-193">System.String</span></span>

### <span data-ttu-id="73f44-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="73f44-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="73f44-195">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73f44-195">OUTPUTS</span></span>

### <span data-ttu-id="73f44-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="73f44-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="73f44-197">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73f44-197">NOTES</span></span>

## <span data-ttu-id="73f44-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73f44-198">RELATED LINKS</span></span>

[<span data-ttu-id="73f44-199">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="73f44-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="73f44-200">New-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="73f44-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="73f44-201">Remove-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="73f44-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="73f44-202">Restart-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="73f44-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="73f44-203">Start-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="73f44-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="73f44-204">Stop-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="73f44-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="73f44-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="73f44-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
