---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: b4b68f654c78da0dc2341966e3f9efaac397e504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955306"
---
# <span data-ttu-id="d503d-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="d503d-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="d503d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d503d-102">SYNOPSIS</span></span>
<span data-ttu-id="d503d-103">Uzyskaj wdrożenie i jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="d503d-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="d503d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d503d-104">SYNTAX</span></span>

### <span data-ttu-id="d503d-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d503d-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d503d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d503d-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d503d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d503d-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d503d-108">Lista</span><span class="sxs-lookup"><span data-stu-id="d503d-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d503d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d503d-109">DESCRIPTION</span></span>
<span data-ttu-id="d503d-110">Uzyskaj wdrożenie i jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="d503d-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="d503d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d503d-111">EXAMPLES</span></span>

### <span data-ttu-id="d503d-112">Przykład 1. Pobierz aplikację Spring Cloud Deploymeng według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d503d-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="d503d-113">Pobierz aplikację Spring Cloud Deploymeng według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d503d-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="d503d-114">Przykład 2. Lista wszystkich wdrożeń w ramach danej aplikacji w chmurze wiosną.</span><span class="sxs-lookup"><span data-stu-id="d503d-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="d503d-115">Lista wszystkich wdrożeń w ramach owej wiosennej aplikacji w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d503d-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="d503d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d503d-116">PARAMETERS</span></span>

### <span data-ttu-id="d503d-117">- AppName</span><span class="sxs-lookup"><span data-stu-id="d503d-117">-AppName</span></span>
<span data-ttu-id="d503d-118">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d503d-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="d503d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d503d-119">-DefaultProfile</span></span>
<span data-ttu-id="d503d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d503d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d503d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d503d-121">-InputObject</span></span>
<span data-ttu-id="d503d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d503d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d503d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d503d-123">-Name</span></span>
<span data-ttu-id="d503d-124">Nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d503d-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="d503d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d503d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d503d-126">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="d503d-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d503d-127">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d503d-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d503d-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d503d-128">-ServiceName</span></span>
<span data-ttu-id="d503d-129">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="d503d-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d503d-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d503d-130">-SubscriptionId</span></span>
<span data-ttu-id="d503d-131">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d503d-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d503d-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d503d-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d503d-133">— Wersja</span><span class="sxs-lookup"><span data-stu-id="d503d-133">-Version</span></span>
<span data-ttu-id="d503d-134">Wersja wdrożeń, które mają zostać wyświetlone</span><span class="sxs-lookup"><span data-stu-id="d503d-134">Version of the deployments to be listed</span></span>

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

### <span data-ttu-id="d503d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d503d-135">CommonParameters</span></span>
<span data-ttu-id="d503d-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d503d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d503d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d503d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d503d-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d503d-138">INPUTS</span></span>

### <span data-ttu-id="d503d-139">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d503d-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d503d-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d503d-140">OUTPUTS</span></span>

### <span data-ttu-id="d503d-141">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.Api200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="d503d-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="d503d-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d503d-142">NOTES</span></span>

<span data-ttu-id="d503d-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d503d-143">ALIASES</span></span>

<span data-ttu-id="d503d-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d503d-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d503d-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d503d-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d503d-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d503d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d503d-147">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d503d-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d503d-148">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d503d-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d503d-149">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="d503d-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d503d-150">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d503d-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d503d-151">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d503d-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d503d-152">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="d503d-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d503d-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d503d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d503d-154">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="d503d-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d503d-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="d503d-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d503d-156">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d503d-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d503d-157">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="d503d-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d503d-158">`[SubscriptionId <String>]`: otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d503d-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d503d-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d503d-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d503d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d503d-160">RELATED LINKS</span></span>

