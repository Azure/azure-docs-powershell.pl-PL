---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198627"
---
# <span data-ttu-id="d8a61-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d8a61-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="d8a61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a61-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a61-103">Pobierz aplikację i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="d8a61-103">Get an App and its properties.</span></span>

## <span data-ttu-id="d8a61-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8a61-104">SYNTAX</span></span>

### <span data-ttu-id="d8a61-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d8a61-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8a61-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d8a61-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8a61-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8a61-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8a61-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8a61-108">DESCRIPTION</span></span>
<span data-ttu-id="d8a61-109">Pobierz aplikację i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="d8a61-109">Get an App and its properties.</span></span>

## <span data-ttu-id="d8a61-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8a61-110">EXAMPLES</span></span>

### <span data-ttu-id="d8a61-111">Przykład 1. Uzyskiwanie aplikacji Spring Cloud według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d8a61-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
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

<span data-ttu-id="d8a61-112">Pobierz aplikację Spring Cloud według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d8a61-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="d8a61-113">Przykład 2. Lista wszystkich aplikacji w ramach danej wiosennej usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d8a61-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="d8a61-114">Lista wszystkich aplikacji w ramach danej wiosennej usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d8a61-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="d8a61-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8a61-115">PARAMETERS</span></span>

### <span data-ttu-id="d8a61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a61-116">-DefaultProfile</span></span>
<span data-ttu-id="d8a61-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8a61-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8a61-118">-InputObject</span></span>
<span data-ttu-id="d8a61-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d8a61-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8a61-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8a61-120">-Name</span></span>
<span data-ttu-id="d8a61-121">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d8a61-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a61-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8a61-123">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="d8a61-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d8a61-124">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d8a61-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d8a61-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d8a61-125">-ServiceName</span></span>
<span data-ttu-id="d8a61-126">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="d8a61-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d8a61-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8a61-127">-SubscriptionId</span></span>
<span data-ttu-id="d8a61-128">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a61-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8a61-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d8a61-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d8a61-130">- SyncStatus</span><span class="sxs-lookup"><span data-stu-id="d8a61-130">-SyncStatus</span></span>
<span data-ttu-id="d8a61-131">Wskazuje, czy stan synchronizacji</span><span class="sxs-lookup"><span data-stu-id="d8a61-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a61-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a61-132">CommonParameters</span></span>
<span data-ttu-id="d8a61-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a61-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a61-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8a61-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a61-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8a61-135">INPUTS</span></span>

### <span data-ttu-id="d8a61-136">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d8a61-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d8a61-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8a61-137">OUTPUTS</span></span>

### <span data-ttu-id="d8a61-138">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="d8a61-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="d8a61-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8a61-139">NOTES</span></span>

<span data-ttu-id="d8a61-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d8a61-140">ALIASES</span></span>

<span data-ttu-id="d8a61-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8a61-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8a61-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d8a61-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8a61-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8a61-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8a61-144">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d8a61-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8a61-145">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d8a61-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d8a61-146">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="d8a61-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d8a61-147">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d8a61-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d8a61-148">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d8a61-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d8a61-149">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="d8a61-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d8a61-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d8a61-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8a61-151">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="d8a61-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d8a61-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="d8a61-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d8a61-153">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d8a61-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d8a61-154">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="d8a61-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d8a61-155">`[SubscriptionId <String>]`: otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a61-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d8a61-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d8a61-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d8a61-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8a61-157">RELATED LINKS</span></span>

