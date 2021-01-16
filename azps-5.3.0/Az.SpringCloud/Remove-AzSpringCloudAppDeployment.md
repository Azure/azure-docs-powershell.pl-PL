---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375711"
---
# <span data-ttu-id="6d9e4-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="6d9e4-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="6d9e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9e4-103">Operacja usuwania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="6d9e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d9e4-104">SYNTAX</span></span>

### <span data-ttu-id="6d9e4-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6d9e4-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d9e4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d9e4-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d9e4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6d9e4-107">DESCRIPTION</span></span>
<span data-ttu-id="6d9e4-108">Operacja usuwania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="6d9e4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d9e4-109">EXAMPLES</span></span>

### <span data-ttu-id="6d9e4-110">Przykład 1: usuwanie rozmieszczenia wiosennego w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="6d9e4-111">Usuń wiosenną rozmieszczenie w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="6d9e4-112">Przykład 2: usuwanie ze swojego potoku wdrożenia w chmurze wiosennej.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="6d9e4-113">Usuń wiosnę ze sprężyny chmurowej z potoku.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="6d9e4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d9e4-114">PARAMETERS</span></span>

### <span data-ttu-id="6d9e4-115">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="6d9e4-115">-AppName</span></span>
<span data-ttu-id="6d9e4-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d9e4-117">-AsJob</span></span>
<span data-ttu-id="6d9e4-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6d9e4-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6d9e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9e4-119">-DefaultProfile</span></span>
<span data-ttu-id="6d9e4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9e4-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6d9e4-121">-InputObject</span></span>
<span data-ttu-id="6d9e4-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e4-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d9e4-123">-Name</span></span>
<span data-ttu-id="6d9e4-124">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e4-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6d9e4-125">-NoWait</span></span>
<span data-ttu-id="6d9e4-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6d9e4-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d9e4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d9e4-127">-PassThru</span></span>
<span data-ttu-id="6d9e4-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6d9e4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9e4-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d9e4-130">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d9e4-131">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e4-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6d9e4-132">-ServiceName</span></span>
<span data-ttu-id="6d9e4-133">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e4-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6d9e4-134">-SubscriptionId</span></span>
<span data-ttu-id="6d9e4-135">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d9e4-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e4-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d9e4-137">-Confirm</span></span>
<span data-ttu-id="6d9e4-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9e4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9e4-139">-WhatIf</span></span>
<span data-ttu-id="6d9e4-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d9e4-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9e4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9e4-142">CommonParameters</span></span>
<span data-ttu-id="6d9e4-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9e4-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d9e4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9e4-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d9e4-145">INPUTS</span></span>

### <span data-ttu-id="6d9e4-146">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="6d9e4-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="6d9e4-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d9e4-147">OUTPUTS</span></span>

### <span data-ttu-id="6d9e4-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d9e4-148">System.Boolean</span></span>

## <span data-ttu-id="6d9e4-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d9e4-149">NOTES</span></span>

<span data-ttu-id="6d9e4-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6d9e4-150">ALIASES</span></span>

<span data-ttu-id="6d9e4-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d9e4-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d9e4-152">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d9e4-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d9e4-154">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6d9e4-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d9e4-155">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="6d9e4-156">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="6d9e4-157">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="6d9e4-158">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="6d9e4-159">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="6d9e4-160">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6d9e4-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d9e4-161">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="6d9e4-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="6d9e4-162">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6d9e4-163">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6d9e4-164">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="6d9e4-165">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6d9e4-166">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d9e4-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d9e4-167">RELATED LINKS</span></span>

