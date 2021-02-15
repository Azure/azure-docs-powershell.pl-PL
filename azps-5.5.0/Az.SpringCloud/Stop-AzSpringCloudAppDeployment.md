---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189002"
---
# <span data-ttu-id="b59ef-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="b59ef-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="b59ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b59ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b59ef-103">Zatrzymaj wdrażanie.</span><span class="sxs-lookup"><span data-stu-id="b59ef-103">Stop the deployment.</span></span>

## <span data-ttu-id="b59ef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b59ef-104">SYNTAX</span></span>

### <span data-ttu-id="b59ef-105">Zatrzymaj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b59ef-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b59ef-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b59ef-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b59ef-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b59ef-107">DESCRIPTION</span></span>
<span data-ttu-id="b59ef-108">Zatrzymaj wdrażanie.</span><span class="sxs-lookup"><span data-stu-id="b59ef-108">Stop the deployment.</span></span>

## <span data-ttu-id="b59ef-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b59ef-109">EXAMPLES</span></span>

### <span data-ttu-id="b59ef-110">Przykład 1. Zatrzymaj wiosenną usługę w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b59ef-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="b59ef-111">Zatrzymaj wiosenną usługę w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b59ef-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="b59ef-112">Przykład 2. Zatrzymanie wiosennej usługi w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="b59ef-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="b59ef-113">Zatrzymaj wiosenną usługę w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="b59ef-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="b59ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b59ef-114">PARAMETERS</span></span>

### <span data-ttu-id="b59ef-115">- AppName</span><span class="sxs-lookup"><span data-stu-id="b59ef-115">-AppName</span></span>
<span data-ttu-id="b59ef-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b59ef-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59ef-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b59ef-117">-AsJob</span></span>
<span data-ttu-id="b59ef-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b59ef-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b59ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59ef-119">-DefaultProfile</span></span>
<span data-ttu-id="b59ef-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b59ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b59ef-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b59ef-121">-InputObject</span></span>
<span data-ttu-id="b59ef-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b59ef-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b59ef-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b59ef-123">-Name</span></span>
<span data-ttu-id="b59ef-124">Nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="b59ef-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59ef-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b59ef-125">-NoWait</span></span>
<span data-ttu-id="b59ef-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b59ef-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b59ef-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b59ef-127">-PassThru</span></span>
<span data-ttu-id="b59ef-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b59ef-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b59ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b59ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="b59ef-130">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="b59ef-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b59ef-131">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b59ef-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59ef-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b59ef-132">-ServiceName</span></span>
<span data-ttu-id="b59ef-133">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="b59ef-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59ef-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b59ef-134">-SubscriptionId</span></span>
<span data-ttu-id="b59ef-135">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b59ef-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b59ef-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="b59ef-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59ef-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b59ef-137">-Confirm</span></span>
<span data-ttu-id="b59ef-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b59ef-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b59ef-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b59ef-139">-WhatIf</span></span>
<span data-ttu-id="b59ef-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b59ef-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b59ef-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b59ef-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b59ef-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59ef-142">CommonParameters</span></span>
<span data-ttu-id="b59ef-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59ef-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59ef-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b59ef-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59ef-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b59ef-145">INPUTS</span></span>

### <span data-ttu-id="b59ef-146">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b59ef-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b59ef-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b59ef-147">OUTPUTS</span></span>

### <span data-ttu-id="b59ef-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b59ef-148">System.Boolean</span></span>

## <span data-ttu-id="b59ef-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b59ef-149">NOTES</span></span>

<span data-ttu-id="b59ef-150">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b59ef-150">ALIASES</span></span>

<span data-ttu-id="b59ef-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b59ef-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b59ef-152">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b59ef-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b59ef-153">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b59ef-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b59ef-154">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b59ef-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b59ef-155">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b59ef-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b59ef-156">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="b59ef-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b59ef-157">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b59ef-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b59ef-158">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="b59ef-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b59ef-159">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="b59ef-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b59ef-160">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b59ef-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b59ef-161">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="b59ef-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b59ef-162">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="b59ef-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b59ef-163">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b59ef-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b59ef-164">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="b59ef-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b59ef-165">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b59ef-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b59ef-166">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="b59ef-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b59ef-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b59ef-167">RELATED LINKS</span></span>

