---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224185"
---
# <span data-ttu-id="17648-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="17648-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="17648-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17648-102">SYNOPSIS</span></span>
<span data-ttu-id="17648-103">Operacja aktualizowania wdrożenia kończącego.</span><span class="sxs-lookup"><span data-stu-id="17648-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="17648-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17648-104">SYNTAX</span></span>

### <span data-ttu-id="17648-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="17648-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="17648-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="17648-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17648-107">Opis</span><span class="sxs-lookup"><span data-stu-id="17648-107">DESCRIPTION</span></span>
<span data-ttu-id="17648-108">Operacja aktualizowania wdrożenia kończącego.</span><span class="sxs-lookup"><span data-stu-id="17648-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="17648-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17648-109">EXAMPLES</span></span>

### <span data-ttu-id="17648-110">Przykład 1: aktualizowanie wdrożenia w chmurze wiosennej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="17648-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="17648-111">Aktualizowanie wdrożenia w chmurze wiosennej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="17648-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="17648-112">Przykład 2: aktualizowanie wdrożenia chmury wiosennej z poziomu potoku.</span><span class="sxs-lookup"><span data-stu-id="17648-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="17648-113">Aktualizowanie wdrożenia chmury wiosennej z poziomu potoku.</span><span class="sxs-lookup"><span data-stu-id="17648-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="17648-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17648-114">PARAMETERS</span></span>

### <span data-ttu-id="17648-115">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="17648-115">-AppName</span></span>
<span data-ttu-id="17648-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="17648-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="17648-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17648-117">-AsJob</span></span>
<span data-ttu-id="17648-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="17648-118">Run the command as a job</span></span>

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

### <span data-ttu-id="17648-119">-Procesor</span><span class="sxs-lookup"><span data-stu-id="17648-119">-Cpu</span></span>
<span data-ttu-id="17648-120">Wymagany procesor</span><span class="sxs-lookup"><span data-stu-id="17648-120">Required CPU</span></span>

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

### <span data-ttu-id="17648-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17648-121">-DefaultProfile</span></span>
<span data-ttu-id="17648-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17648-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17648-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="17648-123">-EnvironmentVariable</span></span>
<span data-ttu-id="17648-124">Kolekcja zmiennych środowiskowych</span><span class="sxs-lookup"><span data-stu-id="17648-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="17648-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="17648-125">-InputObject</span></span>
<span data-ttu-id="17648-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="17648-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17648-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="17648-127">-JvmOption</span></span>
<span data-ttu-id="17648-128">Parametr JVM</span><span class="sxs-lookup"><span data-stu-id="17648-128">JVM parameter</span></span>

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

### <span data-ttu-id="17648-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="17648-129">-MemoryInGb</span></span>
<span data-ttu-id="17648-130">Wymagany rozmiar pamięci w GB</span><span class="sxs-lookup"><span data-stu-id="17648-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="17648-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17648-131">-Name</span></span>
<span data-ttu-id="17648-132">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="17648-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="17648-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="17648-133">-NoWait</span></span>
<span data-ttu-id="17648-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="17648-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="17648-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17648-135">-ResourceGroupName</span></span>
<span data-ttu-id="17648-136">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="17648-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="17648-137">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="17648-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="17648-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="17648-138">-RuntimeVersion</span></span>
<span data-ttu-id="17648-139">Wersja Runtime</span><span class="sxs-lookup"><span data-stu-id="17648-139">Runtime version</span></span>

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

### <span data-ttu-id="17648-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="17648-140">-ServiceName</span></span>
<span data-ttu-id="17648-141">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="17648-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="17648-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="17648-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="17648-143">Selektor dla artefaktu, który ma być wykorzystywany do wdrożenia projektów z wieloma modułami.</span><span class="sxs-lookup"><span data-stu-id="17648-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="17648-144">Powinno to Bethe względną ścieżkę do docelowego modułu/projektu.</span><span class="sxs-lookup"><span data-stu-id="17648-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="17648-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="17648-145">-SourceRelativePath</span></span>
<span data-ttu-id="17648-146">Ścieżka względna miejsca do magazynowania, w którym jest przechowywany źródłowy</span><span class="sxs-lookup"><span data-stu-id="17648-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="17648-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="17648-147">-SourceType</span></span>
<span data-ttu-id="17648-148">Typ przekazanego źródła</span><span class="sxs-lookup"><span data-stu-id="17648-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="17648-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="17648-149">-SourceVersion</span></span>
<span data-ttu-id="17648-150">Wersja źródła</span><span class="sxs-lookup"><span data-stu-id="17648-150">Version of the source</span></span>

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

### <span data-ttu-id="17648-151">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="17648-151">-SubscriptionId</span></span>
<span data-ttu-id="17648-152">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17648-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="17648-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="17648-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="17648-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17648-154">-Confirm</span></span>
<span data-ttu-id="17648-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17648-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17648-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17648-156">-WhatIf</span></span>
<span data-ttu-id="17648-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17648-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17648-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17648-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17648-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17648-159">CommonParameters</span></span>
<span data-ttu-id="17648-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17648-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17648-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17648-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17648-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17648-162">INPUTS</span></span>

### <span data-ttu-id="17648-163">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="17648-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="17648-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17648-164">OUTPUTS</span></span>

### <span data-ttu-id="17648-165">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="17648-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="17648-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17648-166">NOTES</span></span>

<span data-ttu-id="17648-167">PISUJE</span><span class="sxs-lookup"><span data-stu-id="17648-167">ALIASES</span></span>

<span data-ttu-id="17648-168">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17648-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17648-169">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="17648-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17648-170">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17648-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17648-171">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="17648-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17648-172">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="17648-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="17648-173">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="17648-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="17648-174">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="17648-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="17648-175">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="17648-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="17648-176">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="17648-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="17648-177">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="17648-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17648-178">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="17648-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="17648-179">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="17648-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="17648-180">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="17648-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="17648-181">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="17648-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="17648-182">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17648-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="17648-183">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="17648-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="17648-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17648-184">RELATED LINKS</span></span>

