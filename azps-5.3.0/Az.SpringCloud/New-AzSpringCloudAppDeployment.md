---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501353"
---
# <span data-ttu-id="440e8-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="440e8-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="440e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="440e8-102">SYNOPSIS</span></span>
<span data-ttu-id="440e8-103">Utworzenie nowego wdrożenia lub zaktualizowanie wdrożenia kończącego.</span><span class="sxs-lookup"><span data-stu-id="440e8-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="440e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="440e8-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="440e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="440e8-105">DESCRIPTION</span></span>
<span data-ttu-id="440e8-106">Utworzenie nowego wdrożenia lub zaktualizowanie wdrożenia kończącego.</span><span class="sxs-lookup"><span data-stu-id="440e8-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="440e8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="440e8-107">EXAMPLES</span></span>

### <span data-ttu-id="440e8-108">Przykład 1: przykład 1: Tworzenie sprężynowego wdrożenia chmury.</span><span class="sxs-lookup"><span data-stu-id="440e8-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="440e8-109">Tworzenie sprężynowego wdrożenia chmury.</span><span class="sxs-lookup"><span data-stu-id="440e8-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="440e8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="440e8-110">PARAMETERS</span></span>

### <span data-ttu-id="440e8-111">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="440e8-111">-AppName</span></span>
<span data-ttu-id="440e8-112">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="440e8-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="440e8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="440e8-113">-AsJob</span></span>
<span data-ttu-id="440e8-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="440e8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="440e8-115">-Procesor</span><span class="sxs-lookup"><span data-stu-id="440e8-115">-Cpu</span></span>
<span data-ttu-id="440e8-116">Wymagany procesor</span><span class="sxs-lookup"><span data-stu-id="440e8-116">Required CPU</span></span>

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

### <span data-ttu-id="440e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440e8-117">-DefaultProfile</span></span>
<span data-ttu-id="440e8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="440e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="440e8-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="440e8-119">-EnvironmentVariable</span></span>
<span data-ttu-id="440e8-120">Kolekcja zmiennych środowiskowych</span><span class="sxs-lookup"><span data-stu-id="440e8-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="440e8-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="440e8-121">-JvmOption</span></span>
<span data-ttu-id="440e8-122">Parametr JVM</span><span class="sxs-lookup"><span data-stu-id="440e8-122">JVM parameter</span></span>

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

### <span data-ttu-id="440e8-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="440e8-123">-MemoryInGb</span></span>
<span data-ttu-id="440e8-124">Wymagany rozmiar pamięci w GB</span><span class="sxs-lookup"><span data-stu-id="440e8-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="440e8-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="440e8-125">-Name</span></span>
<span data-ttu-id="440e8-126">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="440e8-126">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="440e8-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="440e8-127">-NoWait</span></span>
<span data-ttu-id="440e8-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="440e8-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="440e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="440e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="440e8-130">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="440e8-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="440e8-131">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="440e8-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="440e8-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="440e8-132">-RuntimeVersion</span></span>
<span data-ttu-id="440e8-133">Wersja Runtime</span><span class="sxs-lookup"><span data-stu-id="440e8-133">Runtime version</span></span>

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

### <span data-ttu-id="440e8-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="440e8-134">-ServiceName</span></span>
<span data-ttu-id="440e8-135">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="440e8-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="440e8-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="440e8-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="440e8-137">Selektor dla artefaktu, który ma być wykorzystywany do wdrożenia projektów z wieloma modułami.</span><span class="sxs-lookup"><span data-stu-id="440e8-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="440e8-138">Powinno to Bethe względną ścieżkę do docelowego modułu/projektu.</span><span class="sxs-lookup"><span data-stu-id="440e8-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="440e8-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="440e8-139">-SourceRelativePath</span></span>
<span data-ttu-id="440e8-140">Ścieżka względna miejsca do magazynowania, w którym jest przechowywany źródłowy</span><span class="sxs-lookup"><span data-stu-id="440e8-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="440e8-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="440e8-141">-SourceType</span></span>
<span data-ttu-id="440e8-142">Typ przekazanego źródła</span><span class="sxs-lookup"><span data-stu-id="440e8-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="440e8-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="440e8-143">-SourceVersion</span></span>
<span data-ttu-id="440e8-144">Wersja źródła</span><span class="sxs-lookup"><span data-stu-id="440e8-144">Version of the source</span></span>

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

### <span data-ttu-id="440e8-145">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="440e8-145">-SubscriptionId</span></span>
<span data-ttu-id="440e8-146">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="440e8-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="440e8-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="440e8-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="440e8-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="440e8-148">-Confirm</span></span>
<span data-ttu-id="440e8-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="440e8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="440e8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440e8-150">-WhatIf</span></span>
<span data-ttu-id="440e8-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="440e8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="440e8-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="440e8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="440e8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440e8-153">CommonParameters</span></span>
<span data-ttu-id="440e8-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="440e8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440e8-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="440e8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440e8-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="440e8-156">INPUTS</span></span>

## <span data-ttu-id="440e8-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="440e8-157">OUTPUTS</span></span>

### <span data-ttu-id="440e8-158">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="440e8-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="440e8-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="440e8-159">NOTES</span></span>

<span data-ttu-id="440e8-160">PISUJE</span><span class="sxs-lookup"><span data-stu-id="440e8-160">ALIASES</span></span>

## <span data-ttu-id="440e8-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="440e8-161">RELATED LINKS</span></span>

