---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 466bf2908cf1da940a369d2276dbf39106d60515
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005306"
---
# <span data-ttu-id="a572b-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="a572b-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="a572b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a572b-102">SYNOPSIS</span></span>
<span data-ttu-id="a572b-103">Operacja aktualizacji wywłaszacego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a572b-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="a572b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a572b-104">SYNTAX</span></span>

### <span data-ttu-id="a572b-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a572b-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a572b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a572b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a572b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a572b-107">DESCRIPTION</span></span>
<span data-ttu-id="a572b-108">Operacja aktualizacji wywłaszacego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a572b-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="a572b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a572b-109">EXAMPLES</span></span>

### <span data-ttu-id="a572b-110">Przykład 1. Aktualizowanie wiosennego wdrożenia chmury według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a572b-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="a572b-111">Zaktualizuj wiosenne wdrożenie w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a572b-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="a572b-112">Przykład 2. Zaktualizuj wiosenne wdrożenie chmury z potoku.</span><span class="sxs-lookup"><span data-stu-id="a572b-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="a572b-113">Zaktualizuj wiosenne wdrożenie w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="a572b-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="a572b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a572b-114">PARAMETERS</span></span>

### <span data-ttu-id="a572b-115">- AppName</span><span class="sxs-lookup"><span data-stu-id="a572b-115">-AppName</span></span>
<span data-ttu-id="a572b-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a572b-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="a572b-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a572b-117">-AsJob</span></span>
<span data-ttu-id="a572b-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a572b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a572b-119">— Procesor</span><span class="sxs-lookup"><span data-stu-id="a572b-119">-Cpu</span></span>
<span data-ttu-id="a572b-120">Wymagany procesor</span><span class="sxs-lookup"><span data-stu-id="a572b-120">Required CPU</span></span>

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

### <span data-ttu-id="a572b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a572b-121">-DefaultProfile</span></span>
<span data-ttu-id="a572b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a572b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a572b-123">— EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="a572b-123">-EnvironmentVariable</span></span>
<span data-ttu-id="a572b-124">Zbiór zmiennych środowiska</span><span class="sxs-lookup"><span data-stu-id="a572b-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="a572b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a572b-125">-InputObject</span></span>
<span data-ttu-id="a572b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a572b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a572b-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="a572b-127">-JvmOption</span></span>
<span data-ttu-id="a572b-128">Parametr JVM</span><span class="sxs-lookup"><span data-stu-id="a572b-128">JVM parameter</span></span>

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

### <span data-ttu-id="a572b-129">- MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="a572b-129">-MemoryInGb</span></span>
<span data-ttu-id="a572b-130">Wymagany rozmiar pamięci w GB</span><span class="sxs-lookup"><span data-stu-id="a572b-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="a572b-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a572b-131">-Name</span></span>
<span data-ttu-id="a572b-132">Nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a572b-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="a572b-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a572b-133">-NoWait</span></span>
<span data-ttu-id="a572b-134">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a572b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a572b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a572b-135">-ResourceGroupName</span></span>
<span data-ttu-id="a572b-136">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="a572b-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a572b-137">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a572b-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a572b-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="a572b-138">-RuntimeVersion</span></span>
<span data-ttu-id="a572b-139">Wersja środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="a572b-139">Runtime version</span></span>

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

### <span data-ttu-id="a572b-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a572b-140">-ServiceName</span></span>
<span data-ttu-id="a572b-141">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="a572b-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="a572b-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="a572b-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="a572b-143">Selektor artefaktu, który ma być używany do wdrożenia w projektach wielo module.</span><span class="sxs-lookup"><span data-stu-id="a572b-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="a572b-144">Powinna to być względna ścieżka do modułu docelowego/projektu.</span><span class="sxs-lookup"><span data-stu-id="a572b-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="a572b-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="a572b-145">-SourceRelativePath</span></span>
<span data-ttu-id="a572b-146">Względna ścieżka magazynu, w którym jest przechowywane źródło</span><span class="sxs-lookup"><span data-stu-id="a572b-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="a572b-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="a572b-147">-SourceType</span></span>
<span data-ttu-id="a572b-148">Typ przekazanego źródła</span><span class="sxs-lookup"><span data-stu-id="a572b-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="a572b-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="a572b-149">-SourceVersion</span></span>
<span data-ttu-id="a572b-150">Wersja źródła</span><span class="sxs-lookup"><span data-stu-id="a572b-150">Version of the source</span></span>

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

### <span data-ttu-id="a572b-151">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a572b-151">-SubscriptionId</span></span>
<span data-ttu-id="a572b-152">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a572b-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a572b-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="a572b-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a572b-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a572b-154">-Confirm</span></span>
<span data-ttu-id="a572b-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a572b-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a572b-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a572b-156">-WhatIf</span></span>
<span data-ttu-id="a572b-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a572b-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a572b-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a572b-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a572b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a572b-159">CommonParameters</span></span>
<span data-ttu-id="a572b-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a572b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a572b-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a572b-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a572b-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a572b-162">INPUTS</span></span>

### <span data-ttu-id="a572b-163">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a572b-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a572b-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a572b-164">OUTPUTS</span></span>

### <span data-ttu-id="a572b-165">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.Api200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="a572b-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="a572b-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a572b-166">NOTES</span></span>

<span data-ttu-id="a572b-167">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a572b-167">ALIASES</span></span>

<span data-ttu-id="a572b-168">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a572b-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a572b-169">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a572b-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a572b-170">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a572b-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a572b-171">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="a572b-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a572b-172">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a572b-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a572b-173">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="a572b-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a572b-174">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a572b-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a572b-175">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a572b-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a572b-176">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="a572b-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a572b-177">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a572b-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a572b-178">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="a572b-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a572b-179">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="a572b-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a572b-180">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a572b-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a572b-181">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="a572b-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a572b-182">`[SubscriptionId <String>]`: otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a572b-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a572b-183">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="a572b-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a572b-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a572b-184">RELATED LINKS</span></span>

