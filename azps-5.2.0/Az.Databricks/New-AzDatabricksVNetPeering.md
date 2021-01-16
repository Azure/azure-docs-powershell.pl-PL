---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368795"
---
# <span data-ttu-id="0557d-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="0557d-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="0557d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0557d-102">SYNOPSIS</span></span>
<span data-ttu-id="0557d-103">Tworzy komunikację równorzędną vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0557d-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="0557d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0557d-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0557d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0557d-105">DESCRIPTION</span></span>
<span data-ttu-id="0557d-106">Tworzy komunikację równorzędną vNet dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0557d-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="0557d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0557d-107">EXAMPLES</span></span>

### <span data-ttu-id="0557d-108">Przykład 1. Tworzenie komunikacji równorzędnej wirtualnej dla kostek</span><span class="sxs-lookup"><span data-stu-id="0557d-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="0557d-109">To polecenie tworzy komunikację równorzędną wirtualnej dla datakostki.</span><span class="sxs-lookup"><span data-stu-id="0557d-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="0557d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0557d-110">PARAMETERS</span></span>

### <span data-ttu-id="0557d-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="0557d-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="0557d-112">Czy ruch przekazywany z maszyn wirtualnych w lokalnej sieci wirtualnej będzie dozwolony/niedozwolony w zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0557d-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="0557d-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="0557d-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="0557d-114">Jeśli linki bramy mogą być używane w zdalnej wirtualnej sieci, aby połączyć się z tą siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="0557d-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="0557d-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0557d-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="0557d-116">Czy maszyny wirtualne w lokalnej wirtualnej przestrzeni sieciowej będą mogły uzyskiwać dostęp do maszyn wirtualnych w zdalnej przestrzeni sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0557d-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="0557d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0557d-117">-AsJob</span></span>
<span data-ttu-id="0557d-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0557d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0557d-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="0557d-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="0557d-120">Lista bloków adresów zarezerwowanych dla tej sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="0557d-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="0557d-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0557d-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="0557d-122">Identyfikator sieci wirtualnej datakostek.</span><span class="sxs-lookup"><span data-stu-id="0557d-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="0557d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0557d-123">-DefaultProfile</span></span>
<span data-ttu-id="0557d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0557d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0557d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0557d-125">-Name</span></span>
<span data-ttu-id="0557d-126">Nazwa komunikacji równorzędnej w obszarze roboczym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0557d-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="0557d-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0557d-127">-NoWait</span></span>
<span data-ttu-id="0557d-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0557d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0557d-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="0557d-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="0557d-130">Lista bloków adresów zarezerwowanych dla tej sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="0557d-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="0557d-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0557d-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="0557d-132">Identyfikator zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0557d-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="0557d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0557d-133">-ResourceGroupName</span></span>
<span data-ttu-id="0557d-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0557d-134">The name of the resource group.</span></span>
<span data-ttu-id="0557d-135">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0557d-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0557d-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0557d-136">-SubscriptionId</span></span>
<span data-ttu-id="0557d-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0557d-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0557d-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="0557d-138">-UseRemoteGateway</span></span>
<span data-ttu-id="0557d-139">Jeśli bramy zdalne mogą być używane w tej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0557d-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="0557d-140">Jeśli flaga jest ustawiona na wartość true, a allowGatewayTransit w przypadku zdalnego komunikacji równorzędnej jest również prawdą, Sieć wirtualna będzie używać bramek zdalnej sieci wirtualnej do przesyłania.</span><span class="sxs-lookup"><span data-stu-id="0557d-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="0557d-141">Dla tej flagi może być ustawiona wartość prawda tylko jednej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="0557d-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="0557d-142">Nie można ustawić tej flagi, jeśli sieć wirtualna już ma bramę.</span><span class="sxs-lookup"><span data-stu-id="0557d-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="0557d-143">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="0557d-143">-WorkspaceName</span></span>
<span data-ttu-id="0557d-144">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0557d-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="0557d-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0557d-145">-Confirm</span></span>
<span data-ttu-id="0557d-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0557d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0557d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0557d-147">-WhatIf</span></span>
<span data-ttu-id="0557d-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0557d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0557d-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0557d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0557d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0557d-150">CommonParameters</span></span>
<span data-ttu-id="0557d-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0557d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0557d-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0557d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0557d-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0557d-153">INPUTS</span></span>

## <span data-ttu-id="0557d-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0557d-154">OUTPUTS</span></span>

### <span data-ttu-id="0557d-155">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0557d-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="0557d-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0557d-156">NOTES</span></span>

<span data-ttu-id="0557d-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0557d-157">ALIASES</span></span>

## <span data-ttu-id="0557d-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0557d-158">RELATED LINKS</span></span>

