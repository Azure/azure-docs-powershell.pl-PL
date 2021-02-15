---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188986"
---
# <span data-ttu-id="ddfb8-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="ddfb8-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="ddfb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfb8-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfb8-103">Operation to update an exiting Service.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="ddfb8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddfb8-104">SYNTAX</span></span>

### <span data-ttu-id="ddfb8-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="ddfb8-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ddfb8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ddfb8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddfb8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddfb8-107">DESCRIPTION</span></span>
<span data-ttu-id="ddfb8-108">Operation to update an exiting Service.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="ddfb8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddfb8-109">EXAMPLES</span></span>

### <span data-ttu-id="ddfb8-110">Przykład 1. Aktualizowanie usługi Wiosna w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="ddfb8-111">Zaktualizuj usługę Spring Cloud według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="ddfb8-112">Przykład 2. Zaktualizuj wiosenną usługę w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
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

<span data-ttu-id="ddfb8-113">Zaktualizuj wiosenną usługę w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="ddfb8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddfb8-114">PARAMETERS</span></span>

### <span data-ttu-id="ddfb8-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ddfb8-115">-AsJob</span></span>
<span data-ttu-id="ddfb8-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ddfb8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ddfb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfb8-117">-DefaultProfile</span></span>
<span data-ttu-id="ddfb8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddfb8-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="ddfb8-119">-GitPropertyUri</span></span>
<span data-ttu-id="ddfb8-120">URI repozytorium</span><span class="sxs-lookup"><span data-stu-id="ddfb8-120">URI of the repository</span></span>

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

### <span data-ttu-id="ddfb8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddfb8-121">-InputObject</span></span>
<span data-ttu-id="ddfb8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ddfb8-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ddfb8-123">-Location</span></span>
<span data-ttu-id="ddfb8-124">Lokalizacja GEOGRAFICZNA zasobu.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="ddfb8-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddfb8-125">-Name</span></span>
<span data-ttu-id="ddfb8-126">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddfb8-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ddfb8-127">-NoWait</span></span>
<span data-ttu-id="ddfb8-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ddfb8-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ddfb8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddfb8-129">-ResourceGroupName</span></span>
<span data-ttu-id="ddfb8-130">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ddfb8-131">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ddfb8-132">-SKUName</span><span class="sxs-lookup"><span data-stu-id="ddfb8-132">-SkuName</span></span>
<span data-ttu-id="ddfb8-133">Nazwa sku</span><span class="sxs-lookup"><span data-stu-id="ddfb8-133">Name of the Sku</span></span>

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

### <span data-ttu-id="ddfb8-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ddfb8-134">-SkuTier</span></span>
<span data-ttu-id="ddfb8-135">Warstwa sku</span><span class="sxs-lookup"><span data-stu-id="ddfb8-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="ddfb8-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddfb8-136">-SubscriptionId</span></span>
<span data-ttu-id="ddfb8-137">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ddfb8-138">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ddfb8-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="ddfb8-139">-Tag</span></span>
<span data-ttu-id="ddfb8-140">Tagi usługi, która jest listą kluczy par wartości opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="ddfb8-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="ddfb8-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="ddfb8-142">Target application insight instrumentation key</span><span class="sxs-lookup"><span data-stu-id="ddfb8-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="ddfb8-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="ddfb8-143">-TraceEnabled</span></span>
<span data-ttu-id="ddfb8-144">Wskazuje, czy można włączyć funkcję śledzenia.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="ddfb8-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddfb8-145">-Confirm</span></span>
<span data-ttu-id="ddfb8-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddfb8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddfb8-147">-WhatIf</span></span>
<span data-ttu-id="ddfb8-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddfb8-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddfb8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfb8-150">CommonParameters</span></span>
<span data-ttu-id="ddfb8-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfb8-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddfb8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfb8-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddfb8-153">INPUTS</span></span>

### <span data-ttu-id="ddfb8-154">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ddfb8-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ddfb8-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddfb8-155">OUTPUTS</span></span>

### <span data-ttu-id="ddfb8-156">Microsoft.Azure.PowerShell.cmdlet.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="ddfb8-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="ddfb8-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddfb8-157">NOTES</span></span>

<span data-ttu-id="ddfb8-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ddfb8-158">ALIASES</span></span>

<span data-ttu-id="ddfb8-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ddfb8-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ddfb8-160">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ddfb8-161">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ddfb8-162">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ddfb8-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ddfb8-163">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ddfb8-164">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ddfb8-165">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ddfb8-166">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ddfb8-167">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ddfb8-168">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ddfb8-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ddfb8-169">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="ddfb8-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ddfb8-170">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ddfb8-171">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ddfb8-172">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ddfb8-173">`[SubscriptionId <String>]`: otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ddfb8-174">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ddfb8-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ddfb8-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddfb8-175">RELATED LINKS</span></span>

