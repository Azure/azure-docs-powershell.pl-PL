---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188970"
---
# <span data-ttu-id="0aa44-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="0aa44-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="0aa44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aa44-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa44-103">Operacja aktualizacji wywłaszacego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0aa44-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="0aa44-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0aa44-104">SYNTAX</span></span>

### <span data-ttu-id="0aa44-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0aa44-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0aa44-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0aa44-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0aa44-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0aa44-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa44-108">Operacja aktualizacji wdrożenia wywszego.</span><span class="sxs-lookup"><span data-stu-id="0aa44-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="0aa44-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0aa44-109">EXAMPLES</span></span>

### <span data-ttu-id="0aa44-110">Przykład 1. Aktualizowanie wiosennego wdrożenia chmury według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0aa44-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="0aa44-111">Zaktualizuj wiosenne wdrożenie w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0aa44-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="0aa44-112">Przykład 2. Zaktualizuj wiosenne wdrożenie chmury z potoku.</span><span class="sxs-lookup"><span data-stu-id="0aa44-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="0aa44-113">Zaktualizuj wiosenne wdrożenie w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="0aa44-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="0aa44-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0aa44-114">PARAMETERS</span></span>

### <span data-ttu-id="0aa44-115">- AppName</span><span class="sxs-lookup"><span data-stu-id="0aa44-115">-AppName</span></span>
<span data-ttu-id="0aa44-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0aa44-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa44-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0aa44-117">-AsJob</span></span>
<span data-ttu-id="0aa44-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0aa44-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0aa44-119">— Procesor</span><span class="sxs-lookup"><span data-stu-id="0aa44-119">-Cpu</span></span>
<span data-ttu-id="0aa44-120">Wymagany procesor</span><span class="sxs-lookup"><span data-stu-id="0aa44-120">Required CPU</span></span>

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

### <span data-ttu-id="0aa44-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa44-121">-DefaultProfile</span></span>
<span data-ttu-id="0aa44-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa44-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aa44-123">—EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="0aa44-123">-EnvironmentVariable</span></span>
<span data-ttu-id="0aa44-124">Zbiór zmiennych środowiska</span><span class="sxs-lookup"><span data-stu-id="0aa44-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="0aa44-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aa44-125">-InputObject</span></span>
<span data-ttu-id="0aa44-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0aa44-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa44-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="0aa44-127">-JvmOption</span></span>
<span data-ttu-id="0aa44-128">Parametr JVM</span><span class="sxs-lookup"><span data-stu-id="0aa44-128">JVM parameter</span></span>

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

### <span data-ttu-id="0aa44-129">- MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="0aa44-129">-MemoryInGb</span></span>
<span data-ttu-id="0aa44-130">Wymagany rozmiar pamięci w GB</span><span class="sxs-lookup"><span data-stu-id="0aa44-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="0aa44-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0aa44-131">-Name</span></span>
<span data-ttu-id="0aa44-132">Nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="0aa44-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa44-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0aa44-133">-NoWait</span></span>
<span data-ttu-id="0aa44-134">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0aa44-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0aa44-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa44-135">-ResourceGroupName</span></span>
<span data-ttu-id="0aa44-136">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="0aa44-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0aa44-137">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="0aa44-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa44-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="0aa44-138">-RuntimeVersion</span></span>
<span data-ttu-id="0aa44-139">Wersja środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="0aa44-139">Runtime version</span></span>

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

### <span data-ttu-id="0aa44-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0aa44-140">-ServiceName</span></span>
<span data-ttu-id="0aa44-141">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="0aa44-141">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa44-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="0aa44-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="0aa44-143">Selektor artefaktu, który ma być używany do wdrożenia w projektach wielo module.</span><span class="sxs-lookup"><span data-stu-id="0aa44-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="0aa44-144">Powinna to być względna ścieżka do modułu docelowego/projektu.</span><span class="sxs-lookup"><span data-stu-id="0aa44-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="0aa44-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="0aa44-145">-SourceRelativePath</span></span>
<span data-ttu-id="0aa44-146">Względna ścieżka magazynu, w którym jest przechowywane źródło</span><span class="sxs-lookup"><span data-stu-id="0aa44-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="0aa44-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="0aa44-147">-SourceType</span></span>
<span data-ttu-id="0aa44-148">Typ przekazanego źródła</span><span class="sxs-lookup"><span data-stu-id="0aa44-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="0aa44-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="0aa44-149">-SourceVersion</span></span>
<span data-ttu-id="0aa44-150">Wersja źródła</span><span class="sxs-lookup"><span data-stu-id="0aa44-150">Version of the source</span></span>

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

### <span data-ttu-id="0aa44-151">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0aa44-151">-SubscriptionId</span></span>
<span data-ttu-id="0aa44-152">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa44-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0aa44-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0aa44-153">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa44-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0aa44-154">-Confirm</span></span>
<span data-ttu-id="0aa44-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0aa44-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa44-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa44-156">-WhatIf</span></span>
<span data-ttu-id="0aa44-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aa44-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa44-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0aa44-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aa44-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa44-159">CommonParameters</span></span>
<span data-ttu-id="0aa44-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aa44-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa44-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0aa44-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa44-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0aa44-162">INPUTS</span></span>

### <span data-ttu-id="0aa44-163">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="0aa44-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="0aa44-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0aa44-164">OUTPUTS</span></span>

### <span data-ttu-id="0aa44-165">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="0aa44-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="0aa44-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0aa44-166">NOTES</span></span>

<span data-ttu-id="0aa44-167">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0aa44-167">ALIASES</span></span>

<span data-ttu-id="0aa44-168">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0aa44-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0aa44-169">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0aa44-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0aa44-170">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0aa44-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0aa44-171">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0aa44-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0aa44-172">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0aa44-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="0aa44-173">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="0aa44-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="0aa44-174">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0aa44-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="0aa44-175">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="0aa44-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="0aa44-176">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="0aa44-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="0aa44-177">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0aa44-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0aa44-178">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="0aa44-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="0aa44-179">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="0aa44-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0aa44-180">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="0aa44-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0aa44-181">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="0aa44-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="0aa44-182">`[SubscriptionId <String>]`: otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa44-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="0aa44-183">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0aa44-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0aa44-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0aa44-184">RELATED LINKS</span></span>

