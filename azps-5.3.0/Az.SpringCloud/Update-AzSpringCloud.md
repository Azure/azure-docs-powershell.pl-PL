---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375664"
---
# <span data-ttu-id="bea93-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="bea93-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="bea93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bea93-102">SYNOPSIS</span></span>
<span data-ttu-id="bea93-103">Operacja aktualizowania usługi kończącej pracę.</span><span class="sxs-lookup"><span data-stu-id="bea93-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="bea93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bea93-104">SYNTAX</span></span>

### <span data-ttu-id="bea93-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bea93-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bea93-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bea93-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bea93-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bea93-107">DESCRIPTION</span></span>
<span data-ttu-id="bea93-108">Operacja aktualizowania usługi kończącej pracę.</span><span class="sxs-lookup"><span data-stu-id="bea93-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="bea93-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bea93-109">EXAMPLES</span></span>

### <span data-ttu-id="bea93-110">Przykład 1: aktualizowanie usługi w chmurze wiosennej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="bea93-110">Example 1: Update Spring Cloud Service by name.</span></span>
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

<span data-ttu-id="bea93-111">Zaktualizuj usługę wiosennej chmury według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="bea93-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="bea93-112">Przykład 2: aktualizowanie usługi w chmurze wiosennej z potoku.</span><span class="sxs-lookup"><span data-stu-id="bea93-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
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

<span data-ttu-id="bea93-113">Aktualizuj usługę wiosennej chmury z potoku.</span><span class="sxs-lookup"><span data-stu-id="bea93-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="bea93-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bea93-114">PARAMETERS</span></span>

### <span data-ttu-id="bea93-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bea93-115">-AsJob</span></span>
<span data-ttu-id="bea93-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="bea93-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bea93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea93-117">-DefaultProfile</span></span>
<span data-ttu-id="bea93-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bea93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea93-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="bea93-119">-GitPropertyUri</span></span>
<span data-ttu-id="bea93-120">Identyfikator URI repozytorium</span><span class="sxs-lookup"><span data-stu-id="bea93-120">URI of the repository</span></span>

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

### <span data-ttu-id="bea93-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bea93-121">-InputObject</span></span>
<span data-ttu-id="bea93-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bea93-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bea93-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bea93-123">-Location</span></span>
<span data-ttu-id="bea93-124">Lokalizacja geograficzna zasobu.</span><span class="sxs-lookup"><span data-stu-id="bea93-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="bea93-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bea93-125">-Name</span></span>
<span data-ttu-id="bea93-126">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="bea93-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="bea93-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bea93-127">-NoWait</span></span>
<span data-ttu-id="bea93-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="bea93-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bea93-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea93-129">-ResourceGroupName</span></span>
<span data-ttu-id="bea93-130">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="bea93-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bea93-131">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="bea93-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bea93-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bea93-132">-SkuName</span></span>
<span data-ttu-id="bea93-133">Nazwa jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="bea93-133">Name of the Sku</span></span>

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

### <span data-ttu-id="bea93-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bea93-134">-SkuTier</span></span>
<span data-ttu-id="bea93-135">Warstwa jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="bea93-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="bea93-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bea93-136">-SubscriptionId</span></span>
<span data-ttu-id="bea93-137">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bea93-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bea93-138">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="bea93-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bea93-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="bea93-139">-Tag</span></span>
<span data-ttu-id="bea93-140">Tagi usługi, która jest listą par wartości klucza opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="bea93-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="bea93-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="bea93-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="bea93-142">Docelowy klucz Instrumentacji Application Insights</span><span class="sxs-lookup"><span data-stu-id="bea93-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="bea93-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="bea93-143">-TraceEnabled</span></span>
<span data-ttu-id="bea93-144">Wskazuje, czy włączyć funkcję śledzenia</span><span class="sxs-lookup"><span data-stu-id="bea93-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="bea93-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bea93-145">-Confirm</span></span>
<span data-ttu-id="bea93-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea93-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea93-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea93-147">-WhatIf</span></span>
<span data-ttu-id="bea93-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea93-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea93-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bea93-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea93-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea93-150">CommonParameters</span></span>
<span data-ttu-id="bea93-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea93-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea93-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bea93-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea93-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bea93-153">INPUTS</span></span>

### <span data-ttu-id="bea93-154">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="bea93-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="bea93-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bea93-155">OUTPUTS</span></span>

### <span data-ttu-id="bea93-156">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="bea93-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="bea93-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bea93-157">NOTES</span></span>

<span data-ttu-id="bea93-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="bea93-158">ALIASES</span></span>

<span data-ttu-id="bea93-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bea93-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bea93-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bea93-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bea93-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bea93-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bea93-162">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="bea93-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bea93-163">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bea93-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="bea93-164">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="bea93-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="bea93-165">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bea93-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="bea93-166">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="bea93-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="bea93-167">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="bea93-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="bea93-168">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bea93-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bea93-169">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="bea93-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="bea93-170">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="bea93-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bea93-171">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="bea93-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bea93-172">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="bea93-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="bea93-173">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bea93-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="bea93-174">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="bea93-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bea93-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bea93-175">RELATED LINKS</span></span>

