---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243827"
---
# <span data-ttu-id="c9525-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="c9525-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="c9525-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9525-102">SYNOPSIS</span></span>
<span data-ttu-id="c9525-103">Aktualizowanie komunikacji równorzędnej vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c9525-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="c9525-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9525-104">SYNTAX</span></span>

### <span data-ttu-id="c9525-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c9525-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c9525-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c9525-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c9525-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9525-107">DESCRIPTION</span></span>
<span data-ttu-id="c9525-108">Aktualizowanie komunikacji równorzędnej vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c9525-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="c9525-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9525-109">EXAMPLES</span></span>

### <span data-ttu-id="c9525-110">Przykład 1. Aktualizowanie allowForwardedTraffic komunikacji równorzędnej vnet</span><span class="sxs-lookup"><span data-stu-id="c9525-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="c9525-111">To polecenie aktualizuje polecenie AllowForwardedTraffic komunikacji równorzędnej w sieci vnet.</span><span class="sxs-lookup"><span data-stu-id="c9525-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="c9525-112">Przykład 2. Aktualizowanie właściwości AllowForwardedTraffic komunikacji równorzędnej w sieci vnet według obiektu</span><span class="sxs-lookup"><span data-stu-id="c9525-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="c9525-113">To polecenie aktualizuje obiekt allowForwardedTraffic komunikacji równorzędnej sieci vnet.</span><span class="sxs-lookup"><span data-stu-id="c9525-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="c9525-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9525-114">PARAMETERS</span></span>

### <span data-ttu-id="c9525-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="c9525-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="c9525-116">[System.Management.Automation.SwitchParameters] Czy ruch przesyłany dalej z maszyn wirtualnych w lokalnej sieci wirtualnej będzie dozwolony/zabronione w zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9525-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9525-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="c9525-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="c9525-118">[System.Management.Automation.SwitchParameters] Jeśli łącza bramy mogą być używane w zdalnej sieci wirtualnej do łączenia się z tą siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="c9525-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9525-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c9525-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="c9525-120">[System.Management.Automation.SwitchParameters] Czy maszyny wirtualne w lokalnym wirtualnym przestrzeni sieciowym będą mogły uzyskać dostęp do maszyn wirtualnych w zdalnym wirtualnym miejscu sieciowym.</span><span class="sxs-lookup"><span data-stu-id="c9525-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9525-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c9525-121">-AsJob</span></span>
<span data-ttu-id="c9525-122">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c9525-122">Run the command as a job</span></span>

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

### <span data-ttu-id="c9525-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9525-123">-DefaultProfile</span></span>
<span data-ttu-id="c9525-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9525-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9525-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9525-125">-InputObject</span></span>
<span data-ttu-id="c9525-126">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c9525-126">Identity parameter.</span></span>
<span data-ttu-id="c9525-127">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="c9525-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9525-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9525-128">-Name</span></span>
<span data-ttu-id="c9525-129">Nazwa VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="c9525-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9525-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c9525-130">-NoWait</span></span>
<span data-ttu-id="c9525-131">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c9525-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c9525-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9525-132">-ResourceGroupName</span></span>
<span data-ttu-id="c9525-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9525-133">The name of the resource group.</span></span>
<span data-ttu-id="c9525-134">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c9525-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c9525-135">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9525-135">-SubscriptionId</span></span>
<span data-ttu-id="c9525-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c9525-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c9525-137">— UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="c9525-137">-UseRemoteGateway</span></span>
<span data-ttu-id="c9525-138">[System.Management.Automation.SwitchParameters] Jeśli w tej sieci wirtualnej można używać bram zdalnych.</span><span class="sxs-lookup"><span data-stu-id="c9525-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="c9525-139">Jeśli flaga ma wartość True (Prawda), a funkcja allowGatewayTransit w zdalnej komunikacji równorzędnej również jest prawdziwa, do przesyłania w sieci wirtualnej będą używać bram zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9525-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="c9525-140">Tylko jedna komunikacja równorzędna może mieć ustawioną dla tej flagi wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="c9525-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="c9525-141">Tej flagi nie można ustawić, jeśli sieć wirtualna ma już bramę.</span><span class="sxs-lookup"><span data-stu-id="c9525-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9525-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9525-142">-WorkspaceName</span></span>
<span data-ttu-id="c9525-143">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c9525-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="c9525-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9525-144">-Confirm</span></span>
<span data-ttu-id="c9525-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9525-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9525-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9525-146">-WhatIf</span></span>
<span data-ttu-id="c9525-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9525-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9525-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9525-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9525-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9525-149">CommonParameters</span></span>
<span data-ttu-id="c9525-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9525-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9525-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9525-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9525-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9525-152">INPUTS</span></span>

### <span data-ttu-id="c9525-153">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="c9525-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="c9525-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9525-154">OUTPUTS</span></span>

### <span data-ttu-id="c9525-155">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9525-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="c9525-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9525-156">NOTES</span></span>

<span data-ttu-id="c9525-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c9525-157">ALIASES</span></span>

<span data-ttu-id="c9525-158">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c9525-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9525-159">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c9525-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9525-160">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9525-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9525-161">INPUTOBJECT: <IDatabricksIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c9525-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="c9525-162">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c9525-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9525-163">`[PeeringName <String>]`: nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c9525-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="c9525-164">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9525-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c9525-165">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c9525-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="c9525-166">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c9525-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c9525-167">`[WorkspaceName <String>]`: nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c9525-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="c9525-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9525-168">RELATED LINKS</span></span>

