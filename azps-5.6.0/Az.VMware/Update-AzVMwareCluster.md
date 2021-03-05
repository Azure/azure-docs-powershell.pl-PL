---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: f708d1b752c0d8106d7a8f9f7613fa74b6b19937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988590"
---
# <span data-ttu-id="5a949-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="5a949-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="5a949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a949-102">SYNOPSIS</span></span>
<span data-ttu-id="5a949-103">Aktualizowanie klastrów w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="5a949-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a949-104">SYNTAX</span></span>

### <span data-ttu-id="5a949-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="5a949-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a949-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5a949-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a949-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a949-107">DESCRIPTION</span></span>
<span data-ttu-id="5a949-108">Aktualizowanie klastrów w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="5a949-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a949-109">EXAMPLES</span></span>

### <span data-ttu-id="5a949-110">Przykład 1. Aktualizowanie rozmiaru klastrów według nazwy</span><span class="sxs-lookup"><span data-stu-id="5a949-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5a949-111">Aktualizowanie rozmiaru klastrów według nazwy</span><span class="sxs-lookup"><span data-stu-id="5a949-111">Update cluster size by name</span></span>

### <span data-ttu-id="5a949-112">Przykład 2. Aktualizowanie rozmiaru klastrów według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="5a949-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5a949-113">Aktualizowanie rozmiaru klastrów według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="5a949-113">Update cluster size by input object</span></span>

## <span data-ttu-id="5a949-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a949-114">PARAMETERS</span></span>

### <span data-ttu-id="5a949-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5a949-115">-AsJob</span></span>
<span data-ttu-id="5a949-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5a949-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5a949-117">- ClusterSize</span><span class="sxs-lookup"><span data-stu-id="5a949-117">-ClusterSize</span></span>
<span data-ttu-id="5a949-118">Rozmiar klastrów</span><span class="sxs-lookup"><span data-stu-id="5a949-118">The cluster size</span></span>

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

### <span data-ttu-id="5a949-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a949-119">-DefaultProfile</span></span>
<span data-ttu-id="5a949-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a949-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a949-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a949-121">-InputObject</span></span>
<span data-ttu-id="5a949-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5a949-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a949-123">-Name</span></span>
<span data-ttu-id="5a949-124">Nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="5a949-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a949-125">-NoWait</span></span>
<span data-ttu-id="5a949-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5a949-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5a949-127">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5a949-127">-PrivateCloudName</span></span>
<span data-ttu-id="5a949-128">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="5a949-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a949-129">-ResourceGroupName</span></span>
<span data-ttu-id="5a949-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a949-130">The name of the resource group.</span></span>
<span data-ttu-id="5a949-131">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="5a949-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5a949-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a949-132">-SubscriptionId</span></span>
<span data-ttu-id="5a949-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5a949-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5a949-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a949-134">-Confirm</span></span>
<span data-ttu-id="5a949-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a949-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a949-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a949-136">-WhatIf</span></span>
<span data-ttu-id="5a949-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a949-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a949-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a949-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a949-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a949-139">CommonParameters</span></span>
<span data-ttu-id="5a949-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a949-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a949-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a949-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a949-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a949-142">INPUTS</span></span>

### <span data-ttu-id="5a949-143">Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="5a949-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="5a949-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a949-144">OUTPUTS</span></span>

### <span data-ttu-id="5a949-145">Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="5a949-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="5a949-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a949-146">NOTES</span></span>

<span data-ttu-id="5a949-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5a949-147">ALIASES</span></span>

<span data-ttu-id="5a949-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a949-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a949-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5a949-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a949-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5a949-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a949-151">INPUTOBJECT: <IVMWareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="5a949-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a949-152">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="5a949-153">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="5a949-154">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="5a949-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5a949-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a949-156">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a949-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="5a949-157">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="5a949-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="5a949-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a949-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5a949-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="5a949-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="5a949-160">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5a949-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5a949-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a949-161">RELATED LINKS</span></span>

