---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238129"
---
# <span data-ttu-id="2ebcd-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="2ebcd-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="2ebcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ebcd-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebcd-103">Tworzy komunikacji równorzędne vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="2ebcd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ebcd-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ebcd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ebcd-105">DESCRIPTION</span></span>
<span data-ttu-id="2ebcd-106">Tworzy komunikacji równorzędne vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="2ebcd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ebcd-107">EXAMPLES</span></span>

### <span data-ttu-id="2ebcd-108">Przykład 1. Tworzenie komunikacji równorzędnej w sieci VNET dla danychbricks</span><span class="sxs-lookup"><span data-stu-id="2ebcd-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="2ebcd-109">To polecenie tworzy dla danychbricks komunikacji równorzędnej w sieci VNET.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="2ebcd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ebcd-110">PARAMETERS</span></span>

### <span data-ttu-id="2ebcd-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="2ebcd-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="2ebcd-112">Czy ruch przesyłany dalej z maszyn wirtualnych w lokalnej sieci wirtualnej będzie dozwolony/zabronione w zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="2ebcd-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="2ebcd-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="2ebcd-114">Jeśli łącza bramy mogą być używane w zdalnej sieci wirtualnej do łączenia się z tą siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="2ebcd-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2ebcd-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="2ebcd-116">Czy maszyny wirtualne w lokalnym wirtualnym przestrzeni sieciowym będą mogły uzyskać dostęp do maszyn wirtualnych w zdalnym wirtualnym przestrzeni sieciowym.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="2ebcd-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2ebcd-117">-AsJob</span></span>
<span data-ttu-id="2ebcd-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2ebcd-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2ebcd-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="2ebcd-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="2ebcd-120">Lista bloków adresów zarezerwowanych dla tej sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="2ebcd-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2ebcd-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="2ebcd-122">Identyfikator sieci wirtualnej databricks.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="2ebcd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebcd-123">-DefaultProfile</span></span>
<span data-ttu-id="2ebcd-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebcd-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ebcd-125">-Name</span></span>
<span data-ttu-id="2ebcd-126">Nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="2ebcd-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ebcd-127">-NoWait</span></span>
<span data-ttu-id="2ebcd-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2ebcd-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ebcd-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="2ebcd-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="2ebcd-130">Lista bloków adresów zarezerwowanych dla tej sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="2ebcd-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2ebcd-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="2ebcd-132">Identyfikator zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="2ebcd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebcd-133">-ResourceGroupName</span></span>
<span data-ttu-id="2ebcd-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-134">The name of the resource group.</span></span>
<span data-ttu-id="2ebcd-135">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ebcd-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ebcd-136">-SubscriptionId</span></span>
<span data-ttu-id="2ebcd-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ebcd-138">— UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="2ebcd-138">-UseRemoteGateway</span></span>
<span data-ttu-id="2ebcd-139">Jeśli bram zdalnych można używać w tej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="2ebcd-140">Jeśli flaga ma wartość True (Prawda), a funkcja allowGatewayTransit w zdalnej komunikacji równorzędnej również ma wartość True (Prawda), sieć wirtualna będzie używać bram zdalnej sieci wirtualnej do przesyłania.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="2ebcd-141">Tylko jedna komunikacja równorzędna może mieć ustawioną dla tej flagi wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="2ebcd-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="2ebcd-142">Tej flagi nie można ustawić, jeśli sieć wirtualna ma już bramę.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="2ebcd-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2ebcd-143">-WorkspaceName</span></span>
<span data-ttu-id="2ebcd-144">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="2ebcd-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ebcd-145">-Confirm</span></span>
<span data-ttu-id="2ebcd-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ebcd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ebcd-147">-WhatIf</span></span>
<span data-ttu-id="2ebcd-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ebcd-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ebcd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebcd-150">CommonParameters</span></span>
<span data-ttu-id="2ebcd-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebcd-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ebcd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebcd-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ebcd-153">INPUTS</span></span>

## <span data-ttu-id="2ebcd-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ebcd-154">OUTPUTS</span></span>

### <span data-ttu-id="2ebcd-155">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2ebcd-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="2ebcd-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ebcd-156">NOTES</span></span>

<span data-ttu-id="2ebcd-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2ebcd-157">ALIASES</span></span>

## <span data-ttu-id="2ebcd-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ebcd-158">RELATED LINKS</span></span>

