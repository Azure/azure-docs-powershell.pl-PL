---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332593"
---
# <span data-ttu-id="1b16f-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="1b16f-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="1b16f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b16f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b16f-103">Operacja usuwania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1b16f-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="1b16f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b16f-104">SYNTAX</span></span>

### <span data-ttu-id="1b16f-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1b16f-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1b16f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1b16f-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b16f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1b16f-107">DESCRIPTION</span></span>
<span data-ttu-id="1b16f-108">Operacja usuwania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1b16f-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="1b16f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b16f-109">EXAMPLES</span></span>

### <span data-ttu-id="1b16f-110">Przykład 1: usuwanie rozmieszczenia wiosennego w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1b16f-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="1b16f-111">Usuń wiosenną rozmieszczenie w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1b16f-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="1b16f-112">Przykład 2: usuwanie ze swojego potoku wdrożenia w chmurze wiosennej.</span><span class="sxs-lookup"><span data-stu-id="1b16f-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="1b16f-113">Usuń wiosnę ze sprężyny chmurowej z potoku.</span><span class="sxs-lookup"><span data-stu-id="1b16f-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="1b16f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b16f-114">PARAMETERS</span></span>

### <span data-ttu-id="1b16f-115">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b16f-115">-AppName</span></span>
<span data-ttu-id="1b16f-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b16f-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="1b16f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b16f-117">-AsJob</span></span>
<span data-ttu-id="1b16f-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1b16f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1b16f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b16f-119">-DefaultProfile</span></span>
<span data-ttu-id="1b16f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b16f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b16f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1b16f-121">-InputObject</span></span>
<span data-ttu-id="1b16f-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1b16f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1b16f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b16f-123">-Name</span></span>
<span data-ttu-id="1b16f-124">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1b16f-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="1b16f-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1b16f-125">-NoWait</span></span>
<span data-ttu-id="1b16f-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1b16f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b16f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b16f-127">-PassThru</span></span>
<span data-ttu-id="1b16f-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="1b16f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1b16f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b16f-129">-ResourceGroupName</span></span>
<span data-ttu-id="1b16f-130">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="1b16f-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1b16f-131">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="1b16f-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1b16f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1b16f-132">-ServiceName</span></span>
<span data-ttu-id="1b16f-133">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="1b16f-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="1b16f-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1b16f-134">-SubscriptionId</span></span>
<span data-ttu-id="1b16f-135">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1b16f-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1b16f-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="1b16f-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1b16f-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b16f-137">-Confirm</span></span>
<span data-ttu-id="1b16f-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b16f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b16f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b16f-139">-WhatIf</span></span>
<span data-ttu-id="1b16f-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b16f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b16f-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b16f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b16f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b16f-142">CommonParameters</span></span>
<span data-ttu-id="1b16f-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b16f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b16f-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b16f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b16f-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b16f-145">INPUTS</span></span>

### <span data-ttu-id="1b16f-146">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="1b16f-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="1b16f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b16f-147">OUTPUTS</span></span>

### <span data-ttu-id="1b16f-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b16f-148">System.Boolean</span></span>

## <span data-ttu-id="1b16f-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b16f-149">NOTES</span></span>

<span data-ttu-id="1b16f-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1b16f-150">ALIASES</span></span>

<span data-ttu-id="1b16f-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b16f-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1b16f-152">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1b16f-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b16f-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1b16f-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1b16f-154">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1b16f-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b16f-155">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b16f-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="1b16f-156">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="1b16f-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="1b16f-157">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b16f-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="1b16f-158">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1b16f-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="1b16f-159">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="1b16f-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="1b16f-160">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1b16f-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b16f-161">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="1b16f-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="1b16f-162">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="1b16f-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1b16f-163">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="1b16f-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1b16f-164">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="1b16f-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="1b16f-165">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1b16f-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1b16f-166">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="1b16f-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1b16f-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b16f-167">RELATED LINKS</span></span>

