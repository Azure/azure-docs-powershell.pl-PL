---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 186b93c23de78bddcfb88946fbd19becee8ae938
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955322"
---
# <span data-ttu-id="e1faa-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="e1faa-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="e1faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1faa-102">SYNOPSIS</span></span>
<span data-ttu-id="e1faa-103">Uzyskaj usługę i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="e1faa-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="e1faa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1faa-104">SYNTAX</span></span>

### <span data-ttu-id="e1faa-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e1faa-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1faa-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e1faa-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1faa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e1faa-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1faa-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="e1faa-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1faa-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1faa-109">DESCRIPTION</span></span>
<span data-ttu-id="e1faa-110">Uzyskaj usługę i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="e1faa-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="e1faa-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1faa-111">EXAMPLES</span></span>

### <span data-ttu-id="e1faa-112">Przykład 1. Uzyskiwanie usługi Spring Cloud Service według nazwy</span><span class="sxs-lookup"><span data-stu-id="e1faa-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="e1faa-113">Uzyskiwanie usługi Spring Cloud Według nazwy</span><span class="sxs-lookup"><span data-stu-id="e1faa-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="e1faa-114">Przykład 2. Lista wszystkich wiosennych usług w chmurze w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1faa-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="e1faa-115">Lista wszystkich wiosennych usług w chmurze w ramach grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1faa-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="e1faa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1faa-116">PARAMETERS</span></span>

### <span data-ttu-id="e1faa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1faa-117">-DefaultProfile</span></span>
<span data-ttu-id="e1faa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1faa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1faa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1faa-119">-InputObject</span></span>
<span data-ttu-id="e1faa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e1faa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e1faa-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e1faa-121">-Name</span></span>
<span data-ttu-id="e1faa-122">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="e1faa-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1faa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1faa-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1faa-124">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="e1faa-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e1faa-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="e1faa-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1faa-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1faa-126">-SubscriptionId</span></span>
<span data-ttu-id="e1faa-127">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e1faa-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e1faa-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e1faa-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e1faa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1faa-129">CommonParameters</span></span>
<span data-ttu-id="e1faa-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1faa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1faa-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1faa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1faa-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1faa-132">INPUTS</span></span>

### <span data-ttu-id="e1faa-133">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e1faa-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e1faa-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1faa-134">OUTPUTS</span></span>

### <span data-ttu-id="e1faa-135">Microsoft.Azure.PowerShell.cmdlet.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="e1faa-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="e1faa-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1faa-136">NOTES</span></span>

<span data-ttu-id="e1faa-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e1faa-137">ALIASES</span></span>

<span data-ttu-id="e1faa-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1faa-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1faa-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e1faa-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1faa-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1faa-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1faa-141">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e1faa-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e1faa-142">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1faa-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e1faa-143">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="e1faa-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e1faa-144">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e1faa-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e1faa-145">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="e1faa-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e1faa-146">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="e1faa-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e1faa-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e1faa-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1faa-148">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="e1faa-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e1faa-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="e1faa-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e1faa-150">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="e1faa-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e1faa-151">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="e1faa-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e1faa-152">`[SubscriptionId <String>]`: otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e1faa-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e1faa-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e1faa-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e1faa-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1faa-154">RELATED LINKS</span></span>

