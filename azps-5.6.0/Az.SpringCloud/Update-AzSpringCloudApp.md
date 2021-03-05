---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: 2ea144ec36830286919f9cb512ccec01008428a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005322"
---
# <span data-ttu-id="a41db-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="a41db-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="a41db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a41db-102">SYNOPSIS</span></span>
<span data-ttu-id="a41db-103">Operacja aktualizacji zamykanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a41db-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="a41db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a41db-104">SYNTAX</span></span>

### <span data-ttu-id="a41db-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a41db-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a41db-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a41db-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a41db-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a41db-107">DESCRIPTION</span></span>
<span data-ttu-id="a41db-108">Operacja aktualizacji zamykanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a41db-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="a41db-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a41db-109">EXAMPLES</span></span>

### <span data-ttu-id="a41db-110">Przykład 1. Aktualizowanie aplikacji Spring Cloud według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a41db-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="a41db-111">Zaktualizuj aplikację Spring Cloud według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a41db-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="a41db-112">Przykład 2. Aktualizowanie aplikacji Spring Cloud z potoku.</span><span class="sxs-lookup"><span data-stu-id="a41db-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="a41db-113">Zaktualizuj aplikację Spring Cloud z potoku.</span><span class="sxs-lookup"><span data-stu-id="a41db-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="a41db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a41db-114">PARAMETERS</span></span>

### <span data-ttu-id="a41db-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="a41db-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="a41db-116">Nazwa aktywnego wdrożenia aplikacji</span><span class="sxs-lookup"><span data-stu-id="a41db-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="a41db-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a41db-117">-AsJob</span></span>
<span data-ttu-id="a41db-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a41db-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a41db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a41db-119">-DefaultProfile</span></span>
<span data-ttu-id="a41db-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a41db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a41db-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="a41db-121">-Fqdn</span></span>
<span data-ttu-id="a41db-122">W pełni kwalifikowana nazwa DNS.</span><span class="sxs-lookup"><span data-stu-id="a41db-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="a41db-123">—httpsOnly</span><span class="sxs-lookup"><span data-stu-id="a41db-123">-HttpsOnly</span></span>
<span data-ttu-id="a41db-124">Wskaż, czy jest dozwolone tylko https.</span><span class="sxs-lookup"><span data-stu-id="a41db-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="a41db-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a41db-125">-InputObject</span></span>
<span data-ttu-id="a41db-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a41db-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a41db-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a41db-127">-Location</span></span>
<span data-ttu-id="a41db-128">Lokalizacja GEOGRAFICZNA aplikacji, zawsze taka sama w przypadku jej zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="a41db-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="a41db-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a41db-129">-Name</span></span>
<span data-ttu-id="a41db-130">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a41db-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a41db-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a41db-131">-NoWait</span></span>
<span data-ttu-id="a41db-132">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a41db-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a41db-133">-PersistentMountPath</span><span class="sxs-lookup"><span data-stu-id="a41db-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="a41db-134">Ścieżka instalacji dysku trwałego</span><span class="sxs-lookup"><span data-stu-id="a41db-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="a41db-135">-PersistentSizeInGb</span><span class="sxs-lookup"><span data-stu-id="a41db-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="a41db-136">Rozmiar dysku trwałego w GB</span><span class="sxs-lookup"><span data-stu-id="a41db-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="a41db-137">— publiczna</span><span class="sxs-lookup"><span data-stu-id="a41db-137">-Public</span></span>
<span data-ttu-id="a41db-138">Wskazuje, czy aplikacja udostępnia publiczny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="a41db-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="a41db-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a41db-139">-ResourceGroupName</span></span>
<span data-ttu-id="a41db-140">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="a41db-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a41db-141">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a41db-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a41db-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a41db-142">-ServiceName</span></span>
<span data-ttu-id="a41db-143">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="a41db-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="a41db-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a41db-144">-SubscriptionId</span></span>
<span data-ttu-id="a41db-145">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a41db-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a41db-146">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="a41db-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a41db-147">-TemporaryMountPath</span><span class="sxs-lookup"><span data-stu-id="a41db-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="a41db-148">Ścieżka instalacji dysku tymczasowego</span><span class="sxs-lookup"><span data-stu-id="a41db-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="a41db-149">-TemporarySizeInGb</span><span class="sxs-lookup"><span data-stu-id="a41db-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="a41db-150">Rozmiar dysku tymczasowego w GB</span><span class="sxs-lookup"><span data-stu-id="a41db-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="a41db-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a41db-151">-Confirm</span></span>
<span data-ttu-id="a41db-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a41db-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a41db-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a41db-153">-WhatIf</span></span>
<span data-ttu-id="a41db-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a41db-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a41db-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a41db-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a41db-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a41db-156">CommonParameters</span></span>
<span data-ttu-id="a41db-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a41db-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a41db-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a41db-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a41db-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a41db-159">INPUTS</span></span>

### <span data-ttu-id="a41db-160">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a41db-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a41db-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a41db-161">OUTPUTS</span></span>

### <span data-ttu-id="a41db-162">Microsoft.Azure.PowerShell.cmdlet.SpringCloud.Models.Api200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="a41db-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="a41db-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a41db-163">NOTES</span></span>

<span data-ttu-id="a41db-164">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a41db-164">ALIASES</span></span>

<span data-ttu-id="a41db-165">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a41db-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a41db-166">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a41db-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a41db-167">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a41db-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a41db-168">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="a41db-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a41db-169">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a41db-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a41db-170">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="a41db-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a41db-171">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a41db-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a41db-172">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a41db-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a41db-173">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="a41db-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a41db-174">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a41db-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a41db-175">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="a41db-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a41db-176">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="a41db-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a41db-177">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a41db-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a41db-178">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="a41db-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a41db-179">`[SubscriptionId <String>]`: otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a41db-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a41db-180">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="a41db-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a41db-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a41db-181">RELATED LINKS</span></span>

