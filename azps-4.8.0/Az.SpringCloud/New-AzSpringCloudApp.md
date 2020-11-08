---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: 966a0c0243d8ca8cd982420a9a3018f9d41ab52e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222898"
---
# <span data-ttu-id="29f17-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="29f17-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="29f17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29f17-102">SYNOPSIS</span></span>
<span data-ttu-id="29f17-103">Utwórz nową aplikację lub zaktualizuj aplikację kończącą pracę.</span><span class="sxs-lookup"><span data-stu-id="29f17-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="29f17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29f17-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29f17-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29f17-105">DESCRIPTION</span></span>
<span data-ttu-id="29f17-106">Utwórz nową aplikację lub zaktualizuj aplikację kończącą pracę.</span><span class="sxs-lookup"><span data-stu-id="29f17-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="29f17-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29f17-107">EXAMPLES</span></span>

### <span data-ttu-id="29f17-108">Przykład 1: Tworzenie aplikacji wiosennej w chmurze.</span><span class="sxs-lookup"><span data-stu-id="29f17-108">Example 1: Create a spring cloud app.</span></span>
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

<span data-ttu-id="29f17-109">Utwórz wiosną aplikację w chmurze.</span><span class="sxs-lookup"><span data-stu-id="29f17-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="29f17-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29f17-110">PARAMETERS</span></span>

### <span data-ttu-id="29f17-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="29f17-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="29f17-112">Nazwa aktywnego wdrożenia aplikacji</span><span class="sxs-lookup"><span data-stu-id="29f17-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="29f17-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29f17-113">-AsJob</span></span>
<span data-ttu-id="29f17-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="29f17-114">Run the command as a job</span></span>

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

### <span data-ttu-id="29f17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f17-115">-DefaultProfile</span></span>
<span data-ttu-id="29f17-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29f17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29f17-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="29f17-117">-Fqdn</span></span>
<span data-ttu-id="29f17-118">W pełni kwalifikowana nazwa DNS.</span><span class="sxs-lookup"><span data-stu-id="29f17-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="29f17-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="29f17-119">-HttpsOnly</span></span>
<span data-ttu-id="29f17-120">Wskazuje, czy dozwolony jest tylko protokół https.</span><span class="sxs-lookup"><span data-stu-id="29f17-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="29f17-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="29f17-121">-Location</span></span>
<span data-ttu-id="29f17-122">Lokalizacja geograficzna aplikacji, zawsze taka sama, jak jej zasób nadrzędny</span><span class="sxs-lookup"><span data-stu-id="29f17-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="29f17-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29f17-123">-Name</span></span>
<span data-ttu-id="29f17-124">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="29f17-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="29f17-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="29f17-125">-NoWait</span></span>
<span data-ttu-id="29f17-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="29f17-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="29f17-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="29f17-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="29f17-128">Ścieżka instalacji trwałego dysku</span><span class="sxs-lookup"><span data-stu-id="29f17-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="29f17-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="29f17-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="29f17-130">Rozmiar dysku trwałego w GB</span><span class="sxs-lookup"><span data-stu-id="29f17-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="29f17-131">-Public</span><span class="sxs-lookup"><span data-stu-id="29f17-131">-Public</span></span>
<span data-ttu-id="29f17-132">Wskazuje, czy aplikacja udostępnia publiczny punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="29f17-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="29f17-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f17-133">-ResourceGroupName</span></span>
<span data-ttu-id="29f17-134">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="29f17-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="29f17-135">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="29f17-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="29f17-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="29f17-136">-ServiceName</span></span>
<span data-ttu-id="29f17-137">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="29f17-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="29f17-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="29f17-138">-SubscriptionId</span></span>
<span data-ttu-id="29f17-139">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="29f17-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="29f17-140">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="29f17-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="29f17-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="29f17-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="29f17-142">Ścieżka instalacji dysku tymczasowego</span><span class="sxs-lookup"><span data-stu-id="29f17-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="29f17-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="29f17-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="29f17-144">Rozmiar dysku tymczasowego w GB</span><span class="sxs-lookup"><span data-stu-id="29f17-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="29f17-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29f17-145">-Confirm</span></span>
<span data-ttu-id="29f17-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29f17-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29f17-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f17-147">-WhatIf</span></span>
<span data-ttu-id="29f17-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29f17-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f17-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29f17-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29f17-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f17-150">CommonParameters</span></span>
<span data-ttu-id="29f17-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f17-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f17-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29f17-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f17-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29f17-153">INPUTS</span></span>

## <span data-ttu-id="29f17-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29f17-154">OUTPUTS</span></span>

### <span data-ttu-id="29f17-155">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="29f17-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="29f17-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29f17-156">NOTES</span></span>

<span data-ttu-id="29f17-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="29f17-157">ALIASES</span></span>

## <span data-ttu-id="29f17-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29f17-158">RELATED LINKS</span></span>

