---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 1e5af469f92c07f7223ba95715bd32b22b4eb66f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222911"
---
# <span data-ttu-id="6b866-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="6b866-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="6b866-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b866-102">SYNOPSIS</span></span>
<span data-ttu-id="6b866-103">Pobierz aplikację i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="6b866-103">Get an App and its properties.</span></span>

## <span data-ttu-id="6b866-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b866-104">SYNTAX</span></span>

### <span data-ttu-id="6b866-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6b866-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b866-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6b866-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b866-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b866-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b866-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6b866-108">DESCRIPTION</span></span>
<span data-ttu-id="6b866-109">Pobierz aplikację i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="6b866-109">Get an App and its properties.</span></span>

## <span data-ttu-id="6b866-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b866-110">EXAMPLES</span></span>

### <span data-ttu-id="6b866-111">Przykład 1: Uzyskaj aplikację wiosennej chmury według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6b866-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="6b866-112">Uzyskaj aplikację wiosennej chmury według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6b866-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="6b866-113">Przykład 2: Wyświetlanie listy wszystkich aplikacji w ramach danej usługi w chmurze ze sprężyną.</span><span class="sxs-lookup"><span data-stu-id="6b866-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="6b866-114">Wyświetlanie listy wszystkich aplikacji w ramach danej usługi w chmurze ze sprężyną.</span><span class="sxs-lookup"><span data-stu-id="6b866-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="6b866-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b866-115">PARAMETERS</span></span>

### <span data-ttu-id="6b866-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b866-116">-DefaultProfile</span></span>
<span data-ttu-id="6b866-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b866-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b866-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b866-118">-InputObject</span></span>
<span data-ttu-id="6b866-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6b866-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b866-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b866-120">-Name</span></span>
<span data-ttu-id="6b866-121">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6b866-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="6b866-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b866-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b866-123">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="6b866-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6b866-124">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6b866-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6b866-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6b866-125">-ServiceName</span></span>
<span data-ttu-id="6b866-126">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="6b866-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="6b866-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6b866-127">-SubscriptionId</span></span>
<span data-ttu-id="6b866-128">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b866-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6b866-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6b866-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6b866-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="6b866-130">-SyncStatus</span></span>
<span data-ttu-id="6b866-131">Wskazuje, czy stan synchronizacji</span><span class="sxs-lookup"><span data-stu-id="6b866-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="6b866-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b866-132">CommonParameters</span></span>
<span data-ttu-id="6b866-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b866-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b866-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b866-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b866-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b866-135">INPUTS</span></span>

### <span data-ttu-id="6b866-136">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="6b866-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="6b866-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b866-137">OUTPUTS</span></span>

### <span data-ttu-id="6b866-138">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="6b866-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="6b866-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b866-139">NOTES</span></span>

<span data-ttu-id="6b866-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6b866-140">ALIASES</span></span>

<span data-ttu-id="6b866-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b866-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b866-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6b866-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b866-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b866-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b866-144">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6b866-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b866-145">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6b866-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="6b866-146">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="6b866-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="6b866-147">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6b866-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="6b866-148">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6b866-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="6b866-149">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="6b866-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="6b866-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6b866-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b866-151">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="6b866-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="6b866-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="6b866-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6b866-153">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6b866-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6b866-154">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="6b866-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="6b866-155">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b866-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6b866-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6b866-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6b866-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b866-157">RELATED LINKS</span></span>

