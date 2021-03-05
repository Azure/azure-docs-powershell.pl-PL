---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: a569f605c139d5cd34c42ee1567989acebabbe61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962250"
---
# <span data-ttu-id="a1c95-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="a1c95-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="a1c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c95-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c95-103">Tworzy komunikacji równorzędne vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a1c95-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="a1c95-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1c95-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1c95-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1c95-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c95-106">Tworzy komunikacji równorzędne vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a1c95-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="a1c95-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1c95-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c95-108">Przykład 1. Tworzenie komunikacji równorzędnej w sieci VNET dla danychbricks</span><span class="sxs-lookup"><span data-stu-id="a1c95-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="a1c95-109">To polecenie tworzy dla danychbricks komunikacji równorzędnej w sieci VNET.</span><span class="sxs-lookup"><span data-stu-id="a1c95-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="a1c95-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1c95-110">PARAMETERS</span></span>

### <span data-ttu-id="a1c95-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="a1c95-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="a1c95-112">Czy ruch przesyłany dalej z maszyn wirtualnych w lokalnej sieci wirtualnej będzie dozwolony/zabronione w zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a1c95-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="a1c95-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="a1c95-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="a1c95-114">Jeśli łącza bramy mogą być używane w zdalnej sieci wirtualnej do łączenia się z tą siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="a1c95-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="a1c95-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a1c95-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="a1c95-116">Czy maszyny wirtualne w lokalnym wirtualnym przestrzeni sieciowym będą mogły uzyskać dostęp do maszyn wirtualnych w zdalnym wirtualnym przestrzeni sieciowym.</span><span class="sxs-lookup"><span data-stu-id="a1c95-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="a1c95-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a1c95-117">-AsJob</span></span>
<span data-ttu-id="a1c95-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a1c95-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a1c95-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="a1c95-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="a1c95-120">Lista bloków adresów zarezerwowanych dla tej sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="a1c95-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a1c95-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="a1c95-122">Identyfikator sieci wirtualnej databricks.</span><span class="sxs-lookup"><span data-stu-id="a1c95-122">The Id of the databricks virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c95-123">-DefaultProfile</span></span>
<span data-ttu-id="a1c95-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c95-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1c95-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1c95-125">-Name</span></span>
<span data-ttu-id="a1c95-126">Nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a1c95-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a1c95-127">-NoWait</span></span>
<span data-ttu-id="a1c95-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a1c95-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a1c95-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="a1c95-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="a1c95-130">Lista bloków adresów zarezerwowanych dla tej sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="a1c95-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a1c95-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="a1c95-132">Identyfikator zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a1c95-132">The Id of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c95-133">-ResourceGroupName</span></span>
<span data-ttu-id="a1c95-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1c95-134">The name of the resource group.</span></span>
<span data-ttu-id="a1c95-135">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="a1c95-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1c95-136">-SubscriptionId</span></span>
<span data-ttu-id="a1c95-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a1c95-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-138">— UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="a1c95-138">-UseRemoteGateway</span></span>
<span data-ttu-id="a1c95-139">Jeśli bram zdalnych można używać w tej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a1c95-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="a1c95-140">Jeśli flaga ma wartość True (Prawda), a funkcja allowGatewayTransit w zdalnej komunikacji równorzędnej również ma wartość True (Prawda), sieć wirtualna będzie używać bram zdalnej sieci wirtualnej do przesyłania.</span><span class="sxs-lookup"><span data-stu-id="a1c95-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="a1c95-141">Tylko jedna komunikacja równorzędna może mieć ustawioną dla tej flagi wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="a1c95-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="a1c95-142">Tej flagi nie można ustawić, jeśli sieć wirtualna ma już bramę.</span><span class="sxs-lookup"><span data-stu-id="a1c95-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="a1c95-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1c95-143">-WorkspaceName</span></span>
<span data-ttu-id="a1c95-144">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a1c95-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c95-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1c95-145">-Confirm</span></span>
<span data-ttu-id="a1c95-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1c95-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1c95-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c95-147">-WhatIf</span></span>
<span data-ttu-id="a1c95-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c95-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c95-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1c95-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1c95-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c95-150">CommonParameters</span></span>
<span data-ttu-id="a1c95-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c95-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c95-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1c95-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c95-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1c95-153">INPUTS</span></span>

## <span data-ttu-id="a1c95-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1c95-154">OUTPUTS</span></span>

### <span data-ttu-id="a1c95-155">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a1c95-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="a1c95-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1c95-156">NOTES</span></span>

<span data-ttu-id="a1c95-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a1c95-157">ALIASES</span></span>

## <span data-ttu-id="a1c95-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1c95-158">RELATED LINKS</span></span>

