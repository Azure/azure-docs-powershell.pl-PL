---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: f187a2704ed1f23d6cc5ac7dded1c8d9cd8ae954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008330"
---
# <span data-ttu-id="f62f8-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="f62f8-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="f62f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f62f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f62f8-103">Tworzy nowego słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="f62f8-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="f62f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f62f8-104">SYNTAX</span></span>

### <span data-ttu-id="f62f8-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f62f8-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f62f8-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="f62f8-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f62f8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f62f8-107">DESCRIPTION</span></span>
<span data-ttu-id="f62f8-108">Polecenie New-AzAvailabilityGroupListener cmdlet tworzy nowego słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="f62f8-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="f62f8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f62f8-109">EXAMPLES</span></span>

### <span data-ttu-id="f62f8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f62f8-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="f62f8-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="f62f8-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="f62f8-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="f62f8-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="f62f8-113">Tworzy nowego słuchacza grupy dostępności agListener01 dla grupy dostępności grupy dostępności001 w grupie maszyn wirtualnych SQL SQLVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="f62f8-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="f62f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f62f8-114">PARAMETERS</span></span>

### <span data-ttu-id="f62f8-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f62f8-115">-AsJob</span></span>
<span data-ttu-id="f62f8-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="f62f8-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f62f8-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="f62f8-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="f62f8-118">Nazwa grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="f62f8-118">Availability Group name.</span></span>

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

### <span data-ttu-id="f62f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62f8-119">-DefaultProfile</span></span>
<span data-ttu-id="f62f8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f62f8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f62f8-121">-IpAddress</span></span>
<span data-ttu-id="f62f8-122">Prywatny adres IP</span><span class="sxs-lookup"><span data-stu-id="f62f8-122">Private Ip Address</span></span>

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

### <span data-ttu-id="f62f8-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="f62f8-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="f62f8-124">Identyfikator równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f62f8-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="f62f8-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f62f8-125">-Name</span></span>
<span data-ttu-id="f62f8-126">Nazwa słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="f62f8-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-127">— Port</span><span class="sxs-lookup"><span data-stu-id="f62f8-127">-Port</span></span>
<span data-ttu-id="f62f8-128">Numer portu odbiorcy usługi AG.</span><span class="sxs-lookup"><span data-stu-id="f62f8-128">Port number of AG Listener.</span></span> <span data-ttu-id="f62f8-129">Wartość domyślna to 1433.</span><span class="sxs-lookup"><span data-stu-id="f62f8-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-130">-Wi-Wi-Do</span><span class="sxs-lookup"><span data-stu-id="f62f8-130">-ProbePort</span></span>
<span data-ttu-id="f62f8-131">Port 2010</span><span class="sxs-lookup"><span data-stu-id="f62f8-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="f62f8-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="f62f8-133">Identyfikator zasobu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="f62f8-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="f62f8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f62f8-134">-ResourceGroupName</span></span>
<span data-ttu-id="f62f8-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f62f8-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f62f8-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="f62f8-137">Lista identyfikatorów zasobów maszyn wirtualnych sql</span><span class="sxs-lookup"><span data-stu-id="f62f8-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="f62f8-138">-SqlVMGroupName</span></span>
<span data-ttu-id="f62f8-139">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="f62f8-139">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="f62f8-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="f62f8-141">Obiekt sql virtual machine Group.</span><span class="sxs-lookup"><span data-stu-id="f62f8-141">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f62f8-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f62f8-142">-SubnetId</span></span>
<span data-ttu-id="f62f8-143">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="f62f8-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="f62f8-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f62f8-144">-Confirm</span></span>
<span data-ttu-id="f62f8-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f62f8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f62f8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f62f8-146">-WhatIf</span></span>
<span data-ttu-id="f62f8-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f62f8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f62f8-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f62f8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f62f8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62f8-149">CommonParameters</span></span>
<span data-ttu-id="f62f8-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62f8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62f8-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f62f8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62f8-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f62f8-152">INPUTS</span></span>

### <span data-ttu-id="f62f8-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f62f8-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f62f8-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f62f8-154">OUTPUTS</span></span>

### <span data-ttu-id="f62f8-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f62f8-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="f62f8-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f62f8-156">NOTES</span></span>

## <span data-ttu-id="f62f8-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f62f8-157">RELATED LINKS</span></span>
