---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: de1f09fe6fd484345ebf4ebd7ae2a27d4640c694
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010193"
---
# <span data-ttu-id="40091-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="40091-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="40091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40091-102">SYNOPSIS</span></span>
<span data-ttu-id="40091-103">Utwórz nowe wdrożenie lub zaktualizuj wdrożenie wywszące.</span><span class="sxs-lookup"><span data-stu-id="40091-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="40091-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40091-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="40091-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="40091-105">DESCRIPTION</span></span>
<span data-ttu-id="40091-106">Utwórz nowe wdrożenie lub zaktualizuj wdrożenie wywszące.</span><span class="sxs-lookup"><span data-stu-id="40091-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="40091-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40091-107">EXAMPLES</span></span>

### <span data-ttu-id="40091-108">Przykład 1. Przykład 1. Tworzenie wiosennego wdrożenia w chmurze.</span><span class="sxs-lookup"><span data-stu-id="40091-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="40091-109">Utwórz wiosenne wdrożenie w chmurze.</span><span class="sxs-lookup"><span data-stu-id="40091-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="40091-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40091-110">PARAMETERS</span></span>

### <span data-ttu-id="40091-111">- AppName</span><span class="sxs-lookup"><span data-stu-id="40091-111">-AppName</span></span>
<span data-ttu-id="40091-112">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="40091-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="40091-113">-AsJob</span></span>
<span data-ttu-id="40091-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="40091-114">Run the command as a job</span></span>

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

### <span data-ttu-id="40091-115">— Procesor</span><span class="sxs-lookup"><span data-stu-id="40091-115">-Cpu</span></span>
<span data-ttu-id="40091-116">Wymagany procesor</span><span class="sxs-lookup"><span data-stu-id="40091-116">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40091-117">-DefaultProfile</span></span>
<span data-ttu-id="40091-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40091-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-119">— EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="40091-119">-EnvironmentVariable</span></span>
<span data-ttu-id="40091-120">Zbiór zmiennych środowiska</span><span class="sxs-lookup"><span data-stu-id="40091-120">Collection of environment variables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="40091-121">-JvmOption</span></span>
<span data-ttu-id="40091-122">Parametr JVM</span><span class="sxs-lookup"><span data-stu-id="40091-122">JVM parameter</span></span>

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

### <span data-ttu-id="40091-123">- MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="40091-123">-MemoryInGb</span></span>
<span data-ttu-id="40091-124">Wymagany rozmiar pamięci w GB</span><span class="sxs-lookup"><span data-stu-id="40091-124">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="40091-125">-Name</span></span>
<span data-ttu-id="40091-126">Nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="40091-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="40091-127">-NoWait</span></span>
<span data-ttu-id="40091-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="40091-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="40091-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40091-129">-ResourceGroupName</span></span>
<span data-ttu-id="40091-130">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="40091-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="40091-131">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="40091-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="40091-132">-RuntimeVersion</span></span>
<span data-ttu-id="40091-133">Wersja środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="40091-133">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="40091-134">-ServiceName</span></span>
<span data-ttu-id="40091-135">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="40091-135">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="40091-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="40091-137">Selektor artefaktu, który ma być używany do wdrożenia w projektach wielo module.</span><span class="sxs-lookup"><span data-stu-id="40091-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="40091-138">Powinna to być względna ścieżka do modułu docelowego/projektu.</span><span class="sxs-lookup"><span data-stu-id="40091-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="40091-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="40091-139">-SourceRelativePath</span></span>
<span data-ttu-id="40091-140">Względna ścieżka magazynu, w którym jest przechowywane źródło</span><span class="sxs-lookup"><span data-stu-id="40091-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="40091-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="40091-141">-SourceType</span></span>
<span data-ttu-id="40091-142">Typ przekazanego źródła</span><span class="sxs-lookup"><span data-stu-id="40091-142">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="40091-143">-SourceVersion</span></span>
<span data-ttu-id="40091-144">Wersja źródła</span><span class="sxs-lookup"><span data-stu-id="40091-144">Version of the source</span></span>

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

### <span data-ttu-id="40091-145">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40091-145">-SubscriptionId</span></span>
<span data-ttu-id="40091-146">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40091-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="40091-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="40091-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40091-148">-Confirm</span></span>
<span data-ttu-id="40091-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="40091-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40091-150">-WhatIf</span></span>
<span data-ttu-id="40091-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40091-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40091-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="40091-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40091-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40091-153">CommonParameters</span></span>
<span data-ttu-id="40091-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40091-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40091-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40091-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40091-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40091-156">INPUTS</span></span>

## <span data-ttu-id="40091-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40091-157">OUTPUTS</span></span>

### <span data-ttu-id="40091-158">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.Api200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="40091-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="40091-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40091-159">NOTES</span></span>

<span data-ttu-id="40091-160">ALIASY</span><span class="sxs-lookup"><span data-stu-id="40091-160">ALIASES</span></span>

## <span data-ttu-id="40091-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40091-161">RELATED LINKS</span></span>

