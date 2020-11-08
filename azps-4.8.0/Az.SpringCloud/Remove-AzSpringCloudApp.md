---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222894"
---
# <span data-ttu-id="ae4f7-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="ae4f7-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="ae4f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4f7-103">Operacja usuwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-103">Operation to delete an App.</span></span>

## <span data-ttu-id="ae4f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae4f7-104">SYNTAX</span></span>

### <span data-ttu-id="ae4f7-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ae4f7-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ae4f7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ae4f7-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae4f7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ae4f7-107">DESCRIPTION</span></span>
<span data-ttu-id="ae4f7-108">Operacja usuwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-108">Operation to delete an App.</span></span>

## <span data-ttu-id="ae4f7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae4f7-109">EXAMPLES</span></span>

### <span data-ttu-id="ae4f7-110">Przykład 1: Usuwanie aplikacji wiosennej w chmurze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="ae4f7-111">Usuń aplikację wiosennej chmury według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="ae4f7-112">Przykład 2: Usuwanie aplikacji wiosennej w chmurze z potoku.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="ae4f7-113">Usuń aplikację wiosennej chmury z potoku.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="ae4f7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae4f7-114">PARAMETERS</span></span>

### <span data-ttu-id="ae4f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4f7-115">-DefaultProfile</span></span>
<span data-ttu-id="ae4f7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae4f7-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ae4f7-117">-InputObject</span></span>
<span data-ttu-id="ae4f7-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae4f7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae4f7-119">-Name</span></span>
<span data-ttu-id="ae4f7-120">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-120">The name of the App resource.</span></span>

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

### <span data-ttu-id="ae4f7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae4f7-121">-PassThru</span></span>
<span data-ttu-id="ae4f7-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ae4f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="ae4f7-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ae4f7-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ae4f7-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ae4f7-126">-ServiceName</span></span>
<span data-ttu-id="ae4f7-127">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="ae4f7-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ae4f7-128">-SubscriptionId</span></span>
<span data-ttu-id="ae4f7-129">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae4f7-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ae4f7-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae4f7-131">-Confirm</span></span>
<span data-ttu-id="ae4f7-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4f7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4f7-133">-WhatIf</span></span>
<span data-ttu-id="ae4f7-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae4f7-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4f7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4f7-136">CommonParameters</span></span>
<span data-ttu-id="ae4f7-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4f7-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae4f7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4f7-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae4f7-139">INPUTS</span></span>

### <span data-ttu-id="ae4f7-140">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ae4f7-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ae4f7-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae4f7-141">OUTPUTS</span></span>

### <span data-ttu-id="ae4f7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae4f7-142">System.Boolean</span></span>

## <span data-ttu-id="ae4f7-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae4f7-143">NOTES</span></span>

<span data-ttu-id="ae4f7-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ae4f7-144">ALIASES</span></span>

<span data-ttu-id="ae4f7-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae4f7-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae4f7-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae4f7-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae4f7-148">INPUTobject <ISpringCloudIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ae4f7-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae4f7-149">`[AppName <String>]`: Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ae4f7-150">`[BindingName <String>]`: Nazwa zasobu powiązania.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ae4f7-151">`[CertificateName <String>]`: Nazwa zasobu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ae4f7-152">`[DeploymentName <String>]`: Nazwa zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ae4f7-153">`[DomainName <String>]`: Nazwa niestandardowego zasobu domeny.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ae4f7-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ae4f7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae4f7-155">`[Location <String>]`: region</span><span class="sxs-lookup"><span data-stu-id="ae4f7-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ae4f7-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ae4f7-157">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ae4f7-158">`[ServiceName <String>]`: Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ae4f7-159">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ae4f7-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ae4f7-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ae4f7-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae4f7-161">RELATED LINKS</span></span>

