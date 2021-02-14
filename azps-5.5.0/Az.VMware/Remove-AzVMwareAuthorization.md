---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
ms.openlocfilehash: 39a6f251cd0cfb190ea8541f5b04c35d710de2c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197250"
---
# <span data-ttu-id="e38c1-101">Remove-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="e38c1-101">Remove-AzVMwareAuthorization</span></span>

## <span data-ttu-id="e38c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e38c1-103">Usuwanie autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e38c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e38c1-104">SYNTAX</span></span>

### <span data-ttu-id="e38c1-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="e38c1-105">Delete (Default)</span></span>
```
Remove-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e38c1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e38c1-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwareAuthorization -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e38c1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e38c1-107">DESCRIPTION</span></span>
<span data-ttu-id="e38c1-108">Usuwanie autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e38c1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e38c1-109">EXAMPLES</span></span>

### <span data-ttu-id="e38c1-110">Przykład 1. Usuwanie autoryzacji dla chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="e38c1-111">Usuwanie autoryzacji dla chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="e38c1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e38c1-112">PARAMETERS</span></span>

### <span data-ttu-id="e38c1-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e38c1-113">-AsJob</span></span>
<span data-ttu-id="e38c1-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e38c1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e38c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38c1-115">-DefaultProfile</span></span>
<span data-ttu-id="e38c1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e38c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e38c1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e38c1-117">-InputObject</span></span>
<span data-ttu-id="e38c1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e38c1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38c1-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e38c1-119">-Name</span></span>
<span data-ttu-id="e38c1-120">Nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="e38c1-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e38c1-121">-NoWait</span></span>
<span data-ttu-id="e38c1-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e38c1-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e38c1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e38c1-123">-PassThru</span></span>
<span data-ttu-id="e38c1-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e38c1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e38c1-125">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="e38c1-125">-PrivateCloudName</span></span>
<span data-ttu-id="e38c1-126">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="e38c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e38c1-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e38c1-128">The name of the resource group.</span></span>
<span data-ttu-id="e38c1-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e38c1-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e38c1-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e38c1-130">-SubscriptionId</span></span>
<span data-ttu-id="e38c1-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e38c1-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e38c1-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e38c1-132">-Confirm</span></span>
<span data-ttu-id="e38c1-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e38c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e38c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38c1-134">-WhatIf</span></span>
<span data-ttu-id="e38c1-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e38c1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38c1-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e38c1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e38c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38c1-137">CommonParameters</span></span>
<span data-ttu-id="e38c1-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38c1-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e38c1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38c1-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e38c1-140">INPUTS</span></span>

### <span data-ttu-id="e38c1-141">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity</span><span class="sxs-lookup"><span data-stu-id="e38c1-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="e38c1-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e38c1-142">OUTPUTS</span></span>

### <span data-ttu-id="e38c1-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e38c1-143">System.Boolean</span></span>

## <span data-ttu-id="e38c1-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e38c1-144">NOTES</span></span>

<span data-ttu-id="e38c1-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e38c1-145">ALIASES</span></span>

<span data-ttu-id="e38c1-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e38c1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e38c1-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e38c1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e38c1-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e38c1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e38c1-149">INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e38c1-149">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e38c1-150">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e38c1-151">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e38c1-152">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e38c1-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e38c1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e38c1-154">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e38c1-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e38c1-155">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e38c1-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e38c1-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e38c1-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e38c1-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e38c1-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="e38c1-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e38c1-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e38c1-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e38c1-159">RELATED LINKS</span></span>

