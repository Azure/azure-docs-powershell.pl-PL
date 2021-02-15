---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197787"
---
# <span data-ttu-id="a67d2-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="a67d2-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="a67d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a67d2-103">Operacja usunięcia usługi.</span><span class="sxs-lookup"><span data-stu-id="a67d2-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="a67d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a67d2-104">SYNTAX</span></span>

### <span data-ttu-id="a67d2-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="a67d2-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a67d2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a67d2-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a67d2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a67d2-107">DESCRIPTION</span></span>
<span data-ttu-id="a67d2-108">Operacja usunięcia usługi.</span><span class="sxs-lookup"><span data-stu-id="a67d2-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="a67d2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a67d2-109">EXAMPLES</span></span>

### <span data-ttu-id="a67d2-110">Przykład 1. Usuwanie usługi Spring Cloud według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a67d2-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="a67d2-111">Usuń usługę Spring Cloud według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a67d2-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="a67d2-112">Przykład 2. Usuwanie usługi Spring Cloud z potoku.</span><span class="sxs-lookup"><span data-stu-id="a67d2-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="a67d2-113">Usuń usługę Spring Cloud z potoku.</span><span class="sxs-lookup"><span data-stu-id="a67d2-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="a67d2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a67d2-114">PARAMETERS</span></span>

### <span data-ttu-id="a67d2-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a67d2-115">-AsJob</span></span>
<span data-ttu-id="a67d2-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a67d2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a67d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67d2-117">-DefaultProfile</span></span>
<span data-ttu-id="a67d2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a67d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a67d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a67d2-119">-InputObject</span></span>
<span data-ttu-id="a67d2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a67d2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a67d2-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a67d2-121">-Name</span></span>
<span data-ttu-id="a67d2-122">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="a67d2-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a67d2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a67d2-123">-NoWait</span></span>
<span data-ttu-id="a67d2-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a67d2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a67d2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a67d2-125">-PassThru</span></span>
<span data-ttu-id="a67d2-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="a67d2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a67d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="a67d2-128">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="a67d2-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a67d2-129">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a67d2-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a67d2-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a67d2-130">-SubscriptionId</span></span>
<span data-ttu-id="a67d2-131">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a67d2-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a67d2-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="a67d2-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a67d2-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a67d2-133">-Confirm</span></span>
<span data-ttu-id="a67d2-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a67d2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67d2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67d2-135">-WhatIf</span></span>
<span data-ttu-id="a67d2-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67d2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a67d2-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a67d2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67d2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67d2-138">CommonParameters</span></span>
<span data-ttu-id="a67d2-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67d2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67d2-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a67d2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67d2-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a67d2-141">INPUTS</span></span>

### <span data-ttu-id="a67d2-142">Microsoft.Azure.PowerShell.Cmdlet.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a67d2-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a67d2-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a67d2-143">OUTPUTS</span></span>

### <span data-ttu-id="a67d2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a67d2-144">System.Boolean</span></span>

## <span data-ttu-id="a67d2-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a67d2-145">NOTES</span></span>

<span data-ttu-id="a67d2-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a67d2-146">ALIASES</span></span>

<span data-ttu-id="a67d2-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a67d2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a67d2-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a67d2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a67d2-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a67d2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a67d2-150">INPUTOBJECT: <ISpringCloudIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="a67d2-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a67d2-151">`[AppName <String>]`: nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a67d2-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a67d2-152">`[BindingName <String>]`: nazwa zasobu wiążącego.</span><span class="sxs-lookup"><span data-stu-id="a67d2-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a67d2-153">`[CertificateName <String>]`: nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a67d2-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a67d2-154">`[DeploymentName <String>]`: nazwa zasobu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a67d2-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a67d2-155">`[DomainName <String>]`: nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="a67d2-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a67d2-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a67d2-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a67d2-157">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="a67d2-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a67d2-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="a67d2-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a67d2-159">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a67d2-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a67d2-160">`[ServiceName <String>]`: nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="a67d2-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a67d2-161">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a67d2-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a67d2-162">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="a67d2-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a67d2-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a67d2-163">RELATED LINKS</span></span>

