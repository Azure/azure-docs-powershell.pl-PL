---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183395"
---
# <span data-ttu-id="07b32-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="07b32-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="07b32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b32-102">SYNOPSIS</span></span>
<span data-ttu-id="07b32-103">Utwórz nową aplikację lub zaktualizuj aplikację wy wychodzącą.</span><span class="sxs-lookup"><span data-stu-id="07b32-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="07b32-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07b32-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07b32-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="07b32-105">DESCRIPTION</span></span>
<span data-ttu-id="07b32-106">Utwórz nową aplikację lub zaktualizuj aplikację wy wychodzącą.</span><span class="sxs-lookup"><span data-stu-id="07b32-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="07b32-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07b32-107">EXAMPLES</span></span>

### <span data-ttu-id="07b32-108">Przykład 1. Tworzenie wiosennej aplikacji w chmurze.</span><span class="sxs-lookup"><span data-stu-id="07b32-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
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

<span data-ttu-id="07b32-109">Utwórz wiosenną aplikację w chmurze.</span><span class="sxs-lookup"><span data-stu-id="07b32-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="07b32-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07b32-110">PARAMETERS</span></span>

### <span data-ttu-id="07b32-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="07b32-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="07b32-112">Nazwa aktywnego wdrożenia aplikacji</span><span class="sxs-lookup"><span data-stu-id="07b32-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="07b32-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="07b32-113">-AsJob</span></span>
<span data-ttu-id="07b32-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="07b32-114">Run the command as a job</span></span>

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

### <span data-ttu-id="07b32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b32-115">-DefaultProfile</span></span>
<span data-ttu-id="07b32-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="07b32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b32-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="07b32-117">-Fqdn</span></span>
<span data-ttu-id="07b32-118">W pełni kwalifikowana nazwa DNS.</span><span class="sxs-lookup"><span data-stu-id="07b32-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="07b32-119">—httpsOnly</span><span class="sxs-lookup"><span data-stu-id="07b32-119">-HttpsOnly</span></span>
<span data-ttu-id="07b32-120">Wskaż, czy jest dozwolone tylko https.</span><span class="sxs-lookup"><span data-stu-id="07b32-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="07b32-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="07b32-121">-Location</span></span>
<span data-ttu-id="07b32-122">Lokalizacja GEOGRAFICZNA aplikacji, zawsze taka sama w przypadku jej zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="07b32-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="07b32-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="07b32-123">-Name</span></span>
<span data-ttu-id="07b32-124">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="07b32-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b32-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="07b32-125">-NoWait</span></span>
<span data-ttu-id="07b32-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="07b32-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="07b32-127">-PersistentMountPath</span><span class="sxs-lookup"><span data-stu-id="07b32-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="07b32-128">Ścieżka instalacji dysku trwałego</span><span class="sxs-lookup"><span data-stu-id="07b32-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="07b32-129">-PersistentSizeInGb</span><span class="sxs-lookup"><span data-stu-id="07b32-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="07b32-130">Rozmiar dysku trwałego w GB</span><span class="sxs-lookup"><span data-stu-id="07b32-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="07b32-131">— publiczna</span><span class="sxs-lookup"><span data-stu-id="07b32-131">-Public</span></span>
<span data-ttu-id="07b32-132">Wskazuje, czy aplikacja udostępnia publiczny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="07b32-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="07b32-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b32-133">-ResourceGroupName</span></span>
<span data-ttu-id="07b32-134">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="07b32-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="07b32-135">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="07b32-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="07b32-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="07b32-136">-ServiceName</span></span>
<span data-ttu-id="07b32-137">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="07b32-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="07b32-138">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07b32-138">-SubscriptionId</span></span>
<span data-ttu-id="07b32-139">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="07b32-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="07b32-140">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="07b32-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="07b32-141">-TemporaryMountPath</span><span class="sxs-lookup"><span data-stu-id="07b32-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="07b32-142">Ścieżka do instalacji dysku tymczasowego</span><span class="sxs-lookup"><span data-stu-id="07b32-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="07b32-143">-TemporarySizeInGb</span><span class="sxs-lookup"><span data-stu-id="07b32-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="07b32-144">Rozmiar dysku tymczasowego w GB</span><span class="sxs-lookup"><span data-stu-id="07b32-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="07b32-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07b32-145">-Confirm</span></span>
<span data-ttu-id="07b32-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="07b32-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b32-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b32-147">-WhatIf</span></span>
<span data-ttu-id="07b32-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07b32-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b32-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="07b32-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b32-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b32-150">CommonParameters</span></span>
<span data-ttu-id="07b32-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07b32-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b32-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07b32-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b32-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07b32-153">INPUTS</span></span>

## <span data-ttu-id="07b32-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07b32-154">OUTPUTS</span></span>

### <span data-ttu-id="07b32-155">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="07b32-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="07b32-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07b32-156">NOTES</span></span>

<span data-ttu-id="07b32-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="07b32-157">ALIASES</span></span>

## <span data-ttu-id="07b32-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07b32-158">RELATED LINKS</span></span>

