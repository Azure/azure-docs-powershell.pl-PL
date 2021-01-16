---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375720"
---
# <span data-ttu-id="5cb52-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="5cb52-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="5cb52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cb52-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb52-103">Operacja usuwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cb52-103">Operation to delete an App.</span></span>

## <span data-ttu-id="5cb52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cb52-104">SYNTAX</span></span>

### <span data-ttu-id="5cb52-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5cb52-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5cb52-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5cb52-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5cb52-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5cb52-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb52-108">Operacja usuwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cb52-108">Operation to delete an App.</span></span>

## <span data-ttu-id="5cb52-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cb52-109">EXAMPLES</span></span>

### <span data-ttu-id="5cb52-110">Przykład 1: Usuwanie aplikacji wiosennej w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="5cb52-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="5cb52-111">Usuń aplikację wiosennej chmury według nazwy.</span><span class="sxs-lookup"><span data-stu-id="5cb52-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="5cb52-112">Przykład 2: Usuwanie aplikacji wiosennej w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="5cb52-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="5cb52-113">Usuń aplikację wiosennej chmury z potoku.</span><span class="sxs-lookup"><span data-stu-id="5cb52-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="5cb52-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cb52-114">PARAMETERS</span></span>

### <span data-ttu-id="5cb52-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cb52-115">-AsJob</span></span>
<span data-ttu-id="5cb52-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5cb52-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5cb52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb52-117">-DefaultProfile</span></span>
<span data-ttu-id="5cb52-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cb52-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5cb52-119">-InputObject</span></span>
<span data-ttu-id="5cb52-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5cb52-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cb52-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5cb52-121">-Name</span></span>
<span data-ttu-id="5cb52-122">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cb52-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb52-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5cb52-123">-NoWait</span></span>
<span data-ttu-id="5cb52-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5cb52-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5cb52-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cb52-125">-PassThru</span></span>
<span data-ttu-id="5cb52-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="5cb52-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5cb52-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb52-127">-ResourceGroupName</span></span>
<span data-ttu-id="5cb52-128">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="5cb52-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5cb52-129">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="5cb52-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5cb52-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5cb52-130">-ServiceName</span></span>
<span data-ttu-id="5cb52-131">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="5cb52-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="5cb52-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5cb52-132">-SubscriptionId</span></span>
<span data-ttu-id="5cb52-133">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb52-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5cb52-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5cb52-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5cb52-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cb52-135">-Confirm</span></span>
<span data-ttu-id="5cb52-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cb52-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb52-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb52-137">-WhatIf</span></span>
<span data-ttu-id="5cb52-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cb52-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb52-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5cb52-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb52-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb52-140">CommonParameters</span></span>
<span data-ttu-id="5cb52-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb52-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb52-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cb52-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb52-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cb52-143">INPUTS</span></span>

### <span data-ttu-id="5cb52-144">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="5cb52-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="5cb52-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cb52-145">OUTPUTS</span></span>

### <span data-ttu-id="5cb52-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5cb52-146">System.Boolean</span></span>

## <span data-ttu-id="5cb52-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cb52-147">NOTES</span></span>

<span data-ttu-id="5cb52-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5cb52-148">ALIASES</span></span>

<span data-ttu-id="5cb52-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cb52-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cb52-150">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5cb52-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cb52-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cb52-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cb52-152">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="5cb52-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cb52-153">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cb52-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="5cb52-154">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="5cb52-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="5cb52-155">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5cb52-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="5cb52-156">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5cb52-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="5cb52-157">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="5cb52-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="5cb52-158">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5cb52-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cb52-159">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="5cb52-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="5cb52-160">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="5cb52-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5cb52-161">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="5cb52-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5cb52-162">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="5cb52-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="5cb52-163">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb52-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="5cb52-164">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5cb52-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5cb52-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cb52-165">RELATED LINKS</span></span>

