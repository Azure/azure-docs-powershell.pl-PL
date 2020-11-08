---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224190"
---
# <span data-ttu-id="07b64-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="07b64-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="07b64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07b64-102">SYNOPSIS</span></span>
<span data-ttu-id="07b64-103">Operacja aktualizowania aplikacji kończącej się.</span><span class="sxs-lookup"><span data-stu-id="07b64-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="07b64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07b64-104">SYNTAX</span></span>

### <span data-ttu-id="07b64-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="07b64-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07b64-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="07b64-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07b64-107">Opis</span><span class="sxs-lookup"><span data-stu-id="07b64-107">DESCRIPTION</span></span>
<span data-ttu-id="07b64-108">Operacja aktualizowania aplikacji kończącej się.</span><span class="sxs-lookup"><span data-stu-id="07b64-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="07b64-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07b64-109">EXAMPLES</span></span>

### <span data-ttu-id="07b64-110">Przykład 1: Uaktualnij aplikację wiosennej chmury według nazwy.</span><span class="sxs-lookup"><span data-stu-id="07b64-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="07b64-111">Zaktualizuj aplikację wiosną chmurą według nazwy.</span><span class="sxs-lookup"><span data-stu-id="07b64-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="07b64-112">Przykład 2: Aktualizacja aplikacji wiosennej w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="07b64-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="07b64-113">Aktualizuj aplikację wiosennej chmury z potoku.</span><span class="sxs-lookup"><span data-stu-id="07b64-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="07b64-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07b64-114">PARAMETERS</span></span>

### <span data-ttu-id="07b64-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="07b64-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="07b64-116">Nazwa aktywnego wdrożenia aplikacji</span><span class="sxs-lookup"><span data-stu-id="07b64-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="07b64-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07b64-117">-AsJob</span></span>
<span data-ttu-id="07b64-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="07b64-118">Run the command as a job</span></span>

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

### <span data-ttu-id="07b64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b64-119">-DefaultProfile</span></span>
<span data-ttu-id="07b64-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="07b64-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b64-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="07b64-121">-Fqdn</span></span>
<span data-ttu-id="07b64-122">W pełni kwalifikowana nazwa DNS.</span><span class="sxs-lookup"><span data-stu-id="07b64-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="07b64-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="07b64-123">-HttpsOnly</span></span>
<span data-ttu-id="07b64-124">Wskazuje, czy dozwolony jest tylko protokół https.</span><span class="sxs-lookup"><span data-stu-id="07b64-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="07b64-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="07b64-125">-InputObject</span></span>
<span data-ttu-id="07b64-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="07b64-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="07b64-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="07b64-127">-Location</span></span>
<span data-ttu-id="07b64-128">Lokalizacja geograficzna aplikacji, zawsze taka sama, jak jej zasób nadrzędny</span><span class="sxs-lookup"><span data-stu-id="07b64-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="07b64-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="07b64-129">-Name</span></span>
<span data-ttu-id="07b64-130">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="07b64-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="07b64-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="07b64-131">-NoWait</span></span>
<span data-ttu-id="07b64-132">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="07b64-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="07b64-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="07b64-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="07b64-134">Ścieżka instalacji trwałego dysku</span><span class="sxs-lookup"><span data-stu-id="07b64-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="07b64-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="07b64-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="07b64-136">Rozmiar dysku trwałego w GB</span><span class="sxs-lookup"><span data-stu-id="07b64-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="07b64-137">-Public</span><span class="sxs-lookup"><span data-stu-id="07b64-137">-Public</span></span>
<span data-ttu-id="07b64-138">Wskazuje, czy aplikacja udostępnia publiczny punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="07b64-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="07b64-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b64-139">-ResourceGroupName</span></span>
<span data-ttu-id="07b64-140">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="07b64-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="07b64-141">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="07b64-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="07b64-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="07b64-142">-ServiceName</span></span>
<span data-ttu-id="07b64-143">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="07b64-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="07b64-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="07b64-144">-SubscriptionId</span></span>
<span data-ttu-id="07b64-145">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="07b64-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="07b64-146">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="07b64-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="07b64-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="07b64-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="07b64-148">Ścieżka instalacji dysku tymczasowego</span><span class="sxs-lookup"><span data-stu-id="07b64-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="07b64-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="07b64-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="07b64-150">Rozmiar dysku tymczasowego w GB</span><span class="sxs-lookup"><span data-stu-id="07b64-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="07b64-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07b64-151">-Confirm</span></span>
<span data-ttu-id="07b64-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07b64-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b64-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b64-153">-WhatIf</span></span>
<span data-ttu-id="07b64-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07b64-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b64-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07b64-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b64-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b64-156">CommonParameters</span></span>
<span data-ttu-id="07b64-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07b64-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b64-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07b64-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b64-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07b64-159">INPUTS</span></span>

### <span data-ttu-id="07b64-160">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="07b64-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="07b64-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07b64-161">OUTPUTS</span></span>

### <span data-ttu-id="07b64-162">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="07b64-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="07b64-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07b64-163">NOTES</span></span>

<span data-ttu-id="07b64-164">PISUJE</span><span class="sxs-lookup"><span data-stu-id="07b64-164">ALIASES</span></span>

<span data-ttu-id="07b64-165">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07b64-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07b64-166">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="07b64-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07b64-167">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07b64-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07b64-168">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="07b64-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07b64-169">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="07b64-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="07b64-170">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="07b64-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="07b64-171">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="07b64-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="07b64-172">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="07b64-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="07b64-173">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="07b64-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="07b64-174">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="07b64-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07b64-175">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="07b64-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="07b64-176">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="07b64-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="07b64-177">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="07b64-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="07b64-178">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="07b64-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="07b64-179">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="07b64-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="07b64-180">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="07b64-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="07b64-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07b64-181">RELATED LINKS</span></span>

