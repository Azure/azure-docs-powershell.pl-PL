---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: a331e083075d7ed5fa3f148bc405226d85ddc960
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010257"
---
# <span data-ttu-id="e249a-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="e249a-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="e249a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e249a-102">SYNOPSIS</span></span>
<span data-ttu-id="e249a-103">Utwórz nową usługę lub zaktualizuj usługę wy wychodzącą.</span><span class="sxs-lookup"><span data-stu-id="e249a-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="e249a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e249a-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e249a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e249a-105">DESCRIPTION</span></span>
<span data-ttu-id="e249a-106">Utwórz nową usługę lub zaktualizuj usługę wy wychodzącą.</span><span class="sxs-lookup"><span data-stu-id="e249a-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="e249a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e249a-107">EXAMPLES</span></span>

### <span data-ttu-id="e249a-108">Przykład 1. Tworzenie wiosennej usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="e249a-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="e249a-109">Utwórz wiosenną usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="e249a-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="e249a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e249a-110">PARAMETERS</span></span>

### <span data-ttu-id="e249a-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e249a-111">-AsJob</span></span>
<span data-ttu-id="e249a-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e249a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e249a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e249a-113">-DefaultProfile</span></span>
<span data-ttu-id="e249a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e249a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e249a-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="e249a-115">-GitPropertyUri</span></span>
<span data-ttu-id="e249a-116">URI repozytorium</span><span class="sxs-lookup"><span data-stu-id="e249a-116">URI of the repository</span></span>

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

### <span data-ttu-id="e249a-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e249a-117">-Location</span></span>
<span data-ttu-id="e249a-118">Lokalizacja GEOGRAFICZNA zasobu.</span><span class="sxs-lookup"><span data-stu-id="e249a-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="e249a-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e249a-119">-Name</span></span>
<span data-ttu-id="e249a-120">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="e249a-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e249a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e249a-121">-NoWait</span></span>
<span data-ttu-id="e249a-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e249a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e249a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e249a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e249a-124">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="e249a-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e249a-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="e249a-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e249a-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="e249a-126">-SkuName</span></span>
<span data-ttu-id="e249a-127">Nazwa sku</span><span class="sxs-lookup"><span data-stu-id="e249a-127">Name of the Sku</span></span>

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

### <span data-ttu-id="e249a-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e249a-128">-SkuTier</span></span>
<span data-ttu-id="e249a-129">Warstwa sku</span><span class="sxs-lookup"><span data-stu-id="e249a-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="e249a-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e249a-130">-SubscriptionId</span></span>
<span data-ttu-id="e249a-131">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e249a-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e249a-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e249a-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e249a-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="e249a-133">-Tag</span></span>
<span data-ttu-id="e249a-134">Tagi usługi, która jest listą kluczy par wartości opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="e249a-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="e249a-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="e249a-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="e249a-136">Target application insight instrumentation key</span><span class="sxs-lookup"><span data-stu-id="e249a-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="e249a-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="e249a-137">-TraceEnabled</span></span>
<span data-ttu-id="e249a-138">Wskazuje, czy można włączyć funkcję śledzenia.</span><span class="sxs-lookup"><span data-stu-id="e249a-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="e249a-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e249a-139">-Confirm</span></span>
<span data-ttu-id="e249a-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e249a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e249a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e249a-141">-WhatIf</span></span>
<span data-ttu-id="e249a-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e249a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e249a-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e249a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e249a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e249a-144">CommonParameters</span></span>
<span data-ttu-id="e249a-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e249a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e249a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e249a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e249a-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e249a-147">INPUTS</span></span>

## <span data-ttu-id="e249a-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e249a-148">OUTPUTS</span></span>

### <span data-ttu-id="e249a-149">Microsoft.Azure.PowerShell.cmdlet.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="e249a-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="e249a-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e249a-150">NOTES</span></span>

<span data-ttu-id="e249a-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e249a-151">ALIASES</span></span>

## <span data-ttu-id="e249a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e249a-152">RELATED LINKS</span></span>

