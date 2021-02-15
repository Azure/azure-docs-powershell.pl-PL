---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: cfe9a8aa16803433055eb0cec5993cedcbcb5874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182530"
---
# <span data-ttu-id="e181b-101">Update-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="e181b-101">Update-AzVMwareCluster</span></span>

## <span data-ttu-id="e181b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e181b-102">SYNOPSIS</span></span>
<span data-ttu-id="e181b-103">Aktualizowanie klastrów w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="e181b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e181b-104">SYNTAX</span></span>

### <span data-ttu-id="e181b-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e181b-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e181b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e181b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwareCluster -InputObject <IVMwareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e181b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e181b-107">DESCRIPTION</span></span>
<span data-ttu-id="e181b-108">Aktualizowanie klastrów w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="e181b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e181b-109">EXAMPLES</span></span>

### <span data-ttu-id="e181b-110">Przykład 1. Aktualizowanie rozmiaru klastrów według nazwy</span><span class="sxs-lookup"><span data-stu-id="e181b-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="e181b-111">Aktualizowanie rozmiaru klastrów według nazwy</span><span class="sxs-lookup"><span data-stu-id="e181b-111">Update cluster size by name</span></span>

### <span data-ttu-id="e181b-112">Przykład 2. Aktualizowanie rozmiaru klastrów według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="e181b-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMwareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="e181b-113">Aktualizowanie rozmiaru klastrów według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="e181b-113">Update cluster size by input object</span></span>

## <span data-ttu-id="e181b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e181b-114">PARAMETERS</span></span>

### <span data-ttu-id="e181b-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e181b-115">-AsJob</span></span>
<span data-ttu-id="e181b-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e181b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e181b-117">- ClusterSize</span><span class="sxs-lookup"><span data-stu-id="e181b-117">-ClusterSize</span></span>
<span data-ttu-id="e181b-118">Rozmiar klastrów</span><span class="sxs-lookup"><span data-stu-id="e181b-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e181b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e181b-119">-DefaultProfile</span></span>
<span data-ttu-id="e181b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e181b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e181b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e181b-121">-InputObject</span></span>
<span data-ttu-id="e181b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e181b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e181b-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e181b-123">-Name</span></span>
<span data-ttu-id="e181b-124">Nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e181b-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e181b-125">-NoWait</span></span>
<span data-ttu-id="e181b-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e181b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e181b-127">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="e181b-127">-PrivateCloudName</span></span>
<span data-ttu-id="e181b-128">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e181b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e181b-129">-ResourceGroupName</span></span>
<span data-ttu-id="e181b-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e181b-130">The name of the resource group.</span></span>
<span data-ttu-id="e181b-131">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e181b-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e181b-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e181b-132">-SubscriptionId</span></span>
<span data-ttu-id="e181b-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e181b-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e181b-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e181b-134">-Confirm</span></span>
<span data-ttu-id="e181b-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e181b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e181b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e181b-136">-WhatIf</span></span>
<span data-ttu-id="e181b-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e181b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e181b-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e181b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e181b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e181b-139">CommonParameters</span></span>
<span data-ttu-id="e181b-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e181b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e181b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e181b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e181b-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e181b-142">INPUTS</span></span>

### <span data-ttu-id="e181b-143">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity</span><span class="sxs-lookup"><span data-stu-id="e181b-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="e181b-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e181b-144">OUTPUTS</span></span>

### <span data-ttu-id="e181b-145">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="e181b-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="e181b-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e181b-146">NOTES</span></span>

<span data-ttu-id="e181b-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e181b-147">ALIASES</span></span>

<span data-ttu-id="e181b-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e181b-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e181b-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e181b-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e181b-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e181b-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e181b-151">INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e181b-151">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e181b-152">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e181b-153">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e181b-154">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e181b-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e181b-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e181b-156">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e181b-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e181b-157">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e181b-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e181b-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e181b-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e181b-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e181b-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="e181b-160">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e181b-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e181b-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e181b-161">RELATED LINKS</span></span>

