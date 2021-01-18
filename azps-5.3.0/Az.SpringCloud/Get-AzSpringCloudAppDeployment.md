---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499881"
---
# <span data-ttu-id="f2f91-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="f2f91-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="f2f91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2f91-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f91-103">Pobierz wdrożenie i jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="f2f91-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="f2f91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2f91-104">SYNTAX</span></span>

### <span data-ttu-id="f2f91-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2f91-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2f91-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f2f91-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2f91-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2f91-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2f91-108">Lista</span><span class="sxs-lookup"><span data-stu-id="f2f91-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2f91-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f2f91-109">DESCRIPTION</span></span>
<span data-ttu-id="f2f91-110">Pobierz wdrożenie i jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="f2f91-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="f2f91-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2f91-111">EXAMPLES</span></span>

### <span data-ttu-id="f2f91-112">Przykład 1: Uzyskaj wiosenną aplikację w chmurze Deploymeng według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f2f91-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
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

<span data-ttu-id="f2f91-113">Uzyskaj wiosenną aplikację Deploymeng w chmurze według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="f2f91-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="f2f91-114">Przykład 2: wyświetlanie wszystkich wdrożeń w ramach danej aplikacji ze sprężyną chmurową.</span><span class="sxs-lookup"><span data-stu-id="f2f91-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="f2f91-115">Lista wszystkich wdrożeń w danej aplikacji ze sprężyną chmurową.</span><span class="sxs-lookup"><span data-stu-id="f2f91-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="f2f91-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2f91-116">PARAMETERS</span></span>

### <span data-ttu-id="f2f91-117">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="f2f91-117">-AppName</span></span>
<span data-ttu-id="f2f91-118">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2f91-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f91-119">-DefaultProfile</span></span>
<span data-ttu-id="f2f91-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f91-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f91-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f2f91-121">-InputObject</span></span>
<span data-ttu-id="f2f91-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f2f91-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f91-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2f91-123">-Name</span></span>
<span data-ttu-id="f2f91-124">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f2f91-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f91-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2f91-126">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="f2f91-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f2f91-127">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="f2f91-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f91-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f2f91-128">-ServiceName</span></span>
<span data-ttu-id="f2f91-129">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="f2f91-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f91-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f2f91-130">-SubscriptionId</span></span>
<span data-ttu-id="f2f91-131">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f91-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2f91-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f2f91-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f91-133">-Version</span><span class="sxs-lookup"><span data-stu-id="f2f91-133">-Version</span></span>
<span data-ttu-id="f2f91-134">Wersje wdrożeń, które mają być wyświetlane</span><span class="sxs-lookup"><span data-stu-id="f2f91-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f91-135">CommonParameters</span></span>
<span data-ttu-id="f2f91-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f91-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2f91-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f91-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2f91-138">INPUTS</span></span>

### <span data-ttu-id="f2f91-139">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="f2f91-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="f2f91-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2f91-140">OUTPUTS</span></span>

### <span data-ttu-id="f2f91-141">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="f2f91-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="f2f91-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2f91-142">NOTES</span></span>

<span data-ttu-id="f2f91-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f2f91-143">ALIASES</span></span>

<span data-ttu-id="f2f91-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2f91-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2f91-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f2f91-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2f91-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2f91-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2f91-147">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f2f91-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2f91-148">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2f91-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="f2f91-149">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="f2f91-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="f2f91-150">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f2f91-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="f2f91-151">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f2f91-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="f2f91-152">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="f2f91-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="f2f91-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f2f91-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2f91-154">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="f2f91-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="f2f91-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="f2f91-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f2f91-156">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="f2f91-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f2f91-157">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="f2f91-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="f2f91-158">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f91-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f2f91-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f2f91-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f2f91-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2f91-160">RELATED LINKS</span></span>

