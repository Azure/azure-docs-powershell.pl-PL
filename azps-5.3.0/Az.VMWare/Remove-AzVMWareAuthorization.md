---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498158"
---
# <span data-ttu-id="9a833-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="9a833-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="9a833-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a833-102">SYNOPSIS</span></span>
<span data-ttu-id="9a833-103">Usuwanie autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a833-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="9a833-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a833-104">SYNTAX</span></span>

### <span data-ttu-id="9a833-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9a833-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9a833-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a833-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a833-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9a833-107">DESCRIPTION</span></span>
<span data-ttu-id="9a833-108">Usuwanie autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a833-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="9a833-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a833-109">EXAMPLES</span></span>

### <span data-ttu-id="9a833-110">Przykład 1: usuwanie autoryzacji chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="9a833-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="9a833-111">Usuwanie autoryzacji chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="9a833-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="9a833-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a833-112">PARAMETERS</span></span>

### <span data-ttu-id="9a833-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a833-113">-AsJob</span></span>
<span data-ttu-id="9a833-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9a833-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9a833-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a833-115">-DefaultProfile</span></span>
<span data-ttu-id="9a833-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a833-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a833-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9a833-117">-InputObject</span></span>
<span data-ttu-id="9a833-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9a833-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a833-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a833-119">-Name</span></span>
<span data-ttu-id="9a833-120">Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a833-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a833-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9a833-121">-NoWait</span></span>
<span data-ttu-id="9a833-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9a833-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a833-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a833-123">-PassThru</span></span>
<span data-ttu-id="9a833-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="9a833-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9a833-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="9a833-125">-PrivateCloudName</span></span>
<span data-ttu-id="9a833-126">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="9a833-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="9a833-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a833-127">-ResourceGroupName</span></span>
<span data-ttu-id="9a833-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a833-128">The name of the resource group.</span></span>
<span data-ttu-id="9a833-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9a833-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9a833-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9a833-130">-SubscriptionId</span></span>
<span data-ttu-id="9a833-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9a833-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9a833-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a833-132">-Confirm</span></span>
<span data-ttu-id="9a833-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a833-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a833-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a833-134">-WhatIf</span></span>
<span data-ttu-id="9a833-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a833-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a833-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a833-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a833-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a833-137">CommonParameters</span></span>
<span data-ttu-id="9a833-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a833-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a833-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a833-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a833-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a833-140">INPUTS</span></span>

### <span data-ttu-id="9a833-141">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="9a833-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="9a833-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a833-142">OUTPUTS</span></span>

### <span data-ttu-id="9a833-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a833-143">System.Boolean</span></span>

## <span data-ttu-id="9a833-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a833-144">NOTES</span></span>

<span data-ttu-id="9a833-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9a833-145">ALIASES</span></span>

<span data-ttu-id="9a833-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a833-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a833-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9a833-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a833-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9a833-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a833-149">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9a833-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a833-150">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a833-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9a833-151">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a833-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9a833-152">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="9a833-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9a833-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9a833-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a833-154">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9a833-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9a833-155">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="9a833-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9a833-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a833-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9a833-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9a833-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="9a833-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9a833-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9a833-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a833-159">RELATED LINKS</span></span>

