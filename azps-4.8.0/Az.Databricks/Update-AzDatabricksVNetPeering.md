---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222598"
---
# <span data-ttu-id="84d69-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="84d69-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="84d69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84d69-102">SYNOPSIS</span></span>
<span data-ttu-id="84d69-103">Aktualizowanie komunikacji równorzędnej vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="84d69-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="84d69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84d69-104">SYNTAX</span></span>

### <span data-ttu-id="84d69-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84d69-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="84d69-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="84d69-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84d69-107">Opis</span><span class="sxs-lookup"><span data-stu-id="84d69-107">DESCRIPTION</span></span>
<span data-ttu-id="84d69-108">Aktualizowanie komunikacji równorzędnej vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="84d69-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="84d69-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84d69-109">EXAMPLES</span></span>

### <span data-ttu-id="84d69-110">Przykład 1: aktualizowanie AllowForwardedTraffic sieci równorzędnej VNET</span><span class="sxs-lookup"><span data-stu-id="84d69-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="84d69-111">To polecenie aktualizuje AllowForwardedTraffic komunikacji równorzędnej w sieci VNET.</span><span class="sxs-lookup"><span data-stu-id="84d69-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="84d69-112">Przykład 2: aktualizowanie AllowForwardedTraffic sieci równorzędnej wirtualnej przez obiekt</span><span class="sxs-lookup"><span data-stu-id="84d69-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="84d69-113">To polecenie aktualizuje AllowForwardedTraffic komunikacji równorzędnej wirtualnej przez obiekt.</span><span class="sxs-lookup"><span data-stu-id="84d69-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="84d69-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84d69-114">PARAMETERS</span></span>

### <span data-ttu-id="84d69-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="84d69-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="84d69-116">[System. Management. Automation. SwitchParameter] określa, czy ruch przekazywany z maszyn wirtualnych w lokalnej sieci wirtualnej będzie dozwolony/niedozwolony w zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84d69-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="84d69-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="84d69-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="84d69-118">[System. Management. Automation. SwitchParameter] Jeśli linki bramy mogą być używane w zdalnej wirtualnej sieci, aby połączyć się z tą siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="84d69-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="84d69-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="84d69-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="84d69-120">[System. Management. Automation. SwitchParameter] czy maszyny wirtualne w lokalnej wirtualnej przestrzeni sieciowej będą mogły uzyskiwać dostęp do maszyn wirtualnych w zdalnej przestrzeni wirtualnej sieci.</span><span class="sxs-lookup"><span data-stu-id="84d69-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="84d69-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84d69-121">-AsJob</span></span>
<span data-ttu-id="84d69-122">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="84d69-122">Run the command as a job</span></span>

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

### <span data-ttu-id="84d69-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d69-123">-DefaultProfile</span></span>
<span data-ttu-id="84d69-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84d69-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d69-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84d69-125">-InputObject</span></span>
<span data-ttu-id="84d69-126">Parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="84d69-126">Identity parameter.</span></span>
<span data-ttu-id="84d69-127">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="84d69-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="84d69-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84d69-128">-Name</span></span>
<span data-ttu-id="84d69-129">Nazwa VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="84d69-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="84d69-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="84d69-130">-NoWait</span></span>
<span data-ttu-id="84d69-131">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="84d69-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84d69-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d69-132">-ResourceGroupName</span></span>
<span data-ttu-id="84d69-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84d69-133">The name of the resource group.</span></span>
<span data-ttu-id="84d69-134">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="84d69-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="84d69-135">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="84d69-135">-SubscriptionId</span></span>
<span data-ttu-id="84d69-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="84d69-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="84d69-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="84d69-137">-UseRemoteGateway</span></span>
<span data-ttu-id="84d69-138">[System. Management. Automation. SwitchParameter] Jeśli bramy zdalne mogą być używane w tej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84d69-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="84d69-139">Jeśli flaga jest ustawiona na wartość true, a allowGatewayTransit w przypadku zdalnego komunikacji równorzędnej jest również prawdą, Sieć wirtualna będzie używać bramek zdalnej sieci wirtualnej do przesyłania.</span><span class="sxs-lookup"><span data-stu-id="84d69-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="84d69-140">Dla tej flagi może być ustawiona wartość prawda tylko jednej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="84d69-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="84d69-141">Nie można ustawić tej flagi, jeśli sieć wirtualna już ma bramę.</span><span class="sxs-lookup"><span data-stu-id="84d69-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="84d69-142">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="84d69-142">-WorkspaceName</span></span>
<span data-ttu-id="84d69-143">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="84d69-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="84d69-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84d69-144">-Confirm</span></span>
<span data-ttu-id="84d69-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d69-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d69-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d69-146">-WhatIf</span></span>
<span data-ttu-id="84d69-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d69-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d69-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84d69-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d69-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d69-149">CommonParameters</span></span>
<span data-ttu-id="84d69-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d69-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d69-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84d69-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d69-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84d69-152">INPUTS</span></span>

### <span data-ttu-id="84d69-153">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="84d69-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="84d69-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84d69-154">OUTPUTS</span></span>

### <span data-ttu-id="84d69-155">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="84d69-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="84d69-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84d69-156">NOTES</span></span>

<span data-ttu-id="84d69-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="84d69-157">ALIASES</span></span>

<span data-ttu-id="84d69-158">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84d69-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84d69-159">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="84d69-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84d69-160">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84d69-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84d69-161">INPUTobject <IDatabricksIdentity> : parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="84d69-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="84d69-162">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="84d69-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84d69-163">`[PeeringName <String>]`: Nazwa komunikacji równorzędnej w obszarze roboczym w sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="84d69-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="84d69-164">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84d69-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="84d69-165">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="84d69-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="84d69-166">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="84d69-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="84d69-167">`[WorkspaceName <String>]`: Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="84d69-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="84d69-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84d69-168">RELATED LINKS</span></span>

