---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222908"
---
# <span data-ttu-id="3caff-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="3caff-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="3caff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3caff-102">SYNOPSIS</span></span>
<span data-ttu-id="3caff-103">Pobierz wdrożenie i jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="3caff-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="3caff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3caff-104">SYNTAX</span></span>

### <span data-ttu-id="3caff-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3caff-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3caff-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3caff-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3caff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3caff-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3caff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3caff-108">DESCRIPTION</span></span>
<span data-ttu-id="3caff-109">Pobierz wdrożenie i jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="3caff-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="3caff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3caff-110">EXAMPLES</span></span>

### <span data-ttu-id="3caff-111">Przykład 1: Uzyskaj wiosenną aplikację w chmurze Deploymeng według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3caff-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="3caff-112">Uzyskaj wiosenną aplikację Deploymeng w chmurze według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="3caff-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="3caff-113">Przykład 2: wyświetlanie wszystkich wdrożeń w ramach danej aplikacji ze sprężyną chmurową.</span><span class="sxs-lookup"><span data-stu-id="3caff-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="3caff-114">Lista wszystkich wdrożeń w danej aplikacji ze sprężyną chmurową.</span><span class="sxs-lookup"><span data-stu-id="3caff-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="3caff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3caff-115">PARAMETERS</span></span>

### <span data-ttu-id="3caff-116">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="3caff-116">-AppName</span></span>
<span data-ttu-id="3caff-117">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3caff-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="3caff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caff-118">-DefaultProfile</span></span>
<span data-ttu-id="3caff-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3caff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3caff-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3caff-120">-InputObject</span></span>
<span data-ttu-id="3caff-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3caff-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3caff-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3caff-122">-Name</span></span>
<span data-ttu-id="3caff-123">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3caff-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="3caff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3caff-124">-ResourceGroupName</span></span>
<span data-ttu-id="3caff-125">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="3caff-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3caff-126">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3caff-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3caff-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3caff-127">-ServiceName</span></span>
<span data-ttu-id="3caff-128">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="3caff-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="3caff-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3caff-129">-SubscriptionId</span></span>
<span data-ttu-id="3caff-130">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3caff-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3caff-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3caff-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caff-132">-Version</span><span class="sxs-lookup"><span data-stu-id="3caff-132">-Version</span></span>
<span data-ttu-id="3caff-133">Wersje wdrożeń, które mają być wyświetlane</span><span class="sxs-lookup"><span data-stu-id="3caff-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caff-134">CommonParameters</span></span>
<span data-ttu-id="3caff-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3caff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caff-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3caff-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caff-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3caff-137">INPUTS</span></span>

### <span data-ttu-id="3caff-138">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="3caff-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="3caff-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3caff-139">OUTPUTS</span></span>

### <span data-ttu-id="3caff-140">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="3caff-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="3caff-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3caff-141">NOTES</span></span>

<span data-ttu-id="3caff-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3caff-142">ALIASES</span></span>

<span data-ttu-id="3caff-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3caff-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3caff-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3caff-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3caff-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3caff-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3caff-146">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3caff-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3caff-147">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3caff-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="3caff-148">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="3caff-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="3caff-149">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="3caff-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="3caff-150">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3caff-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="3caff-151">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="3caff-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="3caff-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3caff-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3caff-153">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="3caff-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="3caff-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="3caff-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3caff-155">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3caff-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3caff-156">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="3caff-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="3caff-157">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3caff-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3caff-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3caff-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3caff-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3caff-159">RELATED LINKS</span></span>

