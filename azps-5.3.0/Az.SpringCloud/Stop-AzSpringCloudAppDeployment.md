---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375683"
---
# <span data-ttu-id="5c27a-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="5c27a-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="5c27a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c27a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c27a-103">Zatrzymywanie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5c27a-103">Stop the deployment.</span></span>

## <span data-ttu-id="5c27a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c27a-104">SYNTAX</span></span>

### <span data-ttu-id="5c27a-105">Zatrzymaj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5c27a-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5c27a-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5c27a-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5c27a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5c27a-107">DESCRIPTION</span></span>
<span data-ttu-id="5c27a-108">Zatrzymywanie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5c27a-108">Stop the deployment.</span></span>

## <span data-ttu-id="5c27a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c27a-109">EXAMPLES</span></span>

### <span data-ttu-id="5c27a-110">Przykład 1: zatrzymywanie wiosennej usługi w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="5c27a-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="5c27a-111">Zatrzymywanie wiosennej usługi w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="5c27a-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="5c27a-112">Przykład 2: zatrzymanie wiosennej usługi w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="5c27a-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="5c27a-113">Zatrzymywanie wiosennej usługi w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="5c27a-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="5c27a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c27a-114">PARAMETERS</span></span>

### <span data-ttu-id="5c27a-115">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c27a-115">-AppName</span></span>
<span data-ttu-id="5c27a-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c27a-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="5c27a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c27a-117">-AsJob</span></span>
<span data-ttu-id="5c27a-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5c27a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="5c27a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c27a-119">-DefaultProfile</span></span>
<span data-ttu-id="5c27a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c27a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c27a-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5c27a-121">-InputObject</span></span>
<span data-ttu-id="5c27a-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5c27a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5c27a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c27a-123">-Name</span></span>
<span data-ttu-id="5c27a-124">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5c27a-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="5c27a-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5c27a-125">-NoWait</span></span>
<span data-ttu-id="5c27a-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5c27a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5c27a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c27a-127">-PassThru</span></span>
<span data-ttu-id="5c27a-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="5c27a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5c27a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c27a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5c27a-130">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="5c27a-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5c27a-131">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="5c27a-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5c27a-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5c27a-132">-ServiceName</span></span>
<span data-ttu-id="5c27a-133">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="5c27a-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="5c27a-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5c27a-134">-SubscriptionId</span></span>
<span data-ttu-id="5c27a-135">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5c27a-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5c27a-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5c27a-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5c27a-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c27a-137">-Confirm</span></span>
<span data-ttu-id="5c27a-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c27a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c27a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c27a-139">-WhatIf</span></span>
<span data-ttu-id="5c27a-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c27a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c27a-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c27a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c27a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c27a-142">CommonParameters</span></span>
<span data-ttu-id="5c27a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c27a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c27a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c27a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c27a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c27a-145">INPUTS</span></span>

### <span data-ttu-id="5c27a-146">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="5c27a-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="5c27a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c27a-147">OUTPUTS</span></span>

### <span data-ttu-id="5c27a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c27a-148">System.Boolean</span></span>

## <span data-ttu-id="5c27a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c27a-149">NOTES</span></span>

<span data-ttu-id="5c27a-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5c27a-150">ALIASES</span></span>

<span data-ttu-id="5c27a-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c27a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c27a-152">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5c27a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c27a-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5c27a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c27a-154">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="5c27a-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c27a-155">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c27a-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="5c27a-156">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="5c27a-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="5c27a-157">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5c27a-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="5c27a-158">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5c27a-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="5c27a-159">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="5c27a-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="5c27a-160">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5c27a-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c27a-161">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="5c27a-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="5c27a-162">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="5c27a-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5c27a-163">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="5c27a-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5c27a-164">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="5c27a-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="5c27a-165">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5c27a-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="5c27a-166">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5c27a-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5c27a-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c27a-167">RELATED LINKS</span></span>

