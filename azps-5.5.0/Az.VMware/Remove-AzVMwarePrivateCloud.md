---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 76ad6df6dbbd9b019e4c89fdbca55107264f0406
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241578"
---
# <span data-ttu-id="e79cd-101">Remove-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="e79cd-101">Remove-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="e79cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e79cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e79cd-103">Usuwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-103">Delete a private cloud</span></span>

## <span data-ttu-id="e79cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e79cd-104">SYNTAX</span></span>

### <span data-ttu-id="e79cd-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="e79cd-105">Delete (Default)</span></span>
```
Remove-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e79cd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e79cd-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e79cd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e79cd-107">DESCRIPTION</span></span>
<span data-ttu-id="e79cd-108">Usuwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-108">Delete a private cloud</span></span>

## <span data-ttu-id="e79cd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e79cd-109">EXAMPLES</span></span>

### <span data-ttu-id="e79cd-110">Przykład 1. Usuwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="e79cd-111">Usuwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-111">Delete private cloud</span></span>

## <span data-ttu-id="e79cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e79cd-112">PARAMETERS</span></span>

### <span data-ttu-id="e79cd-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e79cd-113">-AsJob</span></span>
<span data-ttu-id="e79cd-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e79cd-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e79cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79cd-115">-DefaultProfile</span></span>
<span data-ttu-id="e79cd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e79cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e79cd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e79cd-117">-InputObject</span></span>
<span data-ttu-id="e79cd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e79cd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e79cd-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e79cd-119">-Name</span></span>
<span data-ttu-id="e79cd-120">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79cd-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e79cd-121">-NoWait</span></span>
<span data-ttu-id="e79cd-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e79cd-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e79cd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e79cd-123">-PassThru</span></span>
<span data-ttu-id="e79cd-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e79cd-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e79cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e79cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="e79cd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e79cd-126">The name of the resource group.</span></span>
<span data-ttu-id="e79cd-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e79cd-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e79cd-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e79cd-128">-SubscriptionId</span></span>
<span data-ttu-id="e79cd-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e79cd-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e79cd-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e79cd-130">-Confirm</span></span>
<span data-ttu-id="e79cd-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e79cd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e79cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e79cd-132">-WhatIf</span></span>
<span data-ttu-id="e79cd-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e79cd-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e79cd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e79cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79cd-135">CommonParameters</span></span>
<span data-ttu-id="e79cd-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e79cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79cd-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e79cd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79cd-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e79cd-138">INPUTS</span></span>

### <span data-ttu-id="e79cd-139">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity</span><span class="sxs-lookup"><span data-stu-id="e79cd-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="e79cd-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e79cd-140">OUTPUTS</span></span>

### <span data-ttu-id="e79cd-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e79cd-141">System.Boolean</span></span>

## <span data-ttu-id="e79cd-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e79cd-142">NOTES</span></span>

<span data-ttu-id="e79cd-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e79cd-143">ALIASES</span></span>

<span data-ttu-id="e79cd-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e79cd-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e79cd-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e79cd-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e79cd-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e79cd-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e79cd-147">INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e79cd-147">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e79cd-148">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e79cd-149">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e79cd-150">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e79cd-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e79cd-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e79cd-152">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e79cd-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e79cd-153">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e79cd-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e79cd-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e79cd-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e79cd-155">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e79cd-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="e79cd-156">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e79cd-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e79cd-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e79cd-157">RELATED LINKS</span></span>

