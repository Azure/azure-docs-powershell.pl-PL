---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064732"
---
# <span data-ttu-id="4c3ac-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="4c3ac-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="4c3ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3ac-103">Operacja usuwania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="4c3ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c3ac-104">SYNTAX</span></span>

### <span data-ttu-id="4c3ac-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4c3ac-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4c3ac-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4c3ac-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4c3ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4c3ac-107">DESCRIPTION</span></span>
<span data-ttu-id="4c3ac-108">Operacja usuwania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="4c3ac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c3ac-109">EXAMPLES</span></span>

### <span data-ttu-id="4c3ac-110">Przykład 1: usuwanie rozmieszczenia wiosennego w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="4c3ac-111">Usuń wiosenną rozmieszczenie w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="4c3ac-112">Przykład 2: usuwanie ze swojego potoku wdrożenia w chmurze wiosennej.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="4c3ac-113">Usuń wiosnę ze sprężyny chmurowej z potoku.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="4c3ac-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c3ac-114">PARAMETERS</span></span>

### <span data-ttu-id="4c3ac-115">-Nazwa_aplikacji</span><span class="sxs-lookup"><span data-stu-id="4c3ac-115">-AppName</span></span>
<span data-ttu-id="4c3ac-116">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="4c3ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3ac-117">-DefaultProfile</span></span>
<span data-ttu-id="4c3ac-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c3ac-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4c3ac-119">-InputObject</span></span>
<span data-ttu-id="4c3ac-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4c3ac-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c3ac-121">-Name</span></span>
<span data-ttu-id="4c3ac-122">Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-122">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="4c3ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c3ac-123">-PassThru</span></span>
<span data-ttu-id="4c3ac-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4c3ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c3ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c3ac-126">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4c3ac-127">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4c3ac-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4c3ac-128">-ServiceName</span></span>
<span data-ttu-id="4c3ac-129">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="4c3ac-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4c3ac-130">-SubscriptionId</span></span>
<span data-ttu-id="4c3ac-131">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4c3ac-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4c3ac-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c3ac-133">-Confirm</span></span>
<span data-ttu-id="4c3ac-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c3ac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c3ac-135">-WhatIf</span></span>
<span data-ttu-id="4c3ac-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c3ac-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c3ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3ac-138">CommonParameters</span></span>
<span data-ttu-id="4c3ac-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3ac-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c3ac-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3ac-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c3ac-141">INPUTS</span></span>

### <span data-ttu-id="4c3ac-142">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="4c3ac-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="4c3ac-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c3ac-143">OUTPUTS</span></span>

### <span data-ttu-id="4c3ac-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c3ac-144">System.Boolean</span></span>

## <span data-ttu-id="4c3ac-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c3ac-145">NOTES</span></span>

<span data-ttu-id="4c3ac-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4c3ac-146">ALIASES</span></span>

<span data-ttu-id="4c3ac-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c3ac-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4c3ac-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4c3ac-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4c3ac-150">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4c3ac-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4c3ac-151">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="4c3ac-152">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="4c3ac-153">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="4c3ac-154">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="4c3ac-155">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="4c3ac-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4c3ac-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4c3ac-157">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="4c3ac-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="4c3ac-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4c3ac-159">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4c3ac-160">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="4c3ac-161">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="4c3ac-162">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4c3ac-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4c3ac-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c3ac-163">RELATED LINKS</span></span>

