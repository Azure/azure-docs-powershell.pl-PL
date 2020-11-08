---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222252"
---
# <span data-ttu-id="b421b-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="b421b-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="b421b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b421b-102">SYNOPSIS</span></span>
<span data-ttu-id="b421b-103">Operacja aktualizowania wdrożenia kończącego.</span><span class="sxs-lookup"><span data-stu-id="b421b-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="b421b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b421b-104">SYNTAX</span></span>

### <span data-ttu-id="b421b-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b421b-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b421b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b421b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b421b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b421b-107">DESCRIPTION</span></span>
<span data-ttu-id="b421b-108">Operacja aktualizowania wdrożenia kończącego.</span><span class="sxs-lookup"><span data-stu-id="b421b-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="b421b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b421b-109">EXAMPLES</span></span>

### <span data-ttu-id="b421b-110">Przykład 1: aktualizowanie wdrożenia w chmurze wiosennej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b421b-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="b421b-111">Aktualizowanie wdrożenia w chmurze wiosennej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b421b-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="b421b-112">Przykład 2: aktualizowanie wdrożenia chmury wiosennej z poziomu potoku.</span><span class="sxs-lookup"><span data-stu-id="b421b-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="b421b-113">Aktualizowanie wdrożenia chmury wiosennej z poziomu potoku.</span><span class="sxs-lookup"><span data-stu-id="b421b-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="b421b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b421b-114">PARAMETERS</span></span>

### <span data-ttu-id="b421b-115">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="b421b-115">-AppName</span></span>
<span data-ttu-id="b421b-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b421b-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="b421b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b421b-117">-AsJob</span></span>
<span data-ttu-id="b421b-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b421b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b421b-119">-Procesor</span><span class="sxs-lookup"><span data-stu-id="b421b-119">-Cpu</span></span>
<span data-ttu-id="b421b-120">Wymagany procesor</span><span class="sxs-lookup"><span data-stu-id="b421b-120">Required CPU</span></span>

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

### <span data-ttu-id="b421b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b421b-121">-DefaultProfile</span></span>
<span data-ttu-id="b421b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b421b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b421b-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="b421b-123">-EnvironmentVariable</span></span>
<span data-ttu-id="b421b-124">Kolekcja zmiennych środowiskowych</span><span class="sxs-lookup"><span data-stu-id="b421b-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="b421b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b421b-125">-InputObject</span></span>
<span data-ttu-id="b421b-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b421b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b421b-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="b421b-127">-InstanceCount</span></span>
<span data-ttu-id="b421b-128">Liczba wystąpień</span><span class="sxs-lookup"><span data-stu-id="b421b-128">Instance count</span></span>

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

### <span data-ttu-id="b421b-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="b421b-129">-JvmOption</span></span>
<span data-ttu-id="b421b-130">Parametr JVM</span><span class="sxs-lookup"><span data-stu-id="b421b-130">JVM parameter</span></span>

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

### <span data-ttu-id="b421b-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="b421b-131">-MemoryInGb</span></span>
<span data-ttu-id="b421b-132">Wymagany rozmiar pamięci w GB</span><span class="sxs-lookup"><span data-stu-id="b421b-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="b421b-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b421b-133">-Name</span></span>
<span data-ttu-id="b421b-134">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b421b-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="b421b-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b421b-135">-NoWait</span></span>
<span data-ttu-id="b421b-136">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b421b-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b421b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b421b-137">-ResourceGroupName</span></span>
<span data-ttu-id="b421b-138">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b421b-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b421b-139">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b421b-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b421b-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="b421b-140">-RuntimeVersion</span></span>
<span data-ttu-id="b421b-141">Wersja Runtime</span><span class="sxs-lookup"><span data-stu-id="b421b-141">Runtime version</span></span>

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

### <span data-ttu-id="b421b-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b421b-142">-ServiceName</span></span>
<span data-ttu-id="b421b-143">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="b421b-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b421b-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="b421b-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="b421b-145">Selektor dla artefaktu, który ma być wykorzystywany do wdrożenia projektów z wieloma modułami.</span><span class="sxs-lookup"><span data-stu-id="b421b-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="b421b-146">Powinno to Bethe względną ścieżkę do docelowego modułu/projektu.</span><span class="sxs-lookup"><span data-stu-id="b421b-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="b421b-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b421b-147">-SourceRelativePath</span></span>
<span data-ttu-id="b421b-148">Ścieżka względna miejsca do magazynowania, w którym jest przechowywany źródłowy</span><span class="sxs-lookup"><span data-stu-id="b421b-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="b421b-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="b421b-149">-SourceType</span></span>
<span data-ttu-id="b421b-150">Typ przekazanego źródła</span><span class="sxs-lookup"><span data-stu-id="b421b-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="b421b-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="b421b-151">-SourceVersion</span></span>
<span data-ttu-id="b421b-152">Wersja źródła</span><span class="sxs-lookup"><span data-stu-id="b421b-152">Version of the source</span></span>

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

### <span data-ttu-id="b421b-153">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b421b-153">-SubscriptionId</span></span>
<span data-ttu-id="b421b-154">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b421b-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b421b-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b421b-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b421b-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b421b-156">-Confirm</span></span>
<span data-ttu-id="b421b-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b421b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b421b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b421b-158">-WhatIf</span></span>
<span data-ttu-id="b421b-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b421b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b421b-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b421b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b421b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b421b-161">CommonParameters</span></span>
<span data-ttu-id="b421b-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b421b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b421b-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b421b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b421b-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b421b-164">INPUTS</span></span>

### <span data-ttu-id="b421b-165">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b421b-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b421b-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b421b-166">OUTPUTS</span></span>

### <span data-ttu-id="b421b-167">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="b421b-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="b421b-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b421b-168">NOTES</span></span>

<span data-ttu-id="b421b-169">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b421b-169">ALIASES</span></span>

<span data-ttu-id="b421b-170">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b421b-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b421b-171">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b421b-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b421b-172">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b421b-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b421b-173">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b421b-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b421b-174">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b421b-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b421b-175">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="b421b-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b421b-176">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b421b-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b421b-177">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b421b-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b421b-178">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="b421b-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b421b-179">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b421b-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b421b-180">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="b421b-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b421b-181">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b421b-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b421b-182">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b421b-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b421b-183">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="b421b-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b421b-184">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b421b-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b421b-185">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b421b-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b421b-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b421b-186">RELATED LINKS</span></span>

